# TruthProbe v1.1 — AI Reasoning Transparency Layer  
*A portable evaluation layer for safer, clearer AI outputs.*

TruthProbe is a simple, lightweight reasoning-transparency tool designed for any LLM that accepts structured instructions (ChatGPT, Claude, Gemini, Grok, etc.).

It does not change how the AI writes.  
It evaluates how the AI *reasons*.

TruthProbe attaches a structured **TruthTail** to every answer, showing:

- **CertaintyLevel (0–10)** — Heuristic measure of how confident the model appears.
- **EvidenceStrength** — None / Weak / Moderate / Strong.
- **BiasRisk** — Whether the model leans toward a frame or omits alternatives.
- **AssumptionsDetected** — Implicit premises inside the answer.
- **FactVulnerability** — Whether the topic is known to trigger hallucinations.
- **CorrectionNeeded** — Signals when the user should double-check the information.

### Why This Matters  
Modern AI feels confident even when it’s wrong.  
TruthProbe makes that visible.

Users get a fast mental model:
> “Can I trust this, or should I re-check?”

### Design Philosophy  
TruthProbe is built on a simple principle:
**Reasoning transparency should be portable.**

Inspired by human-readable architecture ideas like:
- structured intent parsing  
- adaptive reasoning contexts  
- validation layers  
- memory anchoring  

TruthProbe follows the same spirit without depending on any proprietary system.

### Who Uses This?
- Researchers validating claims  
- Students writing papers  
- Professionals using AI for decisions  
- Developers creating safe agent behaviors  
- Everyday users who want reliability  

TruthProbe is a universal “trust layer” for AI.

### Files in This Repository
- `truthprobe-mode.laf` — The structured mode block you paste into any LLM.  
- `truthprobe-spec.md` — Technical specification + reasoning model.  
- `example-output.md` — Sample inputs + TruthTail examples.  
- `calibration-check.md` — Manual test suite to verify proper behavior.

TruthProbe v1.1 is free to use, fork, and extend.

