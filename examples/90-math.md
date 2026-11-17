# Math

Formulas as GitHub, GitLab, Obsidian, Jupyter and Pandoc write them, in TeX.

## Inline

Reorder when stock falls below $s = d \cdot L + z \sigma_d \sqrt{L}$, where $d$ is the daily demand and $L$ the lead time in days.

With backticks, GitLab's form, which GitHub also reads, so `$` in prose stays a dollar: $`EOQ = \sqrt{2DS/H}`$.

A price is not math: it costs $5 and $10.

## Blocks

$$
EOQ = \sqrt{\frac{2 D S}{H}}
$$

$$
\sigma = \sqrt{\frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2}
$$

As a fenced block:

```math
\begin{aligned}
\text{fill rate} &= \frac{\text{units shipped on time}}{\text{units ordered}} \\
                 &= \frac{9\,412}{9\,800} \approx 96\,\%
\end{aligned}
```

A matrix:

$$
\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
$$

## LaTeX's own delimiters

Jupyter and Pandoc also read \( a^2 + b^2 = c^2 \) inline and

\[
\int_0^1 x^2 \, dx = \tfrac{1}{3}
\]

as a block.
