# Lightweight Semantic Mathlib Search — Demo (Notebook)

This repo hosts the Colab-ready notebook **“Light-Weight Semantic Mathlib Search DEMO (Hugging Face).ipynb”**, a small, reproducible demo for *lightweight, LLM-free* semantic search over Lean’s mathlib.

- **Adapter & assets:** `Isaac74/qwen3-0.6b-lightweight-semantic-mathlib-search-adapter` (Hugging Face model repo)
- **Base encoder:** `Qwen/Qwen3-Embedding-0.6B` + LoRA (PEFT)
- **Data:** ~180k theorems via **LeanDojo** from **Lean 4.20.1** (minor gaps vs. full mathlib)
- **Index:** FAISS HNSW
- **Query types:** supports **natural language** and **formula** queries (can mix), **not** LaTeX-aware (LaTeX won’t match)

> Part of AITP 2025 submission: *“Towards Lightweight and LLM-Free Semantic Search for mathlib4.”*

## Quickstart (Colab)

1. Open **Google Colab**.
2. **Upload** the notebook: `Light-Weight Semantic Mathlib Search DEMO (Hugging Face).ipynb`.
3. Click **Run all**. No extra setup is required, the notebook pulls the adapter and FAISS assets from the HF repo above.
4. On **Colab Free (CPU-only, low RAM)**, the demo delivers **~0.5s/query** interactive search latency.
