# Cogyto – AI Assistant for Unlimited Productivity  

Cogyto serves knowledge-driven organizations by empowering executives, support teams, and analysts with instant insights from documents and business data, enabling all employees to save time and focus on higher-value work.

---

## Key Features  
- **Smart Memoryv – Upload reports, meeting notes, or manuals; Cogyto remembers and retrieves details instantly.
- **Real-Time Knowledge** – Combines internal data with up-to-date web search for accurate answers.
- **Proactive Assistant** – Summarizes documents, drafts or sends emails, and automates routine tasks.
- **Multilingual Supportv – Understands and responds in both English and Indonesian.
- **RAG Workflow** – Uses a plan → execute → reflect cognitive loop for accurate, refined answers.
---

## 🛠Tech Stack  

### Development  
- **Backend:** Flask, SQLAlchemy  
- **Database:** PostgreSQL (pgvector) 
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
