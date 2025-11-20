
# 🚀 Kalash AI Agent

An AI-powered assistant built using **n8n**, **Google Gemini**, and **Pinecone**, designed to provide instant information about the **Kalash Skill Development Club**.
The agent retrieves answers from the club brochure automatically and provides accurate, structured responses through a chat interface.

---

## 📌 Features

* 🔍 **AI Knowledge Retrieval** (Gemini + Pinecone Vector Search)
* 📄 **Automatic Brochure Ingestion** from Google Drive
* 🤖 **Chat-Based AI Assistant** for website users
* 🔄 **Automated Knowledgebase Update** when a new brochure is uploaded
* 💬 **Memory-enabled Conversations**
* ⚡ **Fast, accurate answers** structured from actual brochure data
* 🌐 **Public Chat Widget** to embed on any website

---

## 🧠 Architecture Overview

The Kalash AI Agent consists of **two main n8n workflows**:

### **1️⃣ Knowledgebase Builder (Part-1)**

Automatically updates Pinecone when a new brochure is uploaded.

**Flow:**
Google Drive Trigger → Download File → Text Splitter → Gemini Embeddings → Pinecone Insert

### **2️⃣ AI Chat Agent (Part-2)**

Handles user queries and retrieves relevant information using semantic search.

**Flow:**
Chat Trigger → Gemini LLM → Memory → Pinecone Vector Search → AI Response

---



## ⚙️ Requirements

* **n8n Account / Self-host Setup**
* **Google Drive API Credentials**
* **Google Gemini API Key**
* **Pinecone API Key**
* Pinecone Index created with:

  * Metric: cosine
  * Dimension: depends on Gemini model
* A hosted environment for the chat widget (optional)

---

## 💬 Usage

Once deployed, users can:

* Ask questions about the Kalash Skill Development Club
* Receive accurate answers sourced from brochure data
* Chat naturally with context awareness
* Use the bot 24/7 on any website

Anytime the brochure changes → agent updates automatically.

---

