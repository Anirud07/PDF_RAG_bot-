# 🤖 PDF_RAG_bot – Terminal-Based AI PDF Assistant (RAG + GPT-4)

**PDF_RAG_bot** is a terminal-based AI assistant that allows users to ask natural language questions over any PDF and get intelligent, page-specific answers using GPT-4.

It uses **Retrieval-Augmented Generation (RAG)** architecture with **LangChain**, **OpenAI embeddings**, and a **Qdrant vector database** to deliver highly accurate, context-aware answers from your document.

---

## 🔧 Tech Stack

- 🐍 Python
- 🧠 LangChain
- 🧬 OpenAI Embeddings (`text-embedding-3-large`)
- 🤖 GPT-4.1 (Chat Completions API)
- 🧠 Qdrant (Docker-based vector DB)
- 📄 PyPDFLoader
- ⚙️ CLI-based terminal interaction

---

## 🚀 How It Works

1. **main.py**:
   - Loads a PDF
   - Splits it into chunks
   - Embeds those chunks using OpenAI
   - Stores them in Qdrant vector DB

2. **chat.py**:
   - Accepts a natural language question
   - Retrieves relevant chunks from Qdrant
   - Sends them to GPT-4 with a smart prompt
   - Displays the answer with source page numbers

Create a Virtual Environment (Optional but Recommended)
python -m venv venv
source venv/bin/activate      # Linux/macOS
venv\Scripts\activate         # Windows

Install Dependencies
pip install langchain openai python-dotenv qdrant-client langchain-community langchain-openai langchain-text-splitters

Start Qdrant Vector DB with Docker
docker compose up -d

Set Up Environment Variables
OPENAI_API_KEY=your_openai_key_here


