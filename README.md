# iOS 18 RAG Agent (n8n + Pinecone + OpenAI)

This project demonstrates an end-to-end **Retrieval-Augmented Generation (RAG)** system built using **n8n**, **Pinecone**, and **OpenAI**.  
The agent answers questions about **iOS 18 features** strictly based on official documentation stored in a vector database.

---

## 🚀 Features

- Document ingestion from Google Drive
- Recursive text chunking for high-quality embeddings
- Vector storage using Pinecone
- AI Agent–based retrieval and answering
- Public hosted chat interface via n8n
- Strict document-grounded responses (no hallucinations)

---

## 🧠 Architecture Overview

![Architecture](images/architecture.jpg)

### Document Ingestion Flow
- Google Drive Trigger
- PDF download
- Recursive Character Text Splitter
- OpenAI Embeddings
- Pinecone Vector Store

### Query & Retrieval Flow
- Chat trigger
- AI Agent
- Vector Store Retriever (Pinecone)
- OpenAI Chat Model

---

## 📂 Project Structure

workflow/ → n8n workflow export
data/ → Source PDF used for vectorisation
images/ → Architecture and UI screenshots


---

## 💬 Example Question

> What new camera features are introduced in iOS 18?

The agent retrieves relevant chunks from the vector database and generates a grounded answer.

---

## 🛠️ Tech Stack

- **n8n** – Workflow automation & AI Agent
- **Pinecone** – Vector database
- **OpenAI** – Embeddings & chat model
- **Google Drive** – Document source

---

## ⚠️ Notes

- The AI agent answers **only** based on the uploaded document.
- No external knowledge or assumptions are used.

---

## 📌 Future Improvements

- Source citation per answer
- Authentication for public chat
- Multi-document namespace support
