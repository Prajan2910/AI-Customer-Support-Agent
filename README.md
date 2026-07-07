# 🤖 AI-Powered Customer Support Automation System

An intelligent **Customer Support Automation System** built using **LangGraph**, **Ollama (Qwen2.5:3B)**, **Retrieval-Augmented Generation (RAG)**, **SQLite Memory**, and **Human-in-the-Loop (HITL)** approval workflow.

The system automates customer support by classifying customer queries, routing them to specialized support agents, retrieving relevant company knowledge, maintaining conversation memory, and escalating sensitive requests for human approval.

---

## 📌 Features

- ✅ AI-powered Intent Classification
- ✅ LangGraph Workflow Orchestration
- ✅ Intelligent Query Routing
- ✅ Specialized Support Agents
  - Sales Support
  - Technical Support
  - Billing Support
  - Account Support
- ✅ Retrieval-Augmented Generation (RAG)
- ✅ FAISS Vector Database
- ✅ SQLite Conversation Memory
- ✅ Human-in-the-Loop Approval
- ✅ Supervisor Agent Validation
- ✅ Rich Terminal User Interface
- ✅ Local LLM using Ollama (No API Keys Required)

---

# 🏗️ System Architecture

```
                Customer Query
                       │
                       ▼
             Intent Classification
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
      Memory         Department      HITL
      Recall          Routing      (if needed)
                       │
        ┌──────┬───────┼────────┬───────┐
        ▼      ▼       ▼        ▼
     Sales  Technical Billing Account
        │      │       │        │
        └──────┴───────┴────────┘
                   │
             RAG Retrieval
                   │
            Supervisor Agent
                   │
          Final Customer Response
```

---

# 📂 Project Structure

```text
Customer_Support_AI/
│
├── agents/
│   ├── classifier.py
│   ├── sales.py
│   ├── technical.py
│   ├── billing.py
│   ├── account.py
│   ├── supervisor.py
│   └── human.py
│
├── data/
│   ├── company_policy.txt
│   ├── pricing_guide.txt
│   ├── technical_manual.txt
│   └── faq.txt
│
├── graph/
│   ├── builder.py
│   ├── routes.py
│   └── state.py
│
├── memory/
│   ├── memory.py
│   └── memory.db
│
├── rag/
│   ├── loader.py
│   ├── retriever.py
│   └── rag_node.py
│
├── app.py
├── config.py
├── requirements.txt
├── README.md
│
├── diagrams/
│   └── workflow.png
│
└── screenshots/
```

---

# ⚙️ Prerequisites

- Python **3.13.5**
- Git
- Ollama

Verify Python:

```bash
python --version
```

Expected Output

```text
Python 3.13.5
```

---

# 🚀 Installation

## 1. Clone Repository

```bash
git clone https://github.com/<your-username>/Customer_Support_AI.git
cd Customer_Support_AI
```

---

## 2. Create Virtual Environment

```bash
python -m venv .venv
```

### Activate

**Windows**

```bash
.venv\Scripts\activate
```

**Linux/macOS**

```bash
source .venv/bin/activate
```

---

## 3. Upgrade pip

```bash
python -m pip install --upgrade pip setuptools wheel
```

---

## 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🤖 Install Ollama

Download Ollama:

https://ollama.com/download

Verify:

```bash
ollama --version
```

---

# 📥 Download Required Models

### Chat Model

```bash
ollama pull qwen2.5:3b
```

### Embedding Model

```bash
ollama pull nomic-embed-text
```

Verify:

```bash
ollama list
```

Expected:

```text
qwen2.5:3b
nomic-embed-text
```

---

# ▶️ Start Ollama

```bash
ollama serve
```

Leave this terminal running.

---

# ▶️ Run the Project

```bash
python app.py
```

---

# 🧠 Knowledge Base

The RAG pipeline retrieves information from:

- Company Policy
- Pricing Guide
- Technical Manual
- FAQ Document

The FAISS vector database is created automatically during the first execution.

---

# 💾 Conversation Memory

SQLite stores customer conversations.

Example:

```
Customer:
My name is David.

Customer:
I have a billing issue.

Customer:
What was my previous support issue?
```

The AI retrieves the previous interaction directly from SQLite memory.

---

# 👨‍💼 Human-in-the-Loop Approval

The following requests require supervisor approval before responding:

- Refund Requests
- Subscription Cancellation
- Account Closure
- Compensation Requests
- Escalation to Management

---

# 📋 Sample Queries

### Sales

```
What are the pricing plans available for your software?
```

---

### Account

```
I forgot my account password.
```

---

### Technical Support

```
My application crashes whenever I upload a file.
```

---

### Billing (Human Approval)

```
I need a refund for my annual subscription.
```

---

### Memory Recall

```
What was my previous support issue?
```

---

# 🛠 Technology Stack

| Component | Technology |
|------------|------------|
| Language | Python 3.13.5 |
| Workflow | LangGraph |
| LLM | Ollama (Qwen2.5:3B) |
| Embeddings | nomic-embed-text |
| Vector Database | FAISS |
| Memory | SQLite |
| RAG | LangChain |
| UI | Rich |
| IDE | VS Code |

---

# ✅ Assignment Requirements Covered

| Task | Status |
|------|--------|
| LangGraph Workflow | ✅ |
| State Management | ✅ |
| Intent Classification | ✅ |
| Conditional Routing | ✅ |
| Specialized Support Agents | ✅ |
| RAG Integration | ✅ |
| SQLite Memory | ✅ |
| Human-in-the-Loop Workflow | ✅ |
| Supervisor Agent | ✅ |
| Demonstration | ✅ |

---

# 📸 Project Outputs

The project includes:

- LangGraph Workflow Diagram
- Agent Routing
- RAG Retrieval
- SQLite Memory Storage
- Human Approval Workflow
- Supervisor Validation
- Final Customer Response
- Execution Screenshots

---

# 👨‍💻 Author

**Prajan Kannan**

Electronics and Computer Engineering

AI • Machine Learning • Data Engineering • Agentic AI

---

# 📄 License

This project was developed for academic and educational purposes as part of an AI Agent application using LangGraph and Ollama.
