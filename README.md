# 🦙 RAG System Using Llama 2 and LlamaIndex (Q&A)

This project demonstrates a **Retrieval-Augmented Generation (RAG)** system built with **Llama 2**, **LlamaIndex**, and **Hugging Face Transformers**.  
It allows a user to upload a document, build a vector-based index, and ask natural language questions that the model answers directly from the document’s content.

---

## 📚 Overview

The system integrates:
- **Llama 2 (meta-llama/Llama-2-7b-chat-hf)** as the large language model (LLM)
- **LlamaIndex** for document indexing and retrieval
- **Hugging Face Transformers** for LLM and embedding support
- **LangChain** for embedding compatibility
- **Sentence Transformers (all-mpnet-base-v2)** for text embeddings

The workflow creates an **end-to-end question-answering system** that grounds the model’s answers in uploaded documents.

---

## ⚙️ Installation

Run the following commands in Google Colab to install dependencies:

```bash
!pip install pypdf
!pip install -q transformers einops accelerate langchain bitsandbytes
!pip install sentence_transformers
!pip install llama_index
!pip install llama-index-llms-huggingface
!pip install llama-index-llms-huggingface-api
!pip install langchain-community langchain-core
!pip install llama-index-embeddings-langchain
!pip install llama-index-llms-ollama

### 🧠 Custom NLP Document and Result

In this project, I added a **custom NLP document** inside the `/content/Data` folder.  
The document contained explanations about various **NLP and data analysis concepts**, including the definition of **iloc** in pandas.

After building the RAG index from this document, I asked the question:

> **"What is iloc?"**

The model successfully retrieved the relevant information **directly from the document** and returned the correct answer:


