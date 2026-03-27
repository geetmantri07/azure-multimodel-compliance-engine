# 🎯 Compliance Guardian AI  
### Multimodal AI System for Automated Advertisement Compliance Auditing

---

## 🚀 Overview

**Compliance Guardian AI** is an end-to-end multimodal AI system that automatically audits advertisement videos for regulatory compliance.

The system analyzes video content using:
- 🎥 Transcript (speech)
- 📝 OCR (on-screen text)
- 📄 Compliance policy documents

It then evaluates whether the advertisement violates predefined compliance rules using:
- Azure AI services
- Vector search (RAG pipeline)
- Large Language Models (LLMs)

---

## 🔥 Key Features

- ✅ Automated compliance checking for advertisement videos  
- 🎥 Multimodal analysis (Audio + Visual text)  
- 📄 Policy-based reasoning using real compliance documents  
- ⚡ Retrieval-Augmented Generation (RAG) pipeline  
- 🧠 LLM-based intelligent decision making  
- 📊 Structured compliance reports (JSON + readable summary)  
- 🐳 Fully Dockerized for easy deployment  
- 📡 LangGraph orchestration + LangSmith tracing  

---

## 🧱 System Architecture

The system is divided into 3 major components:

---

### 1️⃣ Knowledge Base Creation

- Load compliance PDFs
- Split into chunks
- Generate embeddings
- Store in vector database (Azure AI Search)

---

### 2️⃣ Video Processing Pipeline

1. User provides YouTube URL  
2. Video is downloaded using `yt-dlp`  
3. Uploaded to Azure Blob Storage  
4. Azure Video Indexer extracts:
   - Transcript (speech-to-text)
   - OCR text (on-screen content)

---

### 3️⃣ RAG + LLM Pipeline

1. Combine transcript + OCR  
2. Convert to embeddings  
3. Perform semantic search on compliance policies  
4. Inject retrieved policies into prompt  
5. Use LLM (GPT-4o-mini) for reasoning  
6. Generate structured compliance report  

---

## 🧠 Tech Stack

### 🔹 Backend
- Python
- FastAPI

### 🔹 AI / ML
- Azure OpenAI (Embeddings + LLM)
- LangChain
- LangGraph

### 🔹 Data Processing
- PyPDFLoader
- RecursiveCharacterTextSplitter

### 🔹 Storage
- Azure Blob Storage
- Azure AI Search (Vector DB)

### 🔹 Video Processing
- yt-dlp
- Azure AI Video Indexer

### 🔹 Observability
- LangSmith

### 🔹 Deployment
- Docker
- Docker Hub

---

## 📂 Project Structure

