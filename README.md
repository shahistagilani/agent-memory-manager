# Agent Memory

**Memory-aware AI agents with Oracle AI Database, LangChain**

---

## Agent

**Research Paper Assistant** — an AI agent that searches, retrieves, and reasons over arxiv papers stored as vectors in Oracle AI Database. Also implemented a `MemoryManager` with six memory types, context engineering techniques that prevent context window overflow, and a turn-level agent harness — finishing with a before/after comparison that makes the impact of memory engineering visible.

## Topic Understanding

To understand the Agent Memory Architecture, Why we need it, How it works - Refer `notes-agent-memory.ipynb`

## File Structure

agent-memory/
├── .devcontainer/
│ ├── devcontainer.json Codespaces configuration
│ ├── docker-compose.yml Oracle AI Database + workshop container
│ ├── setup_build.sh Build-time dependency installation
│ ├── setup_runtime.sh Runtime Oracle health check and setup
│ ├── start_oracle.sh Oracle startup script
│ └── oracle-init/
│ └── 01_vector_memory.sql Vector memory schema init
├── src/
│ ├── agent-memory-setup-and-execution Working notebook to see agent memory in action
| ├── helper.py Utility Methods
│ ├── requirements.txt Dependencies to be installed
|
├── docs/ Guides containing howtos
│ ├── part-1-oracle-setup.md
│ ├── part-2-vector-search.md
│ ├── part-3-memory-engineering.md
│ ├── part-4-context-engineering.md
│ ├── part-5-web-search.md
│ ├── part-6-agent-execution.md
│ ├── TODO-checklist.md All 16 tasks at a glance
│ └── troubleshooting.md Common issues and solutions
├── images/ Screenshots and architecture diagrams
└── README.md

## Stack

- Oracle AI Database via `gvenzl/oracle-free`
- `langchain-oracledb` — LangChain integration for Oracle vector store
- `sentence-transformers` — local embedding model, no API key needed
- `openai` — OCI GenAI (xAI Grok 3 Fast) via OpenAI-compatible endpoint
- `tavily-python` — web search for agents
- `oracledb` — Python Oracle driver

## Source

- **[Agent Memory: Building Memory-Aware Agents](https://www.deeplearning.ai/short-courses/agent-memory-building-memory-aware-agents/)** — DeepLearning.AI short course for deeper exploration of agent memory patterns
- **[Oracle AI Developer Hub](https://github.com/oracle-devrel/oracle-ai-developer-hub)** — More technical assets, samples, and projects with Oracle AI
