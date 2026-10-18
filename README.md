# Varun Kambali

**AI Engineer · Production RAG, AI Agents & LLM Evaluation** · Bengaluru, India

I build production LLM systems on Google Cloud (retrieval-augmented generation, agents and search) for enterprise clients in SaaS, legal and travel. 3+ years, all of it in production ML and GenAI. Currently Senior AI Engineer at Searce (formerly Cloudside Technologies).

**[Portfolio](https://varun-kambali.github.io)**: an evidence map that links every skill to the work behind it · [LinkedIn](https://www.linkedin.com/in/varunkambali) · [kambalivarun@gmail.com](mailto:kambalivarun@gmail.com)

## Shipped in production
Client work is under NDA, so it is described at resume level. The IDs match my resume.

| | Work | Result |
|---|---|---|
| E1 | **Agentic NL2SQL** for executive reporting: a self-correcting loop validates and repairs SQL before execution | 92% execution accuracy on 500+ evaluation questions, across 20 markets |
| E3 | **Multi-tenant RAG platform** (FastAPI, PostgreSQL, Azure AD SSO) with a 4-stage agent pipeline: routing, datastore selection, grounded synthesis, citation verification | Tenant onboarding cut from 1–2 days to under 5 minutes |
| E5 | **Hybrid search over 10M+ assets** for a screen-capture SaaS: PGVector with keyword-weighted ranking (HNSW + weighted RRF). Led 3 engineers | 10M+ screenshots, audio, video and files |
| E6 | **Multimodal enrichment pipeline**, event-driven on Gemini (Pub/Sub, Cloud Functions, BigQuery): OCR, diarized transcription, metadata extraction | 2M+ captures/month |
| E7 | **LLM evaluation tool** (async Python, LiteLLM, Streamlit): benchmarks models in parallel with a Gemini Flash judge on 4 criteria, plus latency and token cost | 5+ models compared at once; the AI team's standard for model selection |

## Building in public
My client code can't be shared, so these open-source projects are the code you can read. Each one ships with a committed eval suite, and its headline number goes here once it exists.

<!-- When a project ships: link the repo and demo, and copy the headline row from its evals/results/summary.md word for word. -->

| | Project | What it is | Status |
|---|---|---|---|
| P1 | Nutrition MCP server | MCP tools that give AI assistants sourced, unit-correct nutrition data for Indian and global foods, measured with and without the tools | In progress |
| P2 | Meal-planner multi-agent | LangGraph agents plan a week of meals within calorie, protein, diet and budget limits. Macros checked in code, Langfuse traces, evals gate CI | Next |
| P3 | Household docs vault | Private document AI on a LoRA-fine-tuned open-weight model, running locally: field extraction, expiry reminders, answers with citations | Planned |

## Stack
- **LLMs and agents:** Gemini, Claude, Google ADK, LangGraph, LlamaIndex, LiteLLM · RAG, NL2SQL, structured outputs
- **Retrieval and data:** PostgreSQL/PGVector, Vertex AI Vector Search, FAISS, Neo4j, BigQuery · hybrid search (HNSW, RRF)
- **Evaluation:** LLM-as-judge, eval datasets, model benchmarking (quality, latency, cost), LangSmith tracing
- **Backend:** Python, SQL, FastAPI, REST APIs, SSE streaming, Docker, Git, CI/CD, Streamlit
- **Google Cloud:** Vertex AI (Gemini API, Pipelines), Gemini Enterprise, Cloud Run, Cloud Functions, Pub/Sub, Cloud SQL

## Certifications
- Google Cloud: [Professional Machine Learning Engineer](https://www.credly.com/badges/fc7321c1-5f35-4efa-bbdc-9a7fc50a396c/public_url) · [Professional Data Engineer](https://www.credly.com/badges/f01c5619-78fe-4579-b777-d2562682709d/public_url)
- Google Cloud Partner Specialist: [Gemini Enterprise Deployment](https://www.credly.com/badges/f5f99e6d-0f08-45de-b012-68b6bdfeef9e/public_url) · [Gemini Enterprise Agent Development](https://www.credly.com/badges/9c00a470-a883-4dbb-b8cf-a7c9ab90938d/public_url)
- Anthropic: [Claude Certified Architect – Foundations](https://www.credly.com/badges/3fbe6b0c-df1b-4581-9262-d668d5edcb5f/public_url)
