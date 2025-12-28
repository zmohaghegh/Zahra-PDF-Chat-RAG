# 🤖 Zahra's Intelligent PDF Chatbot (RAG System)

Welcome to **Zahra's PDF Chatbot**, a high-performance **Retrieval-Augmented Generation (RAG)** application. This project enables users to have interactive conversations with any PDF document, leveraging state-of-the-art Large Language Models (LLMs) and Vector Databases.

---

## 🚀 Project Overview
In the era of Generative AI, LLMs often suffer from "hallucinations" or lack of up-to-date information. This project implements a **RAG Pipeline**, which allows the AI to act as an expert librarian: it searches through your specific PDF, finds the most relevant facts, and then generates an answer based *only* on that verified context.

---

## 🛠️ Tech Stack & Architecture
This project follows the modern AI application architecture:

* **Orchestration:** [LangChain](https://github.com/langchain-ai/langchain)
* **Vector Database:** [FAISS](https://github.com/facebookresearch/faiss) (Facebook AI Similarity Search)
* **Embeddings:** `sentence-transformers/all-MiniLM-L6-v2`
* **LLM (Generator):** `google/flan-t5-base` (Sequence-to-sequence transformer)
* **Web Interface:** [Gradio](https://github.com/gradio-app/gradio)
* **PDF Processing:** `PyPDF` & `LangChain Text Splitters`

---

## 🌟 Key Features
- **Instant Ingestion:** Upload any PDF and start chatting immediately without manual training.
- **Context-Aware Responses:** The system retrieves the top $k$ relevant segments to ensure high accuracy.
- **Hardware Optimization:** Native support for **CUDA (GPU)** for faster embeddings, with seamless fallback to CPU.
- **Scalable Chunking:** Implements `RecursiveCharacterTextSplitter` to maintain semantic coherence.
- **Branded Web UI:** A custom-designed interface for a professional user experience.

---

## 🧠 The RAG Pipeline (Step-by-Step)
1.  **Document Loading:** Raw text is extracted from the uploaded PDF.
2.  **Semantic Chunking:** The text is divided into chunks (size=1000, overlap=200).
3.  **Vector Embedding:** Each chunk is converted into a mathematical representation of its meaning.
4.  **Vector Indexing:** Vectors are stored in a **FAISS** index for high-speed searching.
5.  **Retrieval:** The system finds the most similar chunks using Euclidean distance.
6.  **Augmented Generation:** The retrieved chunks + the user query are fed into the **Flan-T5** model to generate a precise answer.

---

## 💻 Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/YOUR_USERNAME/Zahra-PDF-Chat-RAG.git](https://github.com/YOUR_USERNAME/Zahra-PDF-Chat-RAG.git)
cd Zahra-PDF-Chat-RAG

###2. Install Required Packages
###You can install all dependencies listed in the requirements.txt file:
pip install -r requirements.txt

###3. Launch the Application
###Start the interactive web interface by running:
python app.py




