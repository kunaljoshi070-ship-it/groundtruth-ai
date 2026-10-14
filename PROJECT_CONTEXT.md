# GroundTruth AI — Project Context

## Goal
Build and evaluate a Retrieval-Augmented Generation (RAG) system that answers questions from a fixed collection of documents, cites supporting passages, and abstains when evidence is insufficient.

## Research question
How do retrieval strategy and reranking affect retrieval quality, answer correctness, citation support, and unsupported answers under a fixed evaluation set and budget?

## Hypotheses (to test, not assume)
1. Hybrid keyword + semantic retrieval may outperform either alone.
2. Reranking may improve the evidence passed to the generator.
3. An abstention policy may reduce unsupported answers while lowering answer coverage.

## MVP
- Choose a small, legally usable document collection.
- Create 50–100 manually verified questions, including questions not answerable from the documents.
- Record gold answers and supporting passages for answerable questions.
- Implement BM25/keyword retrieval first, then semantic and hybrid retrieval; add reranking only after baselines work.
- Generate answers with traceable citations or explicit abstention.
- Build the evaluation pipeline before spending time on a UI.

## Metrics
- Retrieval: Recall@K, Mean Reciprocal Rank (MRR).
- Answers: correctness and citation/evidence support.
- Reliability: unsupported-answer rate, abstention accuracy, answer coverage.
- Engineering: latency and estimated cost where measurable.

## Initial stack
Python, pandas, pytest, BM25, sentence-transformers, and a reproducible evaluation script. Keep the LLM provider behind a simple interface. Add a vector database or Streamlit only when justified.

## Research/data rules
- Verify data licenses and cite sources in `docs/research-notes.md`.
- Never commit secrets, private documents, or large raw datasets.
- Prevent leakage between evaluation questions/labels and tuning.
- Distinguish automatic metrics from human-verified judgments.
- Never invent results; record failures and limitations.

## First milestone acceptance criteria
1. Dataset and license decision documented.
2. Evaluation set schema and annotation rules documented.
3. Baseline retrieval runs reproducibly.
4. Results are written to CSV with configuration metadata.
5. At least five failure cases are documented.
