# Hi, I'm Carlos Caicedo 👋

**Systems Engineering Student · Pontificia Universidad Javeriana · Bogotá, Colombia**

I build data pipelines, ML systems, and AI-powered solutions. Currently focused on large-scale data processing, NLP, and semantic search — with hands-on experience in distributed computing (Databricks/PySpark), workflow automation (n8n), LLM orchestration (LangChain), and cloud architecture & analytics (AWS/BigQuery).

---

## 🛠 Tech Stack

**Data & AI**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Spark MLlib](https://img.shields.io/badge/Spark_MLlib-FDEE21?style=flat&logo=apachespark&logoColor=black)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)

**NLP, Semantic Search & LLM Orchestration**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Sentence Transformers](https://img.shields.io/badge/Sentence_Transformers-412991?style=flat)
![Vector DB](https://img.shields.io/badge/Vector_Database-00B4D8?style=flat)
![Cohere](https://img.shields.io/badge/Cohere-39594C?style=flat&logo=cohere&logoColor=white)
![Claude](https://img.shields.io/badge/Claude_AI-000000?style=flat&logo=anthropic&logoColor=white)

**Cloud & Infrastructure**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![AWS Lambda](https://img.shields.io/badge/AWS_Lambda-FF9900?style=flat&logo=awslambda&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon_S3-569A31?style=flat&logo=amazons3&logoColor=white)
![Amazon API Gateway](https://img.shields.io/badge/API_Gateway-FF4F8B?style=flat&logo=amazonapigateway&logoColor=white)
![Amazon RDS](https://img.shields.io/badge/Amazon_RDS-527FFF?style=flat&logo=amazonrds&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat&logo=render&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)

**Automation & Backend**

![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker_Compose-2496ED?style=flat&logo=docker&logoColor=white)

**Databases**

![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=flat&logo=amazondynamodb&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat&logo=neo4j&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-7B61FF?style=flat)

**Data Science Tools**

![RStudio](https://img.shields.io/badge/RStudio-75AADB?style=flat&logo=rstudio&logoColor=white)

---

## 📌 Featured Projects

### 🌐 [Interactive AI Portfolio & Serverless RAG Laboratory](https://carloscaicedo.vercel.app/)
**Next.js · AWS Serverless · n8n · PostgreSQL/pgvector · Groq & Cohere**

An interactive personal portfolio built as an "AI / Data laboratory." Instead of reading a static resume, visitors explore my technical profile and project details by chatting directly with an AI assistant powered by a 100% serverless RAG pipeline.

- **Links:** [Live Web App](https://carloscaicedo.vercel.app/) · [Frontend Repository](https://github.com/00CARLOSECG00/carloscaicedo-portfolio) · [Backend Repository](https://github.com/00CARLOSECG00/carloscaicedo-portafolio-back)
- **Frontend (Vercel):** Next.js (App Router) + TypeScript app that sends user queries to an n8n webhook and renders Markdown responses — including dynamic tables and links — 
- **Content backend (Render):** REST API backed by a Supabase database for profile, project, experience, and education data
- **Orchestration (n8n):** acts as an event-driven middleware/API gateway between the frontend and AWS, routing requests, keeping API keys isolated, and enabling rapid iteration
- **Serverless RAG engine (AWS):** an API Gateway triggers a Lambda function that embeds the incoming question (via Cohere) and performs a cosine-distance similarity search in an AWS RDS PostgreSQL database using `pgvector`
- **Generative AI:** retrieved context and the question are sent to Groq (`openai/gpt-oss-120b`) for near-instantaneous, high-quality Markdown response generation
- **Event-driven ingestion:** dropping a new PDF into an AWS S3 bucket automatically triggers a Python Lambda (`procesador-documentos-rag`) that extracts text with `pypdf`, applies chunking, and stores 1024-dimensional vectors generated with Cohere's `embed-multilingual-v3.0`

> `Next.js` · `TypeScript` · `Vercel` · `Render` · `Supabase` · `n8n` · `AWS Lambda` · `Amazon S3` · `API Gateway` · `RDS/pgvector` · `Cohere API` · `Groq API` · `Serverless Architecture`

---

### 🎯 [Job Offer Scraper](https://github.com/00CARLOSECG00/Job-offer-scraper)
**n8n · Groq API · Google Sheets API · Gmail API**

End-to-end n8n automation that discovers junior/entry-level job openings, filters them against a profile and preferences stored in Google Sheets, scores each one with an LLM, and emails a curated report — the same system that powers the job-search tables built earlier in this profile.

- **Multi-source scraping:** queries Remotive, Jobicy, The Muse, and Get on Board in parallel, then normalizes all four into one schema
- **Rule-based filtering:** rejects unwanted locations, rejected role titles (e.g. *senior*, *lead*), and rejected keywords, requiring desired roles to appear in the job title before any LLM call is spent
- **LLM evaluation (Groq):** sends each of up to 40 qualifying offers to `openai/gpt-oss-120b` for a structured fit score, summary, and matched/missing skills, rate-limited to 1 request/10s with retries
- **Gap-skills tracking:** logs missing skills detected across runs to a `Gap_Skills` sheet, with a secondary workflow that consolidates and ranks them by frequency
- **Automated reporting:** filters offers marked `aplica = true` and emails a formatted report via Gmail, running 4×/week on a schedule

> `n8n` · `Groq API` · `LLM Evaluation` · `Google Sheets API` · `Gmail API` · `Workflow Automation` · `JSON Parsing`

---

### 💸 [WhatsApp AI Financial Tracker](https://github.com/00CARLOSECG00/WhatsApp-Expense-Income-Tracker)
**Node.js · n8n · Groq API (Qwen) · MongoDB Atlas · Google Sheets API**

Event-driven microservices system that lets users log personal expenses and income by simply messaging in natural language over WhatsApp. Messages are captured in real time, orchestrated through n8n, parsed by an LLM into structured JSON, and written automatically to Google Sheets.

- **Backend (Node.js + Baileys):** real-time WhatsApp client hosted on Render, with session persistence in MongoDB Atlas to avoid re-scanning QR codes
- **Orchestration (n8n):** webhook-driven workflow that calls the LLM and routes the structured output downstream
- **AI Processing (Groq API + Qwen):** extracts amount, description, and transaction type from free-text messages, enforcing strict JSON output via prompt engineering
- **Storage (Google Sheets API):** appends each transaction as a new row instantly, with timestamps localized via Luxon

> `Node.js` · `n8n` · `Groq API` · `MongoDB Atlas` · `Baileys` · `Google Sheets API` · `Prompt Engineering`

---

### 📄 [AI Document Intelligence Platform](https://github.com/00CARLOSECG00/AI-Document-Intelligence-Platform)
**Python · FastAPI · LangChain · PostgreSQL/pgvector · n8n**

RAG platform for extracting, processing, and querying information from complex PDF documents, supporting both real-time chat-style queries through a web interface and unattended background processing via n8n.

- **Ingestion (RAG):** PDF processing with LangChain-based dynamic chunking and embedding generation
- **Vector storage:** PostgreSQL with `pgvector` for high-speed semantic similarity search
- **Decoupled architecture:** centralized FastAPI backend exposing `/api/v1/upload` and `/api/v1/ask` endpoints, serving both the web frontend and automated workflows
- **High-speed inference:** Qwen 27B via Groq for low-latency LLM responses
- **Automation layer (n8n):** watches folders/inboxes, ingests PDFs automatically, and extracts structured data into tools like Google Sheets without human intervention

> `Python` · `FastAPI` · `LangChain` · `pgvector` · `PostgreSQL` · `n8n` · `Docker`

---

### 🔬 [Saber 11 Results Analysis — Large-Scale Data Processing](https://github.com/Sparktanos/Proyecto-Pruebas-Saber-11)
**PySpark · Databricks · Python · Medallion Architecture · 7M+ records**

End-to-end data engineering project analyzing the factors that drive academic performance gaps across Colombian municipalities (2015–2023). Built as part of the *Large-Scale Data Processing* course at Universidad Javeriana.

- Integrated **6 public datasets** (7.1M+ student records from ICFES, MEN, DANE, UNIDOS)
- Implemented a **Bronze → Silver medallion architecture** on Databricks
- Built modular PySpark pipelines for each data source with quality reports: null counts, duplicate detection, type correction, and longitudinal imputation

> `Databricks` · `PySpark` · `pandas` · `matplotlib` · `Medallion Architecture` · `Data Quality`

---

### 🧠 RAG - Semantic Search Pipeline — [SEKIA Research Group](https://github.com/00CARLOSECG00/SEKIA)
**Python · Sentence Transformers · Vector Database · NLP · GROQ API**

Prototype RAG system developed within the SEKIA university research group to explore semantic question answering over Colombian electoral proposal documents.

The system processes PDF documents, applies NLP-based chunking to split text into coherent segments, and encodes them into embeddings. These embeddings are stored in a vector database to enable semantic retrieval based on cosine similarity rather than keyword matching.

Retrieved passages are then passed to the Groq API, which generates structured responses by summarizing the relevant context and evaluating proposals using SMART criteria (Specific, Measurable, Achievable, Relevant, Time-bound).

> `Python` · `sentence-transformers` · `vector database` · `RAG` · `semantic search` · `GROQ`

---

### 🏆 [SabanaHack 2025 — Hackathon](https://github.com/00CARLOSECG00/404-Not-Found-Sleep-)
**Python · Problem Solving · Collaborative Development**

Participated in SabanaHack 2025, a competitive hackathon hosted by Universidad de La Sabana. Contributed to a Python-based solution under time pressure, collaborating with a cross-functional team to design, prototype, and present a working solution.

- Applied structured problem-solving under a tight 24-hour constraint
- Worked in a multi-team repository environment with version control coordination

> `Python` · `Hackathon` · `Rapid Prototyping` · `Collaborative Development`

---

## 📫 Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/00carlos-caicedo00/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:carloscaicedog2008.cc@gmail.com)
[![Location](https://img.shields.io/badge/Bogotá,_Colombia-4CAF50?style=flat&logo=googlemaps&logoColor=white)](#)
