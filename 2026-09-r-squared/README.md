# The Day My R² Wouldn't Sit Still

How much of my R² variation was the train/test split alone?

**Data:** Medical Cost Personal dataset (1,338 rows) - `insurance.csv`

**Method:** the same linear regression with a smoker × BMI interaction, fitted
10,000 times on different random splits, to get the distribution of test-set R².

**Result:** R² ranged from about 0.75 to 0.90 across splits. The 0.86 I first saw
sits at the 80th percentile. The 0.91 I actually reported turned up 18 times in
10,000.

Run `r2_split_variability.ipynb` top to bottom on a fresh kernel.
