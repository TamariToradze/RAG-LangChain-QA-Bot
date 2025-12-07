# 🚀 RAG-LANGCHAIN-QA-BOT

A PDF-based Retrieval Augmented Generation (RAG) Question-Answering Chatbot powered by IBM WatsonX foundation models, LangChain, Chroma vector database, and Gradio UI.

This application allows users to upload a PDF, extracts relevant knowledge, and uses a Large Language Model to answer questions based solely on the document content.

---

## ⭐ KEY FEATURES

- 📄 PDF Document Upload
- 🔗 RAG Pipeline Using LangChain
- 🧩 Automatic Text Chunking
- 🧠 WatsonX Embeddings + Mixtral-8x7B Model
- 📊 Chroma Vector Database Integration
- 💬 Context-Aware Question Answering
- ⚡ Lightweight Gradio Web Interface

---

## 🏗️ TECHNOLOGY STACK

| Layer | Technology |
|---|---|
| LLM Provider | IBM WatsonX.AI |
| Model Used | `mistralai/mixtral-8x7b-instruct-v01` |
| Embeddings | `ibm/slate-125m-english-rtrvr` |
| Vector DB | Chroma |
| Framework | LangChain |
| UI Layer | Gradio |

---

## 🧠 SYSTEM WORKFLOW
PDF → Load → Split → Embeddings → Chroma VectorDB → Retriever → LLM → Final Answer


### STEP-BY-STEP:
1. PDF is uploaded and parsed  
2. Text is recursively chunked into segments  
3. Each chunk is vectorized using WatsonX Embeddings  
4. Stored into Chroma DB  
5. User enters a question  
6. Retriever fetches relevant chunks  
7. WatsonX LLM forms answer based on them  

##  SET UP

Setting up the environment is required before constructing the QA Bot. Follow the instructions below.

---

### ✔ Setting up a virtual environment

A virtual environment helps isolate dependencies so packages from one project do not affect another.

In your terminal, run:

```bash
pip install virtualenv
virtualenv my_env  # create a virtual environment named my_env
source my_env/bin/activate  # activate the environment

✔ Installing necessary libraries

To build and run the QA Bot, install the required libraries. These libraries provide:

gradio – interactive UI for end users

ibm-watsonx-ai – foundation models and embedding APIs

langchain-family (langchain, community, ibm) – document processing, retrieval chain, integration layers

chromadb – vector database for embeddings

pypdf – PDF loading and parsing

Run the following inside the virtual environment:

python3.11 -m pip install \
gradio==4.44.0 \
ibm-watsonx-ai==1.1.2 \
langchain==0.2.11 \
langchain-community==0.2.10 \
langchain-ibm==0.1.11 \
chromadb==0.4.24 \
pypdf==4.3.1 \
pydantic==2.9.1 \
huggingface_hub==0.23.0
