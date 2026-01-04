# CFPB Complaint Analysis for RAG System

## Project Overview
This project focuses on analyzing and preparing consumer complaint data from the Consumer Financial Protection Bureau (CFPB) for use in a Retrieval-Augmented Generation (RAG) system. The goal is to build a foundation for semantic search and question answering over consumer complaints related to selected financial products.

This repository currently contains work completed up to **TASK** for the interim submission.
---

## 📌TASK 1: Exploratory Data Analysis and Preprocessing 

### 📁Dataset
The CFPB consumer complaint dataset was used a sprimary data source. Initial exploration was performed to understand the dataset structure, available fields and data quality.

### Filtering
The dataset was filtered in the following manner:
- Only complaints with **non-empty consumer complaint narratives** were retained.
- Complaints were restricted to the targeted product categories relevant to the requirement(e.g., credit cards, personal loans, savings accounts and money transfers).

### Exploratory Data Analysis
Key exploratory steps included:
- Inspecting dataset size and analyzing distribution of complaints across products
- Measuring complaint narratives lengths and visualizing its distribution

These insights informed downstream decisions such as the need for text chunking in later tasks.

### Text Preprocessing
Basic text cleaning to improve embedding quality included:
- Lowercasing text
- Removving Special characters and
- Normalizing whitespaces
---
## Data Handling Note
The cleaned dataset was saved to the data/processed/ directory

## Project / Repository Structure
rag-complaint-chatbot/

├── .vscode/

│   └── settings.json

├── .github/

│   └── workflows/

│       └── unittests.yml

├── data/

│   ├── raw/                       

│   └── processed/

├── vector_store/                   # Persisted FAISS/ChromaDB index

├── notebooks/

│   ├── __init__.py

│   └── README.md

├── src/

│   ├── __init__.py

├── tests/

│   ├── __init__.py

├── app.py                          # Gradio/Streamlit interface

├── requirements.txt

├── README.md

└── .gitignore