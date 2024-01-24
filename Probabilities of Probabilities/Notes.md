# Probabilities of Probabilities Lecture Notes

Playlist: <https://www.youtube.com/playlist?list=PLZHQObOWTQDOjmo3Y6ADm0ScWAlEXf-fp>

## 1 Binomial Distributions

Laplace's Rule of Succession:
Read Amazon ratings: pretend that you see 2 more ratings, a positive and a negative.

![Pretend to See 2 More Ratings](1_files/pretend_2_more.jpg)

Binomial distribution "totals" formula:

![Totals Formula](1_files/totals_formula.jpg)

## 2 Probability Density

Sum of P(head) should be 1.
But lim paradox:

`lim == 0` -> `sum == 0`

![Lim 0 paradox](2_files/lim_zero.jpg)

`lim > 0` -> `sum == infinity`

![Lim 0 paradox](2_files/lim_positive.jpg)

Total probability must be 1.
Paradox: lim probabilities cannot be either all 0 or larger than 0.

Instead, we don't focus on individual values, but on a **range** of values.

![A Range of Values](2_files/range.jpg)

We don't use heights as probabilities.
Instead, the areas on the diagram now represent the probabilities.
This solves the `lim == 0` problem.

In this case, the y axis means probability per unit.

![Probability per Unit](2_files/probability_y_axis.jpg)

Go from big to small ranges (rectangles): shape of the probability distribution doesn't change.

![Area](2_files/range_lim_area.jpg)

Total area = 1

![Total Area](2_files/total_area_1.jpg)

### Discrete vs Continuous Probabilities

- Discrete: sum
- Continuous: not sum, but **integral**

![Discrete vs Continuous](2_files/discrete_vs_continuous.jpg)
