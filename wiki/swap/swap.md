# Swap

[Wiki for Analysis of Bubble Sort](..)

## Definition

A swap of the $l$-th element and the $r$-th element, denoted by $\sigma_{l, r}$, is a transformation of a sequence that $b_{l} = a_{r}, b_{r} = a_{l}$ and $b_{i} = a_{i}$ for every $i$ else where $a$ is a sequence and $b = \sigma_{l, r} \left( a \right)$.

## Example

If $a = \left( 50, 10, 40, 30, 20 \right), b = \sigma_{l, r} \left( a \right)$ and $l = 1, r = 3$, then $b = \left( 40, 10, 50, 30, 20 \right)$.

$$
\begin{matrix}
    & \boxed{1} & 2 & \boxed{3} & 4 & 5 \\
    a & {\color{red} 50} & 10 & {\color{green} 40} & 30 & 20 \\
    b & {\color{green} 40} & 10 & {\color{red} 50} & 30 & 20 \\
\end{matrix}
$$

## Properties

The elements of a sequence after a swap are the elements of the sequence before the swap.

$$
\left\{ b_{i} \mid i \right\} = \left\{ a_{i} \mid i \right\} \text{ where } b = \sigma_{l, r} \left( a \right)
$$

Every swap is self-inverse.

$$
\sigma_{l, r} \left( \sigma_{l, r} \left( a \right) \right) = a
$$

For every element before the $l$-th position before a swap, the elements lefter than it after the swap are the elements lefter than it before the swap.