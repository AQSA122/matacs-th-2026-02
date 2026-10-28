

## AI vs. rules.

AI will be used to extract relevant information from proposals because documents may have different formats and unstructured wording.
Plain code and rules will handle validating mandatory requirements, applying admin-defined weights, calculating scores out of 100, and ranking proposals consistently. 
I drew the line because AI is better at understanding unstructured documents, while plain code ensures scoring and ranking are consistent, predictable, and auditable.

## Consistency and explainability.

The system uses predefined criteria, admin-configured weights, and consistent scoring rules to ensure the same proposals get the same scores when evaluated under the same conditions.
If two proposals have the same score, the system applies admin-defined tie-break rules, like lower price or shorter delivery time, and shows the reason for the ranking along with each proposal's score and criterion breakdown. 
If tie-break rules cannot distinguish the proposals, they share the same rank, and the human reviewer makes the final decision.

## Human in the loop

Human reviewer sees the system ranking and evidence, then confirms or overrides the result with a reason. 
If they override it, the system records the original scores, the final choice, the reason, reviewer name, and timestamp so the decision is fully traceable.

## Changing criteria

Since the system evaluates everything automatically, there's no manual recalculation needed.
It just updates the scores and rankings based on the new rules while keeping the old results for audit.

## Risks
The system doesn't automatically know it's wrong, so we need specific checks. For your proposal tool you could say: AI extracts data like price, timeline, and license, then the system stores the supporting text and page numbers, 
checks required fields and formats, and flags missing or conflicting info before scoring. Scores and rankings are calculated by fixed rules with file limits to keep costs down, and anything uncertain gets flagged for the reviewer. That helps catch errors before they affect decisions.
No system is perfect, so the human review and audit trail are the backstop.