<!-- ============================== HEADER ============================== -->
<p align="center">
  <img src="assets/header.svg" alt="Rishikesh Ombase · Agentic AI Architect" width="100%">
</p>

<p align="center">
  <a href="https://github.com/Rishikesh32">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=21&duration=2800&pause=900&color=22D3EE&center=true&vCenter=true&width=720&lines=Designing+multi-agent+systems+with+LangGraph+%2B+MCP;Agentic+RAG+%C2%B7+GraphRAG+%C2%B7+long-term+agent+memory;Evals%2C+guardrails+and+tracing+by+default;Humans+approve+anything+irreversible;6%2B+years+in+AI+%26+ML+%C2%B7+Kolhapur%2C+India" alt="Typing animation: what I build">
  </a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/rishikesh-ombase-11989b1ab/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:rishikeshombase4@gmail.com"><img src="https://img.shields.io/badge/Email-8B5CF6?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://rishikesh32.github.io"><img src="https://img.shields.io/badge/Portfolio-22D3EE?style=for-the-badge&logo=googlechrome&logoColor=04050d" alt="Portfolio"></a>
  <img src="https://komarev.com/ghpvc/?username=Rishikesh32&style=for-the-badge&color=f472b6&label=PROFILE+VIEWS" alt="Profile views">
</p>

---

## 🧠 `whoami`

```python
class Rishikesh(AgenticAIArchitect):
    location        = "Kolhapur, India 🇮🇳"
    experience      = "6+ years in AI & ML · Senior Data Scientist"
    focus           = ["multi-agent systems", "MCP tool layers", "agentic RAG", "LLMOps"]
    currently       = "building AlphaDesk, a multi-agent quant research platform, in public"
    learning        = ["A2A protocol", "agent memory architectures", "eval-driven development"]
    collaborate_on  = ["open-source MCP servers", "agent evaluation tooling", "AI for finance"]
    ask_me_about    = ["LangGraph supervisors", "GraphRAG", "model routing", "guardrails"]
    open_to         = "AI Architect roles 🚀"

    def principles(self):
        return [
            "Workflows before agents",
            "Evals are the spec",
            "Tools through MCP",
            "Humans on the irreversible",
            "Route for cost",
        ]
```

---

## 🛰️ Flagship · AlphaDesk <sub><img src="https://img.shields.io/badge/status-building_in_public-f472b6?style=flat-square" alt="Status: building in public"></sub>

<p align="center">
  <img src="assets/alphadesk-flow.svg" alt="AlphaDesk agent flow: supervisor agent delegates to market data, research, quant and risk agents, then a report goes to human approval" width="100%">
</p>

A **multi-agent quant research platform**. A LangGraph supervisor breaks a research question into tasks and delegates to specialists:

| Agent | Job | Built with |
|---|---|---|
| 📈 **Market data** | Pulls prices and fundamentals | MCP servers |
| 📚 **Research** | Reasons over filings and news | GraphRAG · Qdrant · Neo4j |
| 🧮 **Quant** | Writes and runs forecasting and backtest code | Sandboxed code execution |
| 🛡️ **Risk** | Checks exposure and limits | Policy rules + LLM critic |
| ✋ **Human** | Approves before any signal leaves the system | Human-in-the-loop interrupt |

> Frontier models plan, small open-weight models extract. Every run is traced in Langfuse and scored by an eval suite before a release ships.

---

## 🏗️ Agentic architectures

Each one started as a classic ML or automation build that I've redesigned for the agentic era.

| Project | Pattern | Stack | Evolved from |
|---|---|---|---|
| 🛰️ **AlphaDesk** | Hierarchical supervisor | LangGraph · MCP · GraphRAG · Langfuse | Quant stock prediction |
| 🏠 **ListingStudio** | Classify → generate → critique | Vision LLM · LangGraph · batch generation at scale | Real-estate content engine |
| 🧾 **InvoiceOps** | Extract → act + human review | Vision LLM · computer use · Pydantic | Invoice automation (OCR) |
| 📑 **FundDocs Studio** | Multi-agent document pipeline | Vision-language models · LLM agents · style-guide RAG | Mutual fund pipeline |
| 🛸 **SkyWatch** | Perceive → reason → act | YOLO · Qwen-VL · vLLM | Drone recognition (OpenCV) |
| 🎬 **CineMind** | Cluster → rank → serve | User embeddings · clustering · Redis · FastAPI | OTT recommendation backend |
| 🔐 **MCP Gateway** | Secure tool gateway | MCP · OAuth · RBAC · OpenTelemetry | Data integration |

