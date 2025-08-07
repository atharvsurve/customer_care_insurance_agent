# Insurance Customer Support Assistant (RAG + LangGraph)

> An intelligent customer support pipeline that uses **LangGraph**, **LangChain**, and **Retrieval-Augmented Generation (RAG)** to respond to insurance-related queries with document-grounded accuracy and smart agent routing.

---

## Project Overview

This project leverages a **modular AI-driven customer support system** built on top of:

-  **LangGraph**: For constructing dynamic, stateful agent workflows.
-  **LangChain**: To orchestrate prompt chaining, memory, and RAG capabilities.
-  **RAG (Retrieval-Augmented Generation)**: Uses real insurance PDFs for contextually accurate answers.
-  **LLM design**: local models served via **LM Studio**.
-  **Smart Routing**: Directs each query to its relevant domain-specific agent.

---

##  Features

###  Intelligent Categorization
Classifies customer queries into fine-grained insurance subcategories:


### Agent-Based Workflow
Based on the query's **category** and **sentiment**, the system routes it to:

- `claims_agent`
- `renewal_agent`
- `premium_agent`
- `exclusions_agent`
- `coverage_agent`
- `handle_general` (fallback)
- `escalate` (if sentiment is negative)

### Sentiment-Aware Escalation
Escalates sensitive or dissatisfied user queries to human support.

### RAG-Powered Accuracy
All domain answers are **backed by your company’s policy documents** using FAISS vector search.

---

## Tech Stack

| Component            | Tool / Library                            |
|---------------------|--------------------------------------------|
| LLMs                | LM Studio (Local Model)           |
| Workflow Engine     | LangGraph                                  |
| Prompt Management   | LangChain                                  |
| Retrieval           | FAISS + HuggingFace Embeddings             |
| PDF Parsing         | LangChain Community (PyPDFLoader)          |
| Text Splitting      | RecursiveCharacterTextSplitter             |

---

## Folder Structure

