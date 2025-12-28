# Teddy – Multimodal Local AI Assistant

**Teddy** is a privacy-first, offline-capable desktop assistant built with a hybrid architecture. It combines the performance of a **Go (Wails)** desktop shell with the rich AI ecosystem of **Python (FastAPI)** to deliver powerful **Retrieval-Augmented Generation (RAG)** and **multimodal analysis**, entirely on your local machine.

---

## 🚀 Key Features

- **🔒 Privacy-First & Offline**  
  Runs fully on your local machine using **Ollama**. No data leaves your device.

- **🧠 Advanced RAG System**  
  Context-aware answers from your local documents (PDF, TXT, MD, DOCX).
  - **Intelligent Routing:** Automatically decides whether a query requires document context or general reasoning.
  - **Hybrid Search:** Semantic embedding-based retrieval for high-precision results.

- **👁️ Multimodal Vision**  
  Drag-and-drop images for real-time analysis using **Qwen 2.5-VL**.

- **🎙️ Voice Interaction**  
  Integrated Speech-to-Text for hands-free interaction.

- **⚡ Hybrid Architecture**
  - **Frontend:** React + Vite, wrapped in Go using Wails for a native desktop UI.
  - **Backend:** FastAPI (Python) for AI orchestration and heavy processing.

---

## 🛠️ Tech Stack

### Frontend / App Layer
- **Wails:** Go-based framework for building native desktop applications
- **React:** UI layer
- **TailwindCSS:** Styling

### AI Backend
- **Python + FastAPI:** REST API for AI workflows
- **Ollama:** Local LLM runtime
- **LangChain:** RAG orchestration
- **ChromaDB:** Vector store for document embeddings

### Models Used
- **Text / Chat:** `gemma3:12b` (configurable)
- **Vision:** `qwen2.5vl:7b`

---

## ⚙️ Prerequisites

Ensure the following are installed:

1. **Go** (v1.23+)
2. **Node.js** (v18+)
3. **Python** (v3.10+)
4. **Ollama**

Pull the required models:

```bash
ollama pull gemma3:12b
ollama pull qwen2.5vl:7b
```

---

## 📦 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/teddy.git
cd teddy
```

### 2. Backend Setup (Python)

```bash
cd backend
python -m venv venv
```

Activate the virtual environment:

**Windows**
```bash
.\venv\Scripts\activate
```

**macOS / Linux**
```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### 3. Frontend Setup

```bash
cd ../frontend
npm install
```

---

## 🖥️ Running the Application

### Development Mode (Recommended)

```bash
wails dev
```

### Backend (if not auto-started)

```bash
cd backend
python ../start_fastapi.py
```

---

## 📦 Building for Production

```bash
wails build
```

---

## 📁 Project Structure

```text
Teddy/
├── backend/
├── frontend/
├── build/
├── app.go
├── main.go
└── wails.json
```

---

## 📄 License

MIT License
