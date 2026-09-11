# Hi, I'm Carlos Caicedo 👋

**Systems Engineering Student · Pontificia Universidad Javeriana · Bogotá, Colombia**

I build data pipelines, ML systems, and AI-powered solutions. Currently focused on large-scale data processing, NLP, and semantic search — with hands-on experience in distributed computing (Databricks/PySpark), workflow automation (n8n), LLM orchestration (LangChain), and cloud analytics (BigQuery).

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
![Claude](https://img.shields.io/badge/Claude_AI-000000?style=flat&logo=anthropic&logoColor=white)

**Automation & Backend**

![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker_Compose-2496ED?style=flat&logo=docker&logoColor=white)

**Databases**

![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=flat&logo=amazondynamodb&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat&logo=neo4j&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-7B61FF?style=flat)

**Data Science Tools**

![RStudio](https://img.shields.io/badge/RStudio-75AADB?style=flat&logo=rstudio&logoColor=white)

---

## 📌 Featured Projects

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
