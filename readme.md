# 🔍 Developer Tools Research Agent

An intelligent command-line agent that takes a developer's query (like "best models of Claude" or "top Groq alternatives") and delivers a **researched, structured recommendation** of developer tools with pricing, open-source status, tech stack, API availability, and more — powered by LLMs, Firecrawl, and LangGraph.

---

## 🚀 Features

- 🔎 **Tool Extraction** from live web content using Firecrawl
- 🧠 **Structured Company Analysis** powered by LangChain + LLMs
- 🧵 **Stateful LangGraph Workflow**: Extract → Research → Analyze
- 🗣️ Natural language interface for developers
- 📝 Recommendations with developer-focused summaries
- ✅ Supports multiple LLM backends (OpenAI, Groq)

---

## 🧠 How It Works

1. Takes a natural query like: `Tell me best models of Groq`
2. Uses Firecrawl to find relevant articles
3. Extracts developer tools from the scraped data
4. Finds official websites of each tool
5. Analyzes tool capabilities (tech stack, pricing, API, etc.)
6. Generates a concise recommendation using LLMs

---

## 🏗️ Folder Structure

AI_Researcher/
│
├── main.py # CLI entry point
├── .env # Environment variables (ignored)
└── src/
├── firecrawl.py # Firecrawl web search + scrape service
├── models.py # Pydantic models (State, CompanyInfo, etc.)
├── prompts.py # Carefully engineered prompt templates
└── workflows.py # LangGraph workflow logic


## 🔧 Setup & Installation

```bash
git clone https://github.com/DakshC17/AI_Researcher.git
cd AI_Researcher
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt



Create a .env file:

GROQ_API_KEY=your_groq_api_key
FIRECRAWL_API_KEY=your_firecrawl_api_key




Developer Tools Research Agent

🔍 Developer Tools Query: best vector database
...
📊 Results for: best vector database
============================================================

1. 🏢 Weaviate
   🌐 Website: https://weaviate.io
   💰 Pricing: Freemium
   📖 Open Source: True
   🛠️  Tech Stack: Python, REST API, Docker
   🔌 API: ✅ Available
   📝 Description: Weaviate is a developer-friendly vector database for semantic search with GraphQL and REST support.

Developer Recommendations:
----------------------------------------
I recommend Weaviate for most teams due to its open-source nature, active development, and built-in semantic search capabilities.



⚙️ Requirements

    Python 3.9+

    langchain

    langgraph

    firecrawl

    dotenv

    Compatible LLM provider (Groq, OpenAI, etc.)


    

