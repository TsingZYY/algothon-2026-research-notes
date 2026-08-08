# Validation and Decision Methodology

## Evidence classes

We separated four kinds of evidence:

1. **Engineering checks** — interface, determinism, limits, runtime, and cache
   correctness.
2. **Public replay** — historical behaviour on data already available to the
   research process.
3. **Controlled transfer stress** — frozen comparisons across multiple public
   windows or cost settings.
4. **Unseen evaluation** — data and feedback not used to create or select the
   candidate.

Only the fourth category can provide clean evidence about future transfer. The
first three are still valuable, but answer different questions.

## Experimental rules

- Freeze the control, candidate family, window, costs, thresholds, and stopping
  rule before reading the result.
- Change one structural factor at a time whenever possible.
- Compare candidates through the same evaluator and accounting path.
- Report worst-window behaviour, fees, turnover, concentration, and runtime in
  addition to the headline score.
- Treat repeated use of the same public window as development, even when the
  implementation is strictly causal in time.
- Preserve rejected results so a closed strategy family is not rediscovered and
  retuned later.

## Release discipline

A candidate passed through separate gates:

- causal and structural sanity;
- mechanical interface checks;
- matched-window performance comparison;
- fee and robustness stress;
- source/package identity;
- explicit decision and upload authorization.

Passing a local package check never implied that the candidate had been uploaded
or that it should replace the incumbent.
