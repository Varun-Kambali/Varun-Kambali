<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <img alt="Varun Kambali, AI Engineer in Bengaluru: production RAG, AI agents and LLM evaluation" src="assets/header-light.svg" width="100%">
</picture>

<p align="center">
  <a href="https://varun-kambali.github.io"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-18181B?style=for-the-badge&logo=githubpages&logoColor=FDE68A"></a>
  <a href="https://www.linkedin.com/in/varunkambali"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge"></a>
  <a href="mailto:kambalivarun@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-18181B?style=for-the-badge&logo=gmail&logoColor=FDE68A"></a>
</p>

## Hi, I'm Varun

I like getting to the root of things. Give me a system that is misbehaving and I'll go looking for the bottleneck that is actually causing it, and for the pattern that isn't obvious at first glance but matters to the people who use it.

I'm a Senior AI Engineer at Searce in Bengaluru. For 3+ years I've built LLM systems that run in production on Google Cloud (retrieval, agents, search and evaluation) for enterprise clients in SaaS, legal and travel. More about me on my [portfolio](https://varun-kambali.github.io).

## What I've shipped at work

**Agents and RAG that check their own work**

- **92% execution accuracy on 500+ evaluation questions.** I built an NL2SQL and vector-search reporting agent for executive leadership in 20 markets. A self-correcting loop validates and repairs the SQL before it runs.
- **Tenant onboarding cut from 1–2 days to under 5 minutes.** I architected a multi-tenant RAG platform (FastAPI, PostgreSQL, Azure AD SSO) with a 4-stage agent pipeline: routing, datastore selection, grounded synthesis and citation verification.

**Search and data at scale**

- **Search over 10M+ screenshots, audio, video and files.** I led 3 engineers building search for a screen-capture SaaS, moving it to PostgreSQL/PGVector with keyword-weighted hybrid ranking (HNSW + weighted RRF).
- **2M+ captures a month made searchable.** I built the event-driven Gemini pipeline behind that search (Pub/Sub, Cloud Functions, BigQuery): OCR, speaker-labelled transcription and metadata extraction.
- **New-market onboarding from multi-day deployments to under a minute.** I designed a config-driven, partitioned BigQuery ingestion engine for the same 20 markets, so adding one is a config change.

**Evaluation and client delivery**

- **The AI team's standard for choosing models.** My evaluation tool runs 5+ models in parallel on the same prompts, scores them with a Gemini Flash judge on 4 criteria, and adds latency and token cost (async Python, LiteLLM, Streamlit).
- **An MVP that became a production engagement.** I led discovery, design and delivery of a Gemini Enterprise MVP with a custom BigQuery natural-language analytics agent over 10 datasets (100+ tables).

## Open-source projects

I build these in my own time, and each one ships with its own evals.

<!-- sync:projects:start -->
### [Nutrition MCP server](https://github.com/Varun-Kambali/nutrition-mcp) · shipped v1.0.0

When I asked AI assistants how much protein is in 2 rotis and a katori of rajma, I got a confident number with no source and no portion. So I built an open-source MCP server that any agent can call for sourced nutrition on 41 Indian dishes and 66 ingredients, in grams or household measures. Dish values are computed in code from USDA and CoFID ingredient data and recipes I wrote, so the model never does the arithmetic.

From memory, Gemini was off by 16.0% on calories. With the server's tools it used the computed totals on 26 of 26 questions. A CI gate checks 18 dishes against independent CoFID and USDA records, at 18.7% average calorie error.

[Why I built it](https://github.com/Varun-Kambali/nutrition-mcp/blob/main/docs/case-study.md) · [Eval results](https://github.com/Varun-Kambali/nutrition-mcp/blob/main/evals/results/summary.md)

### [Meal-planner multi-agent](https://github.com/Varun-Kambali/meal-planner-agents) · shipped v1.0.0

I follow a meal plan I wrote myself. Writing the rules was quick; finding recipes that hit each meal's numbers, fit my kitchen and don't repeat was the slow part. Here you enter your plan's rules once, LangGraph agents write a week of recipes, my nutrition MCP server supplies every number, and plain Python checks each recipe and day, sending failures back for repair. Then it tracks what you actually eat against the plan.

479 of 553 recipes pass every check, against 46 of 553 when a single model call writes the whole week. Evals gate CI, and the Langfuse traces mask every string except ids.

[Live demo](https://varun-kambali.github.io/meal-planner-agents/) · [Why I built it](https://github.com/Varun-Kambali/meal-planner-agents/blob/main/docs/case-study.md) · [Eval results](https://github.com/Varun-Kambali/meal-planner-agents/blob/main/evals/results/summary.md)

Up next: **Household docs vault**, private document AI that runs locally: field extraction, expiry reminders and cited answers, on a LoRA-fine-tuned open-weight model.
<!-- sync:projects:end -->

<sub>Updated <!-- sync:stamp:start -->10 Nov 2026<!-- sync:stamp:end --></sub>

## Arsenal

| Area | Tools and patterns |
|---|---|
| **LLMs & agents** | ![Gemini](https://img.shields.io/badge/Gemini-1C1917?style=for-the-badge&logo=googlegemini&logoColor=FDE68A) ![Claude](https://img.shields.io/badge/Claude-1C1917?style=for-the-badge&logo=claude&logoColor=FDE68A) ![LangGraph](https://img.shields.io/badge/LangGraph-1C1917?style=for-the-badge&logo=langgraph&logoColor=FDE68A) ![Google ADK](https://img.shields.io/badge/Google_ADK-1C1917?style=for-the-badge&logo=googlecloud&logoColor=FDE68A) ![LlamaIndex](https://img.shields.io/badge/LlamaIndex-1C1917?style=for-the-badge) ![LiteLLM](https://img.shields.io/badge/LiteLLM-1C1917?style=for-the-badge) |
| **Patterns** | ![RAG](https://img.shields.io/badge/RAG-3F3F46?style=for-the-badge) ![Agents](https://img.shields.io/badge/Agent_pipelines-3F3F46?style=for-the-badge) ![NL2SQL](https://img.shields.io/badge/NL2SQL-3F3F46?style=for-the-badge) ![Structured outputs](https://img.shields.io/badge/Structured_outputs-3F3F46?style=for-the-badge) ![Citation verification](https://img.shields.io/badge/Citation_verification-3F3F46?style=for-the-badge) |
| **Retrieval & data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL_%2F_PGVector-1C1917?style=for-the-badge&logo=postgresql&logoColor=FDE68A) ![BigQuery](https://img.shields.io/badge/BigQuery-1C1917?style=for-the-badge&logo=googlebigquery&logoColor=FDE68A) ![Vertex AI Vector Search](https://img.shields.io/badge/Vertex_AI_Vector_Search-1C1917?style=for-the-badge&logo=googlecloud&logoColor=FDE68A) ![FAISS](https://img.shields.io/badge/FAISS-1C1917?style=for-the-badge) ![Neo4j](https://img.shields.io/badge/Neo4j-1C1917?style=for-the-badge&logo=neo4j&logoColor=FDE68A) ![Hybrid search](https://img.shields.io/badge/Hybrid_search_(HNSW_%2B_RRF)-3F3F46?style=for-the-badge) |
| **Evaluation** | ![LLM-as-judge](https://img.shields.io/badge/LLM--as--judge-3F3F46?style=for-the-badge) ![Benchmarking](https://img.shields.io/badge/Model_benchmarking-3F3F46?style=for-the-badge) ![LangSmith](https://img.shields.io/badge/LangSmith-1C1917?style=for-the-badge&logo=langchain&logoColor=FDE68A) |
| **Google Cloud** | ![Vertex AI](https://img.shields.io/badge/Vertex_AI-1C1917?style=for-the-badge&logo=googlecloud&logoColor=FDE68A) ![Gemini Enterprise](https://img.shields.io/badge/Gemini_Enterprise-1C1917?style=for-the-badge&logo=googlegemini&logoColor=FDE68A) ![Cloud Run](https://img.shields.io/badge/Cloud_Run-1C1917?style=for-the-badge&logo=googlecloud&logoColor=FDE68A) ![Cloud Functions](https://img.shields.io/badge/Cloud_Functions-1C1917?style=for-the-badge&logo=googlecloud&logoColor=FDE68A) ![Pub/Sub](https://img.shields.io/badge/Pub%2FSub-1C1917?style=for-the-badge&logo=googlepubsub&logoColor=FDE68A) |
| **Backend** | ![Python](https://img.shields.io/badge/Python-1C1917?style=for-the-badge&logo=python&logoColor=FDE68A) ![FastAPI](https://img.shields.io/badge/FastAPI-1C1917?style=for-the-badge&logo=fastapi&logoColor=FDE68A) ![SQL](https://img.shields.io/badge/SQL-1C1917?style=for-the-badge) ![Docker](https://img.shields.io/badge/Docker-1C1917?style=for-the-badge&logo=docker&logoColor=FDE68A) ![Streamlit](https://img.shields.io/badge/Streamlit-1C1917?style=for-the-badge&logo=streamlit&logoColor=FDE68A) ![CI/CD](https://img.shields.io/badge/CI%2FCD-1C1917?style=for-the-badge&logo=githubactions&logoColor=FDE68A) |

## Certified

[![Google Cloud Professional ML Engineer](https://img.shields.io/badge/Google_Cloud-Professional_ML_Engineer-1C1917?style=flat-square&logo=googlecloud&logoColor=FDE68A)](https://www.credly.com/badges/fc7321c1-5f35-4efa-bbdc-9a7fc50a396c/public_url)
[![Google Cloud Professional Data Engineer](https://img.shields.io/badge/Google_Cloud-Professional_Data_Engineer-1C1917?style=flat-square&logo=googlecloud&logoColor=FDE68A)](https://www.credly.com/badges/f01c5619-78fe-4579-b777-d2562682709d/public_url)
[![Gemini Enterprise Deployment](https://img.shields.io/badge/Partner_Specialist-Gemini_Enterprise_Deployment-1C1917?style=flat-square&logo=googlegemini&logoColor=FDE68A)](https://www.credly.com/badges/f5f99e6d-0f08-45de-b012-68b6bdfeef9e/public_url)
[![Gemini Enterprise Agent Development](https://img.shields.io/badge/Partner_Specialist-Gemini_Enterprise_Agent_Development-1C1917?style=flat-square&logo=googlegemini&logoColor=FDE68A)](https://www.credly.com/badges/9c00a470-a883-4dbb-b8cf-a7c9ab90938d/public_url)
[![Claude Certified Architect, Foundations](https://img.shields.io/badge/Anthropic-Claude_Certified_Architect_Foundations-1C1917?style=flat-square&logo=anthropic&logoColor=FDE68A)](https://www.credly.com/badges/3fbe6b0c-df1b-4581-9262-d668d5edcb5f/public_url)
