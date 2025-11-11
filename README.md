
## 🎥 AI-Powered YouTube Summarizer & QA Tool

**Technologies:** LangChain | FAISS | LLM | Streamlit | YouTube Transcript API

The **AI-Powered YouTube Summarizer & QA Tool** is an intelligent application that allows users to extract, summarize, and query insights from YouTube videos. Using **LangChain**, **FAISS**, and a **Large Language Model (LLM)**, the system can answer specific questions about a video’s content and generate concise summaries — saving hours of manual searching and watching.

This project demonstrates how **Retrieval-Augmented Generation (RAG)** can be applied to multimedia data, making video-based knowledge easily searchable and accessible through natural language.

---

### 🚀 Features

* 🧠 **Natural Language Q&A:** Ask specific questions about any YouTube video.
* 📝 **Automated Summarization:** Generate detailed or concise summaries of the video transcript.
* 🔍 **Semantic Search with FAISS:** Retrieve the most relevant transcript chunks for precise answers.
* ⚙️ **RAG Pipeline Integration:** Combines retrieval and generation for context-aware, accurate responses.
* 💻 **Interactive Streamlit Interface:** Simple and intuitive UI for non-technical users.

---

### 🧩 Tech Stack

* **Frontend:** Streamlit
* **Core Libraries:** LangChain, FAISS, YouTube Transcript API
* **Language Model:** OpenAI / IBM watsonx.ai (LLM integration)
* **Embeddings:** Sentence Transformers / OpenAI Embeddings
* **Vector Database:** FAISS (Facebook AI Similarity Search)
* **Other Tools:** `tiktoken`, `requests`, `dotenv`

---



### ⚙️ Setup Instructions

#### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/youtube-summarizer-qa.git
cd youtube-summarizer-qa
```

#### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate     # macOS/Linux
venv\Scripts\activate        # Windows
```

#### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

#### 4. Configure API Keys

Create a `.env` file in the project root:

```
OPENAI_API_KEY=your_api_key_here
```

If you’re using IBM watsonx.ai:

```
WATSONX_API_KEY=your_watsonx_key
WATSONX_URL=https://us-south.ml.cloud.ibm.com
```

#### 5. Run the App

```bash
streamlit run app.py
```

---

### 💡 How It Works

1. **Transcript Extraction:** The app retrieves the full transcript of the provided YouTube video.
2. **Chunking & Embedding:** The transcript is split into chunks, embedded, and stored in a FAISS vector database.
3. **Query Processing:** When a user asks a question, the app retrieves the most relevant chunks using FAISS.
4. **Answer Generation:** A Large Language Model (LLM) generates a precise response based on the retrieved context.
5. **Summary Creation:** Optionally, the tool can produce a summarized version of the entire video.

---

### 🧠 Example Usage

**Input:**

> “Summarize this video in 5 bullet points.”

**Output:**

* The video discusses the rise of generative AI tools in 2024.
* Key use cases include education, healthcare, and automation.
* The speaker highlights ethical concerns and data privacy.
* Demonstrates a real-time chatbot using GPT-based architecture.
* Ends with predictions for the next wave of AI innovation.

---

### 🧰 Key Components

* **LangChain:** Manages the RAG pipeline (retrieval + LLM generation).
* **FAISS:** Enables semantic similarity search for transcript segments.
* **YouTube Transcript API:** Fetches raw transcript text from videos.
* **Streamlit:** Provides a clean and interactive UI for querying and visualization.

---

### 🔮 Future Enhancements

* 🎧 Add support for automatic speech-to-text for videos without transcripts.
* 🌍 Multi-language summarization support.
* 📈 Integration with vector databases like Pinecone or ChromaDB.
* 🗂️ Option to export summaries and answers as downloadable reports.

---

### 🏆 Learning Outcomes

By completing this project, you’ll gain hands-on experience in:

* Implementing **Retrieval-Augmented Generation (RAG)** pipelines.
* Working with **vector databases** and **semantic embeddings**.
* Building **interactive LLM applications** with Streamlit.
* Applying **AI to multimedia understanding** and summarization.

---
