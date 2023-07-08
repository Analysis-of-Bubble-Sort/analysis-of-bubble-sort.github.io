# Swap

## Definition

Swapping the element at the $l$-th position and the element at the $r$-th position is a transformation from a sequence $a$ to a sequence $b$ that $b_{l} = a_{r}, b_{r} = a_{l}$ and $b_{i} = a_{i}$ for every $i$ else.

## Example

Let $a = \left( 50, 10, 40, 30, 20 \right)$ and $l = 1, r = 3$, then swapping $50$ (the element at the $l$-th position) and $40$ (the element at the $r$-th position) transforms $a$ to $b$ that $b = \left( 40, 10, 50, 30, 20 \right)$.

$$
\begin{matrix}
    & \boxed{1} & 2 & \boxed{3} & 4 & 5 \\
    a & {\color{red} 50} & 10 & {\color{green} 40} & 30 & 20 \\
    b & {\color{green} 40} & 10 & {\color{red} 50} & 30 & 20 \\
\end{matrix}
$$

## Properties

Every swap is self-inverse.

$$
\sigma_{l, r} \left( \sigma_{l, r} \left( a \right) \right) = a
$$

The elements of a sequence after a swap are the elements of the sequence before the swap.

$$
\left\{ b_{i} \mid i \right\} = \left\{ a_{i} \mid i \right\} \text{ where } b = \sigma_{l, r} \left( a \right)
$$