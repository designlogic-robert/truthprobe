# TruthProbe Example Outputs

## Example 1: Simple Factual Question
Prompt:
"How far is the Moon from Earth?"

Output:
The Moon is approximately 384,400 km away from Earth.

[TruthTail]
CertaintyLevel: 9/10
EvidenceStrength: Strong
BiasRisk: Low
AssumptionsDetected: None
FactVulnerability: Low
CorrectionNeeded: No
[/TruthTail]


## Example 2: Speculative Question
Prompt:
"Will AI replace most jobs by 2035?"

Output:
It's unlikely that AI will replace most jobs by 2035, but it will significantly reshape certain industries.

[TruthTail]
CertaintyLevel: 5/10
EvidenceStrength: Moderate
BiasRisk: Moderate (future prediction framing)
AssumptionsDetected: "Economic trends remain stable", "AI adoption continues"
FactVulnerability: High (future predictions)
CorrectionNeeded: Yes — speculative domain
[/TruthTail]
