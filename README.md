# RAG-Powered-Chatbot-for-Transactional-Data



## 🧠 RAG-Powered Chatbot for Transactional Data

A Python-based Retrieval-Augmented Generation (RAG) chatbot that answers questions using customer transactional data.
This project uses ChromaDB for vector search and Groq LLM for generating responses based on retrieved context.

## 📌 Project Overview

This project implements a RAG chatbot for a retail company, capable of answering questions such as:

What was the total spending of a customer?

List all transactions for a specific month.

What is the average order amount?

Which product was purchased most often?

It uses vector embeddings to transform transactional data into searchable form and retrieves the most relevant records for the LLM to answer based strictly on provided context.



## Dataset

A transactions.json file is created automatically with the sample data:

[
  {"id": 1, "customer": "Amit", "product": "Laptop", "amount": 55000, "date": "2024-01-12"},

  {"id": 2, "customer": "Amit", "product": "Mouse", "amount": 700, "date": "2024-02-15"},

  {"id": 3, "customer": "Riya", "product": "Mobile", "amount": 30000, "date": "2024-01-05"},

  {"id": 4, "customer": "Riya", "product": "Earbuds", "amount": 1500, "date": "2024-02-20"},
  
  {"id": 5, "customer": "Karan", "product": "Keyboard", "amount": 1200, "date": "2024-03-01"}
]


Each transaction is converted into a descriptive text like:

“On 2024-01-12, Amit purchased a Laptop for 55000.”




## ⚙️ Key Features

### ✔ Data Preprocessing

Converts raw JSON transactions into descriptive natural language sentences.

### ✔ Embedding Generation

Uses **Sentence-Transformer (all-mpnet-base-v2)** via ChromaDB.

### ✔ Vector Store

Stores embeddings + metadata in a persistent Chroma DB.

### ✔ Similarity Retrieval

Fetches the most relevant transaction records based on cosine similarity.

### ✔ RAG Chatbot

Combines:

- Query
- Retrieved context
- Groq LLM (llama-3.1-8b-instant)

to generate accurate answers constrained to the provided data.


## 🚀 Technologies Used



| Component  | Technology                               |
| ---------- | ---------------------------------------- |
| Vector DB  | **ChromaDB**                             |
| Embeddings | **SentenceTransformerEmbeddingFunction** |
| LLM        | **Groq API**                             |
| Language   | **Python**                               |
| Storage    | JSON + Persistent Chroma VectorDB        |








