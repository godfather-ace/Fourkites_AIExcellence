
# 🧠 Building a Basic MCP Server with Python

**Author:** [Alex Merced](https://dev.to/alexmercedcoder)  
**Source:** [DEV.to - Building a Basic MCP Server with Python](https://dev.to/alexmercedcoder/building-a-basic-mcp-server-with-python-5ci7)

---

## 💡 Overview

The **Model Context Protocol (MCP)** allows AI models (like Claude) to safely interact with your **local files and tools**.  
This guide walks through building a **simple MCP server using Python** that can read both **CSV** and **Parquet** files.

> 🧠 MCP enables secure, structured communication between AI assistants and your machine.

---

## 🎯 Objectives

- Create a lightweight Python-based MCP server  
- Add tools to read **CSV** and **Parquet** files  
- Maintain a clean, modular folder structure  
- Connect your MCP server with **Claude for Desktop**

---

## 🧱 What is MCP?

**Model Context Protocol (MCP)** is a communication standard that lets LLMs safely interact with local or cloud-based resources.

You can use MCP to:
- 📂 Read and summarize local files  
- 🧰 Execute tools, scripts, or data pipelines  
- 💬 Build reusable AI workflows and prompts  

For example, Claude can call a local function (like reading a dataset) via MCP, instead of directly accessing your system.

---

## ⚙️ Folder Structure

Organize your project as follows:

```plaintext
mix_server/
│
├── tools/
│   ├── csv_reader.py
│   ├── parquet_reader.py
│
├── __init__.py
├── server.py
└── requirements.txt
```

---

## 🧩 Core Components

### `tools/csv_reader.py`
Reads a CSV file and returns basic information.

```python
import pandas as pd

def read_csv(file_path):
    df = pd.read_csv(file_path)
    return {
        "rows": len(df),
        "columns": len(df.columns),
        "preview": df.head().to_dict()
    }
```

### `tools/parquet_reader.py`
Reads a Parquet file and returns a similar summary.

```python
import pandas as pd

def read_parquet(file_path):
    df = pd.read_parquet(file_path)
    return {
        "rows": len(df),
        "columns": len(df.columns),
        "preview": df.head().to_dict()
    }
```

### `server.py`
Implements and runs the MCP server.

```python
from mcp.server import Server
from tools.csv_reader import read_csv
from tools.parquet_reader import read_parquet

server = Server("mix_server")

@server.tool()
def summarize_csv(file_path: str):
    return read_csv(file_path)

@server.tool()
def summarize_parquet(file_path: str):
    return read_parquet(file_path)

if __name__ == "__main__":
    server.run()
```

---

## ⚙️ Installation & Setup

### 1️⃣ Install Dependencies
```bash
pip install pandas pyarrow mcp
```

### 2️⃣ Run the MCP Server
```bash
python server.py
```

### 3️⃣ Connect with Claude for Desktop

You can add the MCP server configuration to your Claude app (as per the **Anthropic documentation**) to allow local tool access.

---

## 🚀 Example Usage

Once running, you can ask Claude or another MCP-compatible model:

> “Summarize the contents of my CSV file.”  
> “How many rows and columns are in my Parquet dataset?”

The MCP server will handle the request by calling your local tool and returning structured results.

---

## 📚 Resources & References

- 🔗 [MCP SDK Documentation](https://github.com/anthropics/model-context-protocol)  
- 🔗 [Claude for Desktop Setup Guide](https://docs.anthropic.com/)  
- 🔗 [Original DEV Article](https://dev.to/alexmercedcoder/building-a-basic-mcp-server-with-python-5ci7)  
- 🧰 [PyArrow Documentation](https://arrow.apache.org/docs/python/)  

---

## 🧑‍💻 Author

**Alex Merced**  
Senior Developer Advocate at [Dremio](https://dremio.com)  
[GitHub](https://github.com/alexmerced) • [Twitter](https://twitter.com/alexmercedcoder)

---

> ⚡ *Built with Python, Pandas, and love for open standards like MCP.*

