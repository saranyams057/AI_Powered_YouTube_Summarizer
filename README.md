# 🎥 AI-Powered YouTube Summarizer & Q&A Tool  
### Advanced RAG-Based Video Intelligence System

---

## 📌 Project Overview

This project is an **AI-powered YouTube Video Summarizer and Question-Answering system** built using a **Retrieval-Augmented Generation (RAG)** architecture.

It extracts transcripts from YouTube videos, processes them using semantic chunking and vector embeddings, stores them in a FAISS vector database, and enables:

- ✅ Concise video summarization  
- ✅ Context-aware question answering  
- ✅ Semantic retrieval of relevant video segments  

The system leverages **LangChain**, **FAISS**, and **IBM Watsonx.ai foundation models**, with a web interface for user interaction.

---

## 🚀 Key Features

- 🎬 Extracts transcripts directly from YouTube videos  
- ✂️ Intelligent transcript chunking using `RecursiveCharacterTextSplitter`  
- 🔎 Semantic search powered by FAISS  
- 🧠 Retrieval-Augmented Generation (RAG) pipeline  
- 📝 Single-paragraph intelligent video summarization  
- ❓ Context-aware question answering  
- 🌐 Interactive web interface  
- ☁️ IBM Watsonx Granite LLM integration  

---
## Tech Stack

### Components

- **Frontend:** Streamlit  
- **Transcript Extraction:** youtube-transcript-api  
- **Text Processing:** LangChain  
- **Embeddings:** IBM Slate 30M  
- **Vector Store:** FAISS  
- **LLM:** IBM Granite 3.2 8B Instruct  
- **Framework:** LangChain  
- **Cloud AI:** IBM Watsonx.ai  


---

## 🧠 Core Components

### 1️⃣ Transcript Extraction
- Library: `youtube-transcript-api`
- Prioritizes manually created transcripts over auto-generated ones

---

### 2️⃣ Text Processing
- Transcript formatting with text + timestamps
- Chunking using `RecursiveCharacterTextSplitter`
  - `chunk_size = 200`
  - `chunk_overlap = 20`

---

### 3️⃣ Embedding Model
- Model: `ibm/slate-30m-english-rtrvr-v2`
- Generates dense semantic embeddings
- Used to build FAISS vector index

---

### 4️⃣ Vector Database
- Library: `FAISS (faiss-cpu)`
- Enables efficient similarity search
- Retrieves top-k relevant transcript chunks

---

### 5️⃣ Language Model
- Model: `ibm/granite-3-2-8b-instruct`
- Used for:
  - Video summarization
  - Context-based Q&A
- Decoding Method: `GREEDY`
- Max Tokens: `900`

---

## 🔎 RAG Implementation

### 🔹 Summarization Pipeline
1. Fetch transcript
2. Process transcript
3. Pass full transcript to LLM
4. Generate concise summary

### 🔹 Q&A Pipeline
1. Chunk transcript
2. Generate embeddings
3. Store in FAISS
4. Retrieve top-k relevant chunks
5. Pass retrieved context + question to LLM
6. Generate structured answer

---

## 🖥️ User Interface

The application provides:

- Input field for YouTube URL
- Button to generate video summary
- Input field for user question
- Button to generate answer



---

## 📦 Prerequisites & Required Libraries

To ensure seamless execution, install the following libraries:

### Core Dependencies

- `youtube-transcript-api` – Extract transcripts from YouTube videos  
- `faiss-cpu` – Efficient similarity search  
- `langchain` – Text processing and LLM chaining  
- `langchain-community` – FAISS vector store integration  
- `ibm-watsonx-ai` – Access IBM Watsonx foundation models  
- `langchain-ibm` – IBM + LangChain integration  
- `streamlit` – Web application interface  

---

## 📥 Installation

```bash
pip install youtube-transcript-api
pip install faiss-cpu
pip install langchain
pip install langchain-community
pip install ibm-watsonx-ai
pip install langchain-ibm
pip install streamlit

---
```
## ⚙️ Configuration

Update IBM Watsonx credentials in your script:

```python
from ibm_watsonx_ai import Credentials

credentials = Credentials(url="https://us-south.ml.cloud.ibm.com")
project_id = "your_project_id"

```
---

## How to Run

Run the application using:

```bash
python app.py

```


## Use Cases

- Educational video summarization
- Research content analysis
- Interview preparation
- Extracting insights from long-form video content
- Multimedia knowledge retrieval systems

## Conclusion

This project demonstrates a practical implementation of Retrieval-Augmented Generation (RAG) for multimedia intelligence.

By combining transcript extraction, semantic embeddings, vector search, and IBM Watsonx foundation models, the system transforms YouTube videos into an intelligent, searchable knowledge base.

