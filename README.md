# GroundTruth AI

**An evaluation framework for measuring factual accuracy, evidence grounding, and unsupported answers in retrieval-augmented generation (RAG) systems.**

> Status: planning. No performance claims have been made.

## Start here
1. Read `PROJECT_CONTEXT.md`.
2. Follow `docs/START_HERE.md`.
3. Create a legally usable document collection and a small verified question set before implementing advanced methods.
4. Establish a keyword retrieval baseline, then compare semantic, hybrid, and (later) reranked retrieval.

## Repository layout
```text
GroundTruth-AI/
├── PROJECT_CONTEXT.md
├── AGENTS.md                  # instructions for Codex and coding agents
├── CHATGPT_INSTRUCTIONS.txt
├── CLAUDE_INSTRUCTIONS.txt
├── docs/                      # research notes, data card, protocol
├── data/                      # keep raw/private datasets out of Git
├── src/                       # ingestion, retrieval, generation, evaluation
├── tests/
├── experiments/               # configs and results
└── app/                       # optional demo after evaluation works
```

## Principles
- Same evaluation set and protocol across comparisons.
- Reproducible runs, honest reporting, documented failure cases.
- AI-generated code must be tested and understood before merging.
- Keep API keys and private data out of Git.
