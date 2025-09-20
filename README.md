# Cogyto – AI Assistant for Unlimited Productivity  

Cogyto is an **AI-powered personal assistant** built on **LLaMA** that helps you work smarter.  
It processes your documents, retrieves insights from internal + external sources, and even automates tasks like summarizing reports, drafting emails, or sending notifications.  

Stop searching manually. Start working intelligently.  

---

## Key Features  

- 🧠 **Smart Memory** – Upload documents, and Cogyto remembers + retrieves details instantly.  
- 🌐 **Real-Time Knowledge** – Blends internal data with live web search for accurate, updated answers.  
- ⚡ **Proactive Assistant** – Summarizes, drafts, and executes simple tasks (emails, reports, alerts).  
- 🌍 **Multilingual Support** – Works in English and Indonesian.  
- 🔄 **Cognitive Workflow** – Uses *plan → execute → reflect* loop for accuracy and reliability.  
- 📊 **Enterprise-Ready** – Modular, scalable, and integrates easily with business workflows.  

---

## 🛠Tech Stack  

### Development  
- **Backend:** Flask, SQLAlchemy  
- **Database:** PostgreSQL (pgvector) or ChromaDB (local dev)  
- **Knowledge Graph:** Neo4j  
- **LLM:** LLaMA  
- **APIs & Tools:** Tavily, SerpAPI (search), Hugging Face Transformers (NLP/vision), smtplib (email)  
- **Frontend:** HTML, CSS, JavaScript (real-time chat UI)  

### Production (AWS)  
- **LLM Hosting:** LLaMA via Amazon Bedrock / SageMaker  
- **Vector Store:** Amazon Aurora PostgreSQL (pgvector)  
- **Storage:** Amazon S3 (documents, backups)  
- **Backend:** Flask/FastAPI with SQLAlchemy  
- **Orchestration:** LangChain / LlamaIndex  
- **Frontend:** HTML, CSS, JavaScript (streaming-enabled)  

---

## Project Structure  

```bash
cogyto/
├── run.py                 # App entry point
├── config.py              # Config & env variables
├── app/
│   ├── routes/            # API endpoints (chat, kb, main)
│   ├── services/          # Business logic (chat, uploads, sessions)
│   ├── agents/            # Agentic framework (executor, prompts, memory manager)
│   ├── tools/             # Modular tools (web search, vision, email, knowledge graph)
│   ├── models/            # SQLAlchemy models (conversations, etc.)
│   └── utils/             # Text utils (cleaning, translation, language detection)
├── static/                # Frontend assets (HTML, CSS, JS)
└── docs/                  # Documentation
```
---
## How It Works (User Journey)  

1. **Ask or Upload** – Users start by typing a question or uploading documents.  
2. **Plan** – Cogyto,Creates a step-by-step reasoning plan to solve the query.  
3. **Execute** – The system calls the right tools (vector search, knowledge graph, web search, vision analysis, etc.) to gather information.  
4. **Reflect & Refine** – Reviews the draft answer, checks accuracy, and improves clarity before finalizing.  
5. **Deliver** – The user instantly receives a refined, contextual response enriched with insights.  

---

## Roadmap
- Add multimodal support (images, videos)
- Smarter long-term memory & personalization
- Caching & batch reranking for speed
- Improved UI with workflow visualizations
