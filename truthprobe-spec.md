# TruthProbe — AI Safety Layer v1.0
## Specification Document  
Author: Robert Hansen (Design Logic)  
Updated: Nov 14, 2025

---

## 1. Overview
TruthProbe is a lightweight epistemic-safety layer for AI assistants.  
It does not alter the *content* of responses — instead, it reveals what the model is doing internally:

- How confident the model is
- Whether the answer relies on strong evidence or weak inference
- Whether bias or stylistic drift is influencing the output
- Whether the AI is guessing, extrapolating, or uncertain

TruthProbe attaches a short “Truth Tail” to every response, helping users decide when to trust the output and when to double-check.

This solves the universal AI problem:
> “I can’t tell when the AI is confident or just making something up.”

---

## 2. Design Goals
1. **Simplicity** — install by copy/paste, no technical setup.
2. **Portability** — works on ChatGPT, Claude, Bard, and any LLM with system instructions.
3. **Transparency** — reveal hidden model states in a human-friendly way.
4. **Zero interference** — TruthProbe never overrides or censors content; it only adds metadata.
5. **Fail-gracefully** — if the model cannot assess a dimension, it declares uncertainty instead of hiding it.

---

## 3. Signal Model  
TruthProbe outputs four primary signals:

### 3.1 Confidence Level  
Model self-assessment of correctness.  
Values:
- **High**
- **Medium**
- **Low**
- **Speculative**

Derived from:
- semantic certainty  
- existence of known facts  
- clarity of the prompt  
- latent hesitation indicators

---

### 3.2 Evidence Strength  
How much the answer depends on:
- verified facts  
- known patterns  
- extrapolation  
- pure inference  

Values:
- **Strong Evidence**
- **Moderate Evidence**
- **Weak Evidence**
- **No Evidence (Inference)**

---

### 3.3 Bias Risk  
Detects whether stylistic or ideological drift may have influenced the output.

Values:
- **Low Bias**
- **Medium Bias**
- **High Bias**

Sources include:
- overly confident tone  
- political/cultural markers  
- subjective framing  
- emotionally-influenced language  

---

### 3.4 Uncertainty Notes  
A one-line human-readable explanation of *why* the output might be unstable.

Examples:
- “Reasoning required to fill in missing facts.”
- “Topic is ambiguous or under-specified.”
- “Answer depends on assumptions not stated in the prompt.”

---

## 4. Truth Tail Format  
Every response ends with:

