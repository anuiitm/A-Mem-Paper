A minimal, easy-to-run demo that implements the core idea from **A-MEM: Agentic Memory for LLM Agents (2025)** - a memory-augmented chat agent that stores past interactions as embeddings and retrieves the most relevant memories at each turn.

## What it demonstrates
- Storing conversational turns (user query + agent response) in a local JSON memory store.
- Creating embeddings for each memory entry.
- Retrieving top-k relevant memories via cosine similarity.
- Prepending retrieved memories to an LLM prompt so the agent answers with context.

## Files
- `memory_agent.ipynb` — runnable demo notebook
- `README.md` — this file

## Setup
1. Clone/fork this repo to your GitHub.
2. Install the libraries in the code, if not available
3. Set your OpenAI/DeepSeek or any API key as an environment variable (.env file):
```bash
DEEPSEEK_API_KEY="sk-..."
```
4. Run the notebook:


## Note
- This is a minimal proof-of-concept - it is **not** production-ready.

## Paper Reference
- Xu et al., "A-MEM: Agentic Memory for LLM Agents" (2025). arXiv:2502.12110 [https://arxiv.org/pdf/2502.12110v10] 

---
