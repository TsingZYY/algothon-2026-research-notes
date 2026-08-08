# Research Timeline

## Early July — understand the task

- Read the official interface, scoring, position-limit, runtime, and packaging
  requirements.
- Reproduced the local evaluator before changing the starter strategy.
- Established a rule that local checks, public replay, and server feedback must
  be reported separately.

## 13–15 July — build simple baselines

- Tested short-horizon momentum and reversal ideas.
- Used these strategies as controls for accounting, fees, turnover, and runtime.
- Concluded that repeated tuning inside the same reversal family had limited
  information value.

## 16–17 July — move from returns to price-level structure

- Changed the research question from “which return window works?” to “which
  relationships in price levels remain stable?”
- Identified pair-spread mean reversion as the first materially stronger
  structural mechanism.
- Added causal reselection and history-bound caching so results did not depend on
  evaluator call order.

## 17–20 July — treat submissions as measurements

- Tracked the effect of the expanding evaluation window.
- Stopped comparing scores produced on different windows as though they were
  directly comparable.
- Used the frozen incumbent as a control and treated each limited submission
  opportunity as a controlled measurement rather than an invitation to submit
  an arbitrary new variant.

## 21–24 July — close saturated strategy families

- Audited many nearby variants and found that most were highly correlated with
  the existing pair-spread strategy.
- Introduced one-change-at-a-time experiments, preregistered gates, cost stress,
  and explicit rejection rules.
- Shifted research effort away from small parameter changes and toward distinct
  mechanisms with incremental explanatory value.

## 25 July — separate public-window optimisation from transfer

- Replayed candidates on the fully released General window using one frozen
  evaluator and data identity.
- Produced a strong public-window-specialised strategy.
- Recorded that this result measured fit to a known public window, not future
  hidden-period performance.

## 26–30 July — design for transfer and failure containment

- Froze stable structural relationships rather than repeatedly reselecting from
  all known data.
- Combined pair-spread signals with a residual cross-asset routing component.
- Tested bounded weak-signal persistence and online expert selection.
- Added malformed-input handling, deterministic cache behaviour, position-limit
  checks, and long synthetic runtime tests.

## 30 July–3 August — audit the final research branch

- Used component ablation to distinguish useful modules from unstable additions.
- Compared cost sensitivity, turnover, drawdown, concentration, and runtime, not
  only aggregate score.
- Preserved the distinction between a locally verified package and an actually
  uploaded competition submission.

## 9 August — archive the process privately

- Condensed the work into a timeline, idea map, methodology, and lessons.
- Deliberately excluded code, data, exact parameters, submission artifacts, and
  reproducible implementation details.