<details>
<summary><b>🔎 Project details (click to expand)</b></summary>
<br>

**📑 FundDocs Studio.** Prospectuses, summary prospectuses and SAI documents go in alongside the client's style guide. Vision-language models read the layout of every page, a style-guide agent decides which rule applies to each heading, table and footnote, and LLM agents apply the formatting and verify it against the guide before a person signs off.

**🎬 CineMind.** The recommendation backend for an OTT platform:
- Watch events become user embeddings, clustered into taste groups so viewers with similar habits are shown similar films
- Candidates come from the viewer's cluster plus item similarity, then a ranker personalises the list
- Redis serves precomputed recommendations, sessions and trending lists for fast reads
- FastAPI microservices on PostgreSQL, packaged with Docker, with a conversational agent that explains each pick

**🏠 ListingStudio.** It goes beyond tagging photos. Vision models classify every image by room and feature, then LLM agents generate the rest of each listing at scale: the view and surroundings, amenities, neighbourhood details and the full description. A critic agent checks every claim before publishing.

</details>

<details>
<summary><b>📐 My reference architecture (click to expand)</b></summary>
<br>

```text
 ┌──────────────┐  ┌──────────────────────────────────────────────────┐  ┌──────────────┐
 │  SECURITY &  │  │ Interfaces      chat · API · Slack/Teams · voice │  │ OBSERVABILITY│
 │  GOVERNANCE  │  │ Guardrails      input validation · policy · out  │  │   & EVALS    │
 │              │  │ Orchestration   supervisor · LangGraph · ✋ HITL │  │              │
 │ identity/RBAC│  │ Specialists     planner · researcher · critic    │  │ Langfuse     │
 │ PII redaction│  │ Tools via MCP   APIs · DBs · browser · sandbox   │  │ eval suites  │
 │ injection def│  │ Knowledge       vector + graph RAG · memory      │  │ cost budgets │
 │ audit trail  │  │ Model gateway   routing · frontier · vLLM · cache│  │ drift alerts │
 └──────────────┘  └──────────────────────────────────────────────────┘  └──────────────┘
```

</details>

---

## 🧰 Tech stack

**Agents & orchestration**

