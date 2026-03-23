# GenAI Tools & Frameworks
---

## Foundations & Training

| Tool | Description |
|------|-------------|
| **PyTorch** | The dominant deep learning framework for training and researching GenAI models |
| **TensorFlow / Keras** | Google's ML platform, widely used in production pipelines |
| **JAX** | High-performance array computing with autograd, popular for large-scale research (e.g. Google DeepMind) |
| **Hugging Face Transformers** | Model hub and library for loading, fine-tuning, and sharing pretrained models |
| **PEFT / LoRA** | Parameter-efficient fine-tuning methods for adapting LLMs cheaply |
| **DeepSpeed** | Microsoft's library for distributed training of very large models |
| **Axolotl** | Config-driven fine-tuning framework built on top of Hugging Face |

---

## Orchestration & RAG

| Tool | Description |
|------|-------------|
| **LangChain** | The most widely adopted LLM orchestration framework; chains, agents, and tool use |
| **LlamaIndex** | Focused on RAG pipelines — indexing, retrieval, and querying over documents |
| **Haystack** | Open-source NLP framework for search and RAG applications |
| **DSPy** | Stanford framework for programming (rather than prompting) LLMs — optimizes prompts automatically |
| **Semantic Kernel** | Microsoft's SDK for integrating LLMs into apps (C#, Python, Java) |
| **Instructor** | Structured output extraction from LLMs using Pydantic schemas |

---

## Vector Databases

| Tool | Description |
|------|-------------|
| **Pinecone** | Fully managed vector database, developer-friendly |
| **Weaviate** | Open-source, supports hybrid search (vector + keyword) |
| **Chroma** | Lightweight, embeddable vector DB popular for prototyping |
| **Qdrant** | High-performance, written in Rust, good for production |
| **Milvus** | Scalable open-source vector DB for enterprise workloads |
| **pgvector** | Postgres extension — adds vector search to your existing DB |
| **Redis VSS** | Vector similarity search built into Redis |

---

## Inference & Model Serving

| Tool | Description |
|------|-------------|
| **vLLM** | Fast LLM inference with PagedAttention; high throughput serving |
| **Ollama** | Run LLMs locally with a simple CLI and API |
| **llama.cpp** | CPU-friendly inference for quantized models |
| **TGI (Text Generation Inference)** | Hugging Face's production serving framework |
| **Triton Inference Server** | NVIDIA's high-performance model serving platform |
| **LM Studio** | Desktop app for running local models with a UI |
| **SGLang** | Structured generation language for efficient LLM serving |

---

## Evaluation & Observability

| Tool | Description |
|------|-------------|
| **LangSmith** | LangChain's platform for tracing, debugging, and evaluating LLM apps |
| **Weights & Biases / Weave** | Experiment tracking extended to LLM eval and tracing |
| **Ragas** | Metrics framework specifically for evaluating RAG pipelines |
| **Arize Phoenix** | Open-source LLM observability and evaluation platform |
| **Braintrust** | Eval and prompt management platform |
| **PromptFoo** | CLI tool for testing and red-teaming prompts |

---

## Agents & Workflows

| Tool | Description |
|------|-------------|
| **LangGraph** | Graph-based framework for building stateful, multi-step agents |
| **AutoGen** | Microsoft's multi-agent conversation framework |
| **CrewAI** | Role-based agent orchestration — assign agents personas and tasks |
| **MCP (Model Context Protocol)** | Anthropic's open standard for connecting LLMs to tools and data sources |
| **Prefect / Apache Airflow** | Workflow orchestration for AI pipelines at scale |
| **Claude Code** | Agentic coding assistant from Anthropic, runs in the terminal |

---

## APIs & Model Providers

| Provider | Notable Models |
|----------|----------------|
| **Anthropic** | Claude 3.5 / Claude 4 family |
| **OpenAI** | GPT-4o, o1, o3 |
| **Google DeepMind** | Gemini 2.0, Gemini Flash |
| **Meta** | Llama 3 (open weights) |
| **Mistral AI** | Mistral Large, Mixtral (open weights) |
| **Cohere** | Command R+ (enterprise RAG focus) |

---

## Image, Audio & Multimodal

| Tool | Description |
|------|-------------|
| **Diffusers (HF)** | Library for diffusion models — Stable Diffusion, FLUX, etc. |
| **ComfyUI** | Node-based UI for image generation pipelines |
| **Whisper** | OpenAI's open-source speech-to-text model |
| **ElevenLabs** | High-quality text-to-speech and voice cloning API |
| **Replicate** | API platform for running open-source models in the cloud |

---
