# Evolution of the Strategy Ideas

## 1. Simple return signals as controls

Momentum and reversal strategies were useful first baselines because they were
easy to reason about and exposed mistakes in accounting, sizing, fees, and
evaluation. Their main contribution was diagnostic: they showed that local
parameter tuning alone was unlikely to explain the strongest results.

## 2. Pair-spread mean reversion

The main conceptual breakthrough came from studying price-level relationships
instead of only return predictability. Some assets moved together while their
relative price spread reverted. This motivated a causal pair-spread strategy
with periodic structural review and a conservative fallback for assets without
a convincing relationship.

## 3. Stability before breadth

The first pair-selection mechanism could create asymmetric or many-to-one
relationships. The next step was to prefer relationships that remained mutual
and stable across adjacent checkpoints. This reduced the temptation to trade
every weak relationship discovered in the public sample.

## 4. Explain the residual book

After the stable pair component, some assets remained unexplained. A residual
cross-asset lead-lag network was used as a separate expert for this part of the
book. The design goal was not to stack every signal on every asset, but to route
each asset to the mechanism with the clearest role.

## 5. Bounded persistence

Cross-asset signals can become temporarily weak without reversing. A bounded
carry rule allowed recent direction to survive a short evidence gap. The key
constraint was that persistence had to be limited and attributable; it could not
become an indefinite hidden state.

## 6. Conservative online adaptation

The adaptive component compared a long-history expert with a recent-history
expert using only outcomes already realised in the new period. The long-history
expert remained the default, and the recent expert required stronger evidence
before taking control. This was online statistical routing, not reinforcement
learning.

## 7. Engineering safety as part of the strategy

A trading idea was not considered ready until it also behaved correctly under
repeated calls, reversed call order, malformed numeric input, extreme prices,
and long sequential runs. Determinism and fail-flat behaviour were treated as
part of the model design rather than packaging details.
