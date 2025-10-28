A minimal, easy-to-run demo that implements the core idea from **A-MEM: Agentic Memory for LLM Agents (2025)** — a memory-augmented chat agent that stores past interactions as embeddings and retrieves the most relevant memories at each turn.

This repo is intentionally small so you can fork it, run it locally, and include it with your internship application.

## What it demonstrates
- Storing conversational turns (user query + agent response) in a local JSON memory store.
- Creating embeddings for each memory entry (using OpenAI Embeddings API).
- Retrieving top-k relevant memories via cosine similarity.
- Prepending retrieved memories to an LLM prompt so the agent answers with context.

## Files
- `memory_agent_demo.py` — runnable demo script (interactive CLI)
- `requirements.txt` — Python dependencies
- `README.md` — this file

## Setup
1. Clone/fork this repo to your GitHub.
2. Create a virtual environment and install dependencies:

```bash
python -m venv venv
source venv/bin/activate # macOS/Linux
venv\Scripts\activate # Windows
pip install -r requirements.txt
```

3. Set your OpenAI API key as an environment variable:

```bash
export OPENAI_API_KEY="sk-..."
# Windows (PowerShell): $env:OPENAI_API_KEY = "sk-..."
```

4. Run the demo:

```bash
python memory_agent_demo.py
```

## Notes
- The script uses the OpenAI embeddings API to produce vectors. If you prefer, switch to a local sentence-transformer model by changing the `embed_text()` function.
- This is a minimal proof-of-concept — it is **not** production-ready. It focuses on clarity and reproducibility for a quick internship assignment.

## Paper Reference
- Xu et al., "A-MEM: Agentic Memory for LLM Agents" (2025). arXiv:2502.12110

---