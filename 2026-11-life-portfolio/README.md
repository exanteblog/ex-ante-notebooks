# Everything You Do Is a Portfolio and You Are Managing It Badly

Allocating hours across the things you care about is the same problem as
allocating money across assets. Same inputs, same optimiser, same failure mode.

Data: constructed, not measured. Six weekly activities, drawn from a known
distribution so the true expected returns can be compared against what a short
sample says they are. Nobody has a real dataset of life satisfaction per hour,
and inventing one and calling it real would be worse than inventing one and
saying so.

Method: estimate expected returns and a six by six covariance matrix from 10
weeks, build three allocations from those estimates (unconstrained mean-variance,
the same with no short positions allowed, and naive equal weighting), then test
all three on 40 weeks none of them has seen. Repeated 1,000 times with fresh
data each run.

Result: the unconstrained optimiser put 97 of 100 hours into sleep and took a
position of minus 44 hours in seeing friends, which were the two largest
estimation errors in the sample rather than the two best and worst activities.
In sample it scored 1.06 against equal weighting's 0.15. Out of sample it fell
to 0.46 while equal weighting rose to 0.53. Across 1,000 repeats, equal
weighting averaged 0.36 and won 75% of the time against the unconstrained
optimiser, and 59% against the no-short version.

Caveat: set WEEKS_TRAIN to 100 and the optimiser starts winning. Optimisation is
not broken, it is demanding about how much evidence it needs.

References: DeMiguel, Garlappi & Uppal (2009); Kritzman, Page & Turkington
(2010); Markowitz (1952).

Run life_portfolio.ipynb top to bottom on a fresh kernel.