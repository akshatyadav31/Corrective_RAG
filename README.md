# Corrective RAG Agentic Workflow (Local/Open Source)

**A fully local, privacy-focused, open-source Retrieval-Augmented Generation (RAG) system with corrective context filtering and AI-powered search.**

---

## ✨ Project Overview

This project demonstrates a modern RAG pipeline, running entirely on your laptop or local server, with **no cloud or paid dependencies**. Features:

- **LLM Self-Assessment**: Uses local LLM (DeepSeek-R1/Llama 3 via Ollama) to filter and improve retrieval quality.
- **Vector Database**: All documents indexed into a local Qdrant vector store (**Docker**).
- **RAG Orchestration**: Handled by LlamaIndex for modular, hackable workflow design.
- **Optional Web Search Fallback**: Integrates free search APIs (DuckDuckGo/SERP) if local data is insufficient.
- **Private, Free, Reproducible**: No data leaves your device; all tools are open source.

---

## 🛠️ Tech Stack

- **[Ollama](https://ollama.com/)** - Local LLM inference engine (DeepSeek-R1, Llama 3, or other open weights).
- **[Qdrant](https://qdrant.tech/)** - Vector database for document storage (Docker/local).
- **[LlamaIndex](https://www.llamaindex.ai/)** - Orchestrates retrieval and context assembly.
- **Python** - Core project logic, orchestration code, and CLI tools.
- **Optional:** DuckDuckGo Search API, Streamlit/Gradio frontend.

---

## 🚀 Quickstart

### Prerequisites

- [Python 3.9+](https://www.python.org/)
- [Ollama](https://ollama.com/)
- [Docker](https://www.docker.com/products/docker-desktop)

---

### 1. Clone and Create a Virtual Environment

git clone https://github.com/yourusername/corrective-rag.git
cd corrective-rag
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

---

### 2. Start the Vector Database (Qdrant)

docker pull qdrant/qdrant
docker run -p 6333:6333 qdrant/qdrant


---

### 3. Start Ollama and Pull a Model

ollama serve
ollama pull llama3 # or 'deepseek' or any supported open LLM


---

### 4. Index Documents

Customize and run:
python3 src/utils/indexer.py

---

### 5. Run Retrieval/Q&A Pipeline

python3 src/your_query_pipeline.py


---

### 6. (Optional) Access Qdrant UI

- Visit [http://localhost:6333/dashboard](http://localhost:6333/dashboard) in your browser.

---

## 🧩 Features

- Plug-and-play with any open-source LLM supported by Ollama.
- Modular structure for rapid prototyping and extension.
- Runs entirely offline for full data privacy.
- Correction step using local LLM ensures only the most relevant context is used in answers.
- Easy integration with command-line or web frontends.

---

---

## 📝 Sample Use Case

> “Given a set of technical PDFs, index and query knowledge, filtering for best context using a local LLM and retrieving supplemental info from free web search if needed.”

---

## 🙋‍♂️ Contributing

Open to all contributions, issue reports, and improvements!

---

## 📜 License

[MIT License](LICENSE) or your chosen open-source license.

---

## ⭐ Acknowledgments

- [Ollama](https://ollama.com/)
- [Qdrant](https://qdrant.tech/)
- [LlamaIndex](https://www.llamaindex.ai/)

---


