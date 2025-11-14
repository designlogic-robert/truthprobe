# TruthProbe — AI Safety Layer v1.0  
*A portable confidence, bias-risk, and evidence-strength indicator for LLM outputs.*

TruthProbe is a lightweight, open-source safety layer designed to run on top of any instruction-driven LLM (ChatGPT, Claude, Gemini, etc.).  
It adds a single structured “Truth Tail” to every response, automatically flagging:

- **Confidence Level** (low / medium / high)  
- **Evidence Strength** (weak / moderate / strong)  
- **Bias Risk** (low / elevated / high)  
- **Uncertainty Notes** (what the model is guessing about)

The goal is simple:  
**Make it obvious when the AI is confident and when it’s guessing.**

TruthProbe blends three worlds:

### 1. Practical Product Tooling  
A portable mode that real users can install in seconds.  
Zero setup. Zero dependencies. Just copy, paste, and activate.

### 2. Professional Open-Source Design  
Clear logic, documented behavior, predictable outputs.  
The repo includes the full specification, examples, and implementation notes—structured for engineers evaluating AI reliability and human-in-the-loop workflows.

### 3. Research-Driven Safety Primitive  
TruthProbe sits in a broader category of “lightweight alignment aids.”  
It operationalizes concepts like epistemic uncertainty, error decomposition, and bias surfaces in a way ordinary users can understand.

It is intentionally simple, intentionally transparent, and intentionally extensible.

---

## Why TruthProbe Exists

LLMs are extremely capable, but they blur the line between **certainty** and **guessing**.  
Typical users can’t see:

- when outputs are hallucination-prone,  
- when bias risks spike,  
- or when internal reasoning signals low confidence.

TruthProbe exposes that signal in plain English.

This is not meant to replace formal alignment research; it’s a *practical safety augmentation* for everyday use.

---

## Features

- **Portable Mode** — works across ChatGPT, Claude, and any LLM that accepts system-level instructions.  
- **Deterministic Format** — one-line Truth Tail for auditing or logging.  
- **Bias-Risk Heuristics** — simple but effective pattern detectors.  
- **Configurable Strictness** — users can tune how conservative TruthProbe is.  
- **Drop-in Integration** for workflows, scratchpads, or agents.

---

## Project Structure

- `truthprobe-spec.md` — logic, rules, and decision criteria  
- `truthprobe-mode.laf` — the reusable mode (copy/paste)  
- `examples/` — sample queries with annotated outputs  
- `extensibility-notes.md` — how to build BiasRisk or EvidenceStrength add-ons  

More components coming as the Design Logic ecosystem evolves.

---

## License

MIT License — open for community use, modification, and integration.

---

## Author

**Robert Hansen (Design Logic)**  
AI Systems Developer & Framework Architect  
Creator of LOS → Loryne → AdaptE → LaFQL (Design Logic Architecture)
