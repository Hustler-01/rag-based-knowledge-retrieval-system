# RAG-Based Knowledge Retrieval System

A **Retrieval-Augmented Generation (RAG)** based information retrieval system that enables users to ask questions over **custom PDF documents** and receive **context-aware answers** using Large Language Models (LLMs).

---

## 🚀 Project Overview

This project demonstrates how **Generative AI** can be combined with **semantic search** to build a document-based question-answering system. Instead of relying solely on a language model, the system retrieves relevant information from uploaded PDFs and uses it as context to generate accurate responses.

---

## 🧠 How It Works

1. Users upload one or more PDF documents through the web interface.  
2. Text is extracted from PDFs and split into smaller chunks to fit LLM context limits.  
3. Each chunk is converted into vector embeddings and stored in a **FAISS vector database**.  
4. When a user asks a question, a semantic search retrieves the most relevant chunks.  
5. The retrieved context is passed to an LLM (Google PaLM2) to generate a grounded answer.  
6. Conversational memory maintains context across multiple user queries.

---

## 🛠 Tech Stack

- **Programming Language:** Python  
- **Frameworks:** LangChain, Streamlit  
- **LLM:** Google PaLM2  
- **Vector Database:** FAISS  
- **NLP & Embeddings:** Google PaLM Embeddings  
- **PDF Processing:** PyPDF2  

---

## ✨ Key Features

- Retrieval-Augmented Generation (RAG) based architecture  
- Semantic search over custom PDF documents  
- Conversational memory for multi-turn interactions  
- Modular and easy-to-extend codebase  
- Simple and intuitive Streamlit UI  

---

## 📂 Project Structure

```text
.
├── app.py
├── src/
│   └── __init__.py
│   └── helper.py
├── .env
├── requirements.txt
└── README.md

```

---

## ⚙️ How to Run?

### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n llmapp python=3.8 -y
```

```bash
conda activate llmapp
```

### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```

### Create a `.env` file in the root directory and add your GOOGLE_API_KEY as follows:

```ini
GOOGLE_API_KEY= "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


```bash
# Finally run the following command
streamlit run app.py
```

Now,
```bash
open up : http://localhost:8501
```
