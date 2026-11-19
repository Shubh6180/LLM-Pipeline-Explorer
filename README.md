# Neural Text & Vector Workbench

An interactive, zero-dependency educational tool demonstrating how raw text is broken into subword tokens and projected into 3D semantic space. Runs 100% client-side in the browser.

## 🌐 Live Demo

- **Production App:** [https://llm-weld-sigma.vercel.app](https://llm-weld-sigma.vercel.app)
- **Invariant Self-Test Mode:** [https://llm-weld-sigma.vercel.app/?selftest=true](https://llm-weld-sigma.vercel.app/?selftest=true)

---

## Features

- **Subword Tokenizer Lab:**
  - Deterministic WordPiece-style greedy tokenization
  - Dynamic vocabulary truncation slider (demonstrating how dropping whole words fractures them into `##` continuation subwords)
  - Real-time token badges, compression ratio telemetry, and sticky-header vocabulary inspector table
- **3D Semantic Vector Space:**
  - 64-dimensional deterministic feature hashing (FNV-1a) with character 3-grams and subword weighting
  - Corpus-wide Inverse Document Frequency (IDF) weighting and unit $L_2$ normalization
  - Exact Dual PCA eigensolver using cyclic Jacobi rotations
  - Dual 3D renderer: Interactive Plotly.js WebGL scatter plot with automatic fallback to custom vanilla HTML5 Canvas 2D perspective engine
  - Live query sandbox ("Probe the Vector Space") projecting novel sequences into the exact same 3D coordinate space with 3-step breakdown
- **Invariant Self-Test Mode:**
  - Run with `?selftest=true` to verify all mathematical and algorithmic invariants in real time.

## Deployment

Deployable as a static single-page application on Vercel, GitHub Pages, or any static host.
