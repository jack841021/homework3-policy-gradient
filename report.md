# Homework3-Policy-Gradient report


## All About That Base

Look at results, we can discover that the one with baseline has lower variance.

However, average return is dominated by initial configuration.

It seems that baseline does not affect gradient.

Why?

### loss = ( Σ [ Σ [ log ( policy ) * ( reward - baseline ) ] τ from 0 to T ] n from 1 to N ) / NT

Baseline is not a function of current action but reward is.

Var [ reward - baseline ] < Var [ reward ] => Var [ loss with baseline ] < Var [ loss without baseline ]

### gradient = ∇ [ loss ] w.r.t θ

Baseline is not a function of current action, so it is not a function of θ.

After differentiated by θ, it disappears.

Therefore, it does not affect gradient.


## Problem 5

Actor-critic should have better performance compare to previous problems.

Indeed, it surpassed 150 quickly.

However, many classmates including me couldn't have the algorithm hit 200.

It just kept hanging around 175 even for 300 iterations.

There must be something wrong but I couldn't figure it out.
