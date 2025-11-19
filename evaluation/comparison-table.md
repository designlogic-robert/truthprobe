# TruthProbe Behavior Comparison Table

| Scenario                      | Expected Behavior | Example Output |
|------------------------------|------------------|----------------|
| Well-known fact              | High certainty, strong evidence | Strong |
| Complex reasoning            | Moderate certainty | Moderate |
| Opinion questions            | BiasRisk: Moderate | Moderate |
| Unknown topic                | CertaintyLevel < 5 | Weak |
| Sensitive domains            | TopicRisk: High | High |