![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-8B5CF6?style=for-the-badge&logo=anthropic&logoColor=white)
![A2A](https://img.shields.io/badge/A2A_Protocol-4285F4?style=for-the-badge&logo=google&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-FF5A50?style=for-the-badge&logoColor=white)
![OpenAI Agents SDK](https://img.shields.io/badge/OpenAI_Agents_SDK-412991?style=for-the-badge&logoColor=white)
![Claude Agent SDK](https://img.shields.io/badge/Claude_Agent_SDK-D97757?style=for-the-badge&logo=anthropic&logoColor=white)

**Models**

![Claude](https://img.shields.io/badge/Claude-191919?style=for-the-badge&logo=anthropic&logoColor=white)
![GPT](https://img.shields.io/badge/GPT-10A37F?style=for-the-badge&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![Llama](https://img.shields.io/badge/Llama-0467DF?style=for-the-badge&logo=meta&logoColor=white)
![Qwen](https://img.shields.io/badge/Qwen-615CED?style=for-the-badge&logoColor=white)
![DeepSeek](https://img.shields.io/badge/DeepSeek-4D6BFE?style=for-the-badge&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

**Knowledge & memory**

![LlamaIndex](https://img.shields.io/badge/LlamaIndex-6E44FF?style=for-the-badge&logoColor=white)
![GraphRAG](https://img.shields.io/badge/GraphRAG-22D3EE?style=for-the-badge&logoColor=04050d)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=for-the-badge&logo=neo4j&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge&logo=qdrant&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

**LLMOps & governance**

![Langfuse](https://img.shields.io/badge/Langfuse-0A0A0A?style=for-the-badge&logoColor=white)
![LangSmith](https://img.shields.io/badge/LangSmith-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![Ragas](https://img.shields.io/badge/Ragas-F472B6?style=for-the-badge&logoColor=white)
![DeepEval](https://img.shields.io/badge/DeepEval-8B5CF6?style=for-the-badge&logoColor=white)
![Guardrails](https://img.shields.io/badge/Guardrails-34D399?style=for-the-badge&logoColor=04050d)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=for-the-badge&logo=opentelemetry&logoColor=white)

**Platform & cloud**

<p>
  <img src="https://skillicons.dev/icons?i=py,fastapi,docker,kubernetes,aws,azure,gcp,pytorch,postgres,redis,linux,git,github&theme=dark" alt="Python, FastAPI, Docker, Kubernetes, AWS, Azure, GCP, PyTorch, Postgres, Redis, Linux, Git, GitHub">
</p>

![vLLM](https://img.shields.io/badge/vLLM-30A2FF?style=for-the-badge&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white)
![AWS Bedrock](https://img.shields.io/badge/AWS_Bedrock-FF9900?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Vertex AI](https://img.shields.io/badge/Vertex_AI-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Azure AI Foundry](https://img.shields.io/badge/Azure_AI_Foundry-0078D4?style=for-the-badge&logoColor=white)

---

## 💼 Experience

| When | Role | Where |
|---|---|---|
| **Dec 2023 — now** | Senior Data Scientist: LLM-integrated API services and GenAI modules for financial reports | AIT Global India |
| **Jul 2023 — Oct 2023** | AI Data Specialist: real-time data for pricing models | Futurense Technologies |
| **Jul 2022 — Mar 2023** | Software Engineer: systems for large-scale trading data | Systech Solutions |
| **Jan 2020 — Mar 2022** | Data Scientist: stock-movement models and alpha signals | Varilligence Technologies |

🎓 M.Sc. Computer Science, Shivaji University · 🏆 Best Performer of the Month · Spot Award · GOM Award

---

## 📊 GitHub activity

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=Rishikesh32&show_icons=true&hide_border=true&bg_color=04050d&title_color=22d3ee&icon_color=8b5cf6&text_color=c9cbe8&ring_color=f472b6&count_private=true" alt="GitHub stats">
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Rishikesh32&layout=compact&hide_border=true&bg_color=04050d&title_color=22d3ee&text_color=c9cbe8&langs_count=6" alt="Top languages">
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=Rishikesh32&hide_border=true&background=04050d&ring=8B5CF6&fire=F472B6&currStreakLabel=22D3EE&sideLabels=C9CBE8&currStreakNum=EEF0FF&sideNums=EEF0FF&dates=5F6489&stroke=1F2440" alt="GitHub streak" width="80%">
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Rishikesh32&bg_color=04050d&color=c9cbe8&line=8b5cf6&point=22d3ee&area=true&area_color=8b5cf6&hide_border=true" alt="Contribution activity graph" width="100%">
</p>

<!-- Snake animation: generated daily by .github/workflows/snake.yml -->
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Rishikesh32/Rishikesh32/output/github-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Rishikesh32/Rishikesh32/output/github-snake.svg">
    <img alt="Snake eating my contribution graph" src="https://raw.githubusercontent.com/Rishikesh32/Rishikesh32/output/github-snake-dark.svg">
  </picture>
</p>

---

<p align="center">
  <b>Building something agentic? Let's talk.</b><br>
  <a href="mailto:rishikeshombase4@gmail.com">rishikeshombase4@gmail.com</a> ·
  <a href="https://www.linkedin.com/in/rishikesh-ombase-11989b1ab/">LinkedIn</a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:22d3ee,50:8b5cf6,100:f472b6&height=120&section=footer" alt="" width="100%">
</p>
