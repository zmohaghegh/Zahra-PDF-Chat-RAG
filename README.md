# Zahra's Intelligent PDF Chatbot (RAG System) 🤖📚

This repository contains a professional-grade **Retrieval-Augmented Generation (RAG)** system developed by **Zahra**. The system allows users to upload any PDF document and interact with its content using state-of-the-art Natural Language Processing (NLP) models.

## 🚀 Overview
Traditional LLMs are limited by their training data. This project overcomes that limitation by implementing a RAG pipeline, which enables the model to fetch and reason over external PDF documents in real-time without the need for expensive fine-tuning.

## 🛠️ Tech Stack
- **Framework:** [LangChain](https://github.com/langchain-ai/langchain) (for RAG orchestration)
- **Vector Database:** [FAISS](https://github.com/facebookresearch/faiss) (Facebook AI Similarity Search)
- **Embeddings:** `all-MiniLM-L6-v2` (via Hugging Face Transformers)
- **LLM:** `Flan-T5-base` by Google
- **UI:** [Gradio](https://github.com/gradio-app/gradio) for a web-based interactive interface
- **Environment:** Google Colab / Python 3.12

## 🧠 How It Works
1. **Document Loading:** PDF files are parsed using `PyPDFLoader`.
2. **Text Splitting (Chunking):** Uses `RecursiveCharacterTextSplitter` to maintain semantic context within 1000-character windows.
3. **Vectorization:** Text chunks are converted into 384-dimensional dense vectors.
4. **Similarity Search:** When a user asks a question, the system finds the most relevant document chunks using Euclidean distance.
5. **Contextual Generation:** The LLM receives the question along with the retrieved context to generate a factual, grounded answer.

## 💻 Installation & Usage
To run this project locally or on Google Colab:

1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Zahra-Chat-PDF-RAG.git](https://github.com/YOUR_USERNAME/Zahra-Chat-PDF-RAG.git)
