# Light-weight Semantic Mathlib Search — Demo

This repo hosts the Colab-ready notebook **“Light-Weight Semantic Mathlib Search DEMO.ipynb”**, a small, reproducible demo for *lightweight, LLM-free* semantic search over Lean’s mathlib.

- **Adapter & assets:** [Isaac74/qwen3-0.6b-lightweight-semantic-mathlib-search-adapter](https://huggingface.co/Isaac74/qwen3-0.6b-lightweight-semantic-mathlib-search-adapter)
- **Base encoder:** `Qwen/Qwen3-Embedding-0.6B` + LoRA (PEFT)
- **Data:** ~180k theorems via **LeanDojo** from **Lean 4.20.1** (minor gaps vs. full mathlib)
- **Index:** FAISS HNSW
- **Query types:** supports **natural language** and **formula** queries (can mix), **do not** supports LaTeX queries

> Part of AITP 2025 submission: [Towards Lightweight and LLM-Free Semantic Search for mathlib4](https://aitp-conference.org/2025/abstract/AITP_2025_paper_12.pdf)

## Quickstart (Colab)

1. Open **Google Colab**.
2. **Upload** the notebook: `Light-Weight Semantic Mathlib Search DEMO.ipynb`.
3. Click **Run all**. No extra setup is required, the notebook pulls the adapter and FAISS assets from the HF repo above.
4. On **Colab Free (CPU-only, low RAM)**, the demo uses **~7.2GB RAM** and delivers **~0.5s/query** interactive search latency.

## Examples

Below are a few queries you can paste into the demo to see what it finds.

🔎 `law of cosine`

🔎 `addition is commutative`

🔎 `triangle inequality` 

🔎 `the least factor of a number is a prime`

🔎 `w+q=q+w for rationals`

🔎 `o+-p=o-p`  

🔎 `i^2+j^2-2*i*j*cos` 

🔎 `∀ a b, gcd a b = gcd b a`  
