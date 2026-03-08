# Qwen-RAG-PDF-Chat


# 📚 Qwen2.5-PDF-RAG: Private Document Conversational AI

An end-to-end **Retrieval-Augmented Generation (RAG)** pipeline that allows you to "chat" with your PDF documents locally. This project leverages the power of **Alibaba's Qwen 2.5-3B** model and **LangChain** to provide accurate, context-aware answers without relying on paid APIs.

## 🚀 Features

* **Local LLM Integration:** Uses `Qwen/Qwen2.5-3B-Instruct` for high-quality English and Arabic reasoning.
* **Efficient Memory Usage:** Implements **4-bit Quantization** (via `bitsandbytes`) to run smoothly on consumer GPUs (like Google Colab T4).
* **Fast Retrieval:** Utilizes **FAISS** (Facebook AI Similarity Search) for near-instant document searching.
* **Modern LangChain LCEL:** Built using the latest **LangChain Expression Language** for a modular and scalable pipeline.

## 🛠️ Tech Stack

* **LLM:** Qwen 2.5-3B (Instruct version)
* **Framework:** LangChain (Community & HuggingFace integrations)
* **Vector Database:** FAISS
* **Embeddings:** HuggingFace `all-MiniLM-L6-v2`
* **Document Loader:** PyPDF

## 📦 Installation & Setup

1. **Clone the repository:**
```bash
git clone https://github.com/YourUsername/Qwen2.5-PDF-RAG.git
cd Qwen2.5-PDF-RAG

```


2. **Install dependencies:**
```bash
pip install transformers accelerate bitsandbytes langchain-huggingface pypdf faiss-cpu sentence-transformers langchain-community

```


3. **Run the Notebook/Script:**
Make sure to update the `pdf_path` in the code to point to your document (e.g., `Egypt.pdf`).

## 📖 How It Works

1. **Ingestion:** The PDF is loaded and split into overlapping chunks (1000 characters).
2. **Embedding:** Each chunk is converted into a high-dimensional vector using a Sentence-Transformer model.
3. **Vector Store:** Vectors are indexed in FAISS for semantic similarity searching.
4. **RAG Chain:**
* The user asks a question.
* The system retrieves the top 3 relevant chunks.
* Qwen 2.5 generates an answer based **only** on the retrieved context.



## 📋 Example

**Question:** *"What continent is Egypt located in?"* **Context:** *"...Egypt is a transcontinental country spanning the northeast corner of Africa and the southwest corner of Asia..."* **Output:** *"Egypt is primarily located in the northeast corner of Africa."*



-.

هل محتاج مساعدة في رفع الكود لـ GitHub باستخدام الـ **Git Commands**؟
