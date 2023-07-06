# Swap and Inversion

Among all the algorithms sorting a sequence by swapping adjacent elements, the bubble sort contains the minimum number of the swaps which is equals to the inversion of the sequence before sorting, and each swap of a bubble sort is necessary.

An inversion of a sequence is a pair of unordered elements, which means the left element of the pair is greater than the right element of the pair. And the inversion number of a sequence is the number of the inversions of the sequence. An sequence is ordered if and only if the inversion number of it is exactly zero.

A swap is to choose two positions and to exchange the element at the left position and the element at the right position. The element at the left position after a swap is the element at the right position after the swap, and the element at the right position after a swap is the element at the left position before the swap. For any other position, the element at it after the swap is the element at it before the swap.

For example,

$$
\begin{matrix}
    & \boxed{1} & 2 & \boxed{3} & 4 & 5 \\
    a & {\color{red} 50} & 10 & {\color{green} 40} & 30 & 20 \\
    a' & {\color{green} 40} & 10 & {\color{red} 50} & 30 & 20 \\
\end{matrix}
$$

If the sequence $a$ is $\left( 50, 10, 40, 30, 20 \right)$, which means $a_{1} = 50, a_{2} = 10, a_{3} = 40, a_{4} = 30, a_{5} = 20$, then after swapping the elements at the positions $l = 1$ and $r = 3$, the sequence $a'$ is $\left( 40, 10, 50, 30, 20 \right)$, which means $a'_{1} = 40, a'_{2} = 10, a'_{3} = 50, a'_{4} = 30, a'_{5} = 20$. Therefore, $a'_{l} = a_{r}, a'_{r} = a_{l}$, and if $i \ne l$ and $i \ne r$ then $a'_{i} = a_{i}$.

For the element at the right position before swapping unordered adjacent elements, the element at the left position before the swap is greater than it and is lefter than it before the swap but righter than it after the swap, and each element lefter than it except the element at the left position before the swap is still lefter than it after the swap. Therefore, swapping unordered adjacent elements decreases the number of the elements lefter and greater than it by exactly one, which means the number of the elements lefter and greater than it after the swap is exactly one less than the number of elements lefter and greater than it.

For example,

$$
\begin{matrix}
    & 1 & 2 & 3 & \boxed{4} & \boxed{5} \\
    a & {\color{green} 50} & 10 & {\color{blue} 40} & {\color{yellow} 30} & {\color{red} 20} \\
    a' & {\color{green} 50} & 10 & {\color{blue} 40} & {\color{red} 20} & 30 \\
\end{matrix}
$$

If the sequence is $a = \left( 50, 10, 40, 30, 20\right)$, then after swapping the unordered elements at the positions $l = 4$ and $r = 5$, the sequence $a'$ is $\left( 50, 10, 40, 20, 30 \right)$. The elements lefter and greater than $a_{r}$ are $50, 40, 30$ before the swap but $50, 40$ after the swap. Therefore, swapping unordered adjacent elements decreases the number of the elements lefter and greater than $a_{r}$ by exactly $1$.

For the element at the left position before the swap, the elements lefter than it before the swap are still lefter than it and each element lefter than it after the swap except the element at the right position before the swap is lefter than it before the swap. Therefore, swapping unordered adjacent elements does not change the number of the elements lefter and greater than it, which means the number of the elements lefter and greater than it after the swap is the same as the number of elements lefter and greater than it.

For example,

$$
\begin{matrix}
    & 1 & 2 & 3 & \boxed{4} & \boxed{5} \\
    a & {\color{green} 50} & 10 & {\color{blue} 40} & {\color{red} 30} & 20 \\
    a' & {\color{green} 50} & 10 & {\color{blue} 40} & 20 & {\color{red} 30} \\
\end{matrix}
$$

If the sequence is $a = \left( 50, 10, 40, 30, 20\right)$, then after swapping the unordered elements at the positions $l = 4$ and $r = 5$, the sequence $a'$ is $\left( 50, 10, 40, 20, 30 \right)$. The elements lefter and greater than $a_{l}$ are $50, 40$ before the swap and after the swap. Therefore, swapping unordered adjacent elements does not change the number of the elements lefter and greater than $a_{l}$.

For any other element, the elements lefter than it before the swap is the same as the elements lefter than it after the swap, which means each element lefter than it before the swap is still lefter than it after the swap and each element lefter than it after the swap is lefter than it before the swap. Therefore, swapping unordered adjacent elements does not change the number of the elements lefter and greater than it, which means the number of the elements lefter and greater than it after the swap is the same as the number of elements lefter and greater than it.

For example,

$$
\begin{matrix}
    & 1 & 2 & 3 & \boxed{4} & \boxed{5} \\
    a & {\color{green} 50} & 10 & {\color{red} 40} & 30 & 20 \\
    a' & {\color{green} 50} & 10 & {\color{red} 40} & 20 & 30 \\
\end{matrix}
$$

If the sequence is $a = \left( 50, 10, 40, 30, 20\right)$, then after swapping the unordered elements at the positions $l = 4$ and $r = 5$, the sequence $a'$ is $\left( 50, 10, 40, 20, 30 \right)$. Let $i$ be $3$, then the elements lefter and greater than $a_{i}$ are $50$ before the swap and after the swap. Therefore, swapping unordered adjacent elements does not change the number of the elements lefter and greater than $a_{i}$.

$$
\begin{matrix}
    & \boxed{1} & \boxed{2} & 3 & 4 & 5 \\
    a & {\color{green} 50} & 10 & {\color{red} 40} & 30 & 20 \\
    a' & 10 & {\color{green} 50} & {\color{red} 40} & 30 & 20 \\
\end{matrix}
$$

If the sequence is $a = \left( 50, 10, 40, 30, 20\right)$, then after swapping the unordered elements at the positions $l = 1$ and $r = 2$, the sequence $a'$ is $\left( 10, 50, 40, 30, 20 \right)$. Let $i$ be $3$, then the elements lefter and greater than $a_{i}$ are $50$ before the swap and after the swap. Therefore, swapping unordered adjacent elements does not change the number of the elements lefter and greater than $a_{i}$.

Therefore, swapping unordered adjacent elements decreases the inversion number of the sequence by exactly one, which means the inversion number of the sequence after the swap is exactly one less than the inversion number of the sequence before the swap. Inversely, swapping ordered adjacent elements increases the inversion number of the sequence by exactly one, which means the inversion number of the sequence after the swap is exactly one more than the inversion number of the sequence before the swap.

The number of the swaps of an algorithm sorting a sequence by swapping adjacent elements is not more than the inversion number of the sequence. Among all the algorithms sorting a sequence by swapping adjacent elements, an algorithm swapping exactly unordered adjacent elements such as the bubble sort contains the minimum number of the swaps which is equals to the inversion of the sequence before sorting. And each swap of a bubble sort is necessary, because each swap of a bubble sort one-to-one corresponds to a decrease of exactly one of the inversion number of the sequence.

---

A pass of a bubble sort is, for each pair of adjacent positions of the sequence from the left to the right, to compare the elements at the positions and to swap them if and only if they are unordered.