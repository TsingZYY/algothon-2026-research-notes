# Lessons and Takeaways

## Research lessons

- A new representation of the problem can matter more than another parameter
  search. Moving from returns to price-level relationships changed the project.
- Strong public-window performance and strong transfer evidence are different
  achievements.
- When a strategy family is saturated, new variants often reproduce the same
  exposure under different names.
- Module-level ablation is necessary: a candidate can contain one good idea and
  one unstable addition.
- Online adaptation should have a conservative default, explicit evidence gates,
  and an automatic route back to the stable expert.

## Engineering lessons

- Cache keys must bind to the visible data, not merely its length.
- Evaluator call order should not change positions.
- Position constraints, integer conversion, invalid values, and extreme prices
  need explicit tests.
- Synthetic data is useful for runtime and safety checks, but says nothing about
  expected trading performance.
- A frozen source identity and a verified package identity prevent accidental
  submission drift.

## Collaboration lessons

- “Do not guess; run the same experiment” was the most useful operating rule.
- Disagreements improved the process when they were translated into a measurable
  comparison or a corrected evidence boundary.
- Reporting what a result cannot prove made the final narrative more credible.
- A concise timeline and decision record are more reusable than a folder full of
  unlabelled high-scoring candidates.
