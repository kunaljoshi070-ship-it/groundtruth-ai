# Start Here

## 1. Create the repository
Create a GitHub repository named `GroundTruth-AI` (or `groundtruth-ai`), extract this folder, and push the files. Keep the repository public only if you are comfortable publishing all its contents.

## 2. Configure the tools
- **ChatGPT Project:** create `GroundTruth AI`; upload `PROJECT_CONTEXT.md`; paste `CHATGPT_INSTRUCTIONS.txt` into project instructions.
- **Codex:** open the repository folder in Codex. Keep `AGENTS.md` at the repository root; Codex can use it as project guidance. Ask it to inspect the repo and propose Milestone 1 only.
- **Claude Project:** create `GroundTruth AI`; add `PROJECT_CONTEXT.md` to project knowledge; paste `CLAUDE_INSTRUCTIONS.txt` into project instructions.
- Keep all three aligned by updating `PROJECT_CONTEXT.md` when a decision changes.

## 3. First task
Ask ChatGPT to propose 2–3 candidate document collections and verify source/license. Ask Claude to critique the dataset and evaluation plan. Decide on one collection and document the decision. Then ask Codex to scaffold only the data schema, annotation guidelines, and tests—do not implement the full RAG pipeline yet.

## 4. Suggested first GitHub issues
1. Select and document a licensed document collection.
2. Define JSONL schema for questions, gold answers, and evidence spans.
3. Write annotation guidelines, including unanswerable questions.
4. Implement a tiny BM25 baseline and unit tests.
5. Add Recall@K/MRR evaluation and CSV output.

## 5. Gemini 4 Argon
Optional, not required. Use it for a second opinion on a difficult design or bug, not as a fourth parallel implementer. Verify advice and test it before accepting.
