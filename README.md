# 🧾 RAG Pipeline for Multi-Format Customer Support Data

This project demonstrates a Retrieval-Augmented Generation (RAG) pipeline applied to a customer support ticket dataset. It simulates an enterprise environment by ingesting data from multiple formats (CSV, SQLite, PDF), embedding documents using HuggingFace models, and enabling natural language querying through ChromaDB.

---

## 📌 Project Overview

- **Goal**: Build a RAG pipeline that enables natural language question-answering over a multi-source customer support dataset.
- **Workflow**:
  - Load and clean support ticket data
  - Export cleaned data into CSV, SQLite, and PDF formats
  - Ingest documents using LangChain’s document loaders
  - Generate vector embeddings with HuggingFace
  - Store and persist documents in ChromaDB
  - Perform similarity-based search for user queries

---

## 📂 Dataset

The dataset used in this project is the [Customer Support Ticket Dataset](https://www.kaggle.com/datasets/suraj520/customer-support-ticket-dataset) available on Kaggle. It contains support tickets and resolutions from various customer service domains.

- **Source**: [Kaggle Dataset – Suraj520](https://www.kaggle.com/datasets/suraj520/customer-support-ticket-dataset)  
- **License**: CC0: Public Domain  
- **Usage**: All data used is anonymized and intended solely for educational and research purposes.

---

## 🛠️ Tools & Technologies

- **Languages & Libraries**: Python, `pandas`, `sqlite3`, `fpdf`
- **NLP Tools**: `LangChain`, `HuggingFace Transformers`, `sentence-transformers`
- **Embedding Model**: `all-MiniLM-L6-v2`
- **Vector Store**: `ChromaDB`
- **Document Loaders**: `CSVLoader`, `SQLDatabaseLoader`, `PDFMinerLoader`

---

## 🧪 Example Query

> **User Input**: "How are billing issues typically resolved?"

Returns top 3 semantically similar tickets with relevant resolutions from the embedded support data.

---

## 📁 Project Structure

```bash
.
├── Data Engineering RAG.ipynb         # Main notebook
├── data/
│   ├── support_tickets.csv            # Cleaned CSV file
│   ├── support_tickets.db             # SQLite version
│   └── support_summary.pdf            # PDF summary of sample tickets
├── chroma_db/                         # Persisted vector store
├── requirements.txt                   # (Optional) dependencies
└── README.md                          # Project documentation
