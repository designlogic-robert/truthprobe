# TruthProbe v1.2 — Reasoning Transparency Layer for LLM Outputs

TruthProbe is a lightweight, portable reasoning-transparency module for LLMs.  
It evaluates any model-generated answer and attaches a **TruthTail** containing:

- Certainty level  
- Evidence strength  
- Bias risk  
- Detected assumptions  
- Topic risk  
- Fact vulnerability  
- Correction flag  

TruthProbe does **not** modify or rewrite the original answer.  
It evaluates only what the model already produced.

---

## 🔍 Why TruthProbe Exists

LLMs often sound confident even when they're guessing.  
TruthProbe reveals:
- when the model is unsure  
- when assumptions were made  
- when bias could influence the output  
- when the topic is known to be high-risk  
- when the answer may require correction  

This makes AI outputs **auditable, transparent, and safer to use**.

---

## 🧩 How TruthProbe Works

TruthProbe runs as a SynCE-compatible runtime mode:

1. The assistant gives its normal answer.  
2. TruthProbe analyzes that answer.  
3. TruthProbe attaches a structured, machine-readable **TruthTail**.  

TruthProbe never adds outside knowledge, only evaluates the answer produced.

---

## 📦 Repository Contents
```
truthprobe/
├── README.md
├── truthprobe-mode.laf
├── truthprobe-spec-v1.2.md
├── example-output.md
└── evaluation/
├── before-after.md
├── comparison-table.md
├── observed-notes.md
└── calibration-check.md

```
---

## 📘 Spec Document

The full public-stable specification is here:

➡ **truthprobe-spec-v1.2.md**

---

## 📝 Example Output

A full example of TruthProbe applied to a normal LLM response:

➡ **example-output.md**

---

## 🧪 Evaluation Suite

The `/evaluation/` folder contains:

- before/after comparisons  
- comparison table of behaviors  
- observed behavior notes  
- the full CalibrationCheck program  

Designed so developers can validate TruthProbe behavior in different models.

---

## 🔧 Integration

TruthProbe integrates cleanly into:

- SynCE Runtime (L5)  
- Tooling / prompt engines  
- Evaluation systems  
- Safety/audit workflows  

It requires no external APIs and introduces no hallucination risk.

---

## 📄 License

MIT.

