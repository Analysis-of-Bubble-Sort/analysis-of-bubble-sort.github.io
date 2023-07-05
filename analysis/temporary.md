$a_{1}, a_{2}, \cdots, a_{n}$ to $b_{1}, b_{2}, \cdots, b_{n}$

Let $a^{i, j}_1, a^{i, j}_{2}, a^{i, j}_{3}, \cdots, a^{i, j}_{n}$ be the sequence before the $j$-th comparison in the $i$-th pass.

$$
a^{i + 1}_{k} = a^{\infty}_{k} \text{ for } x
$$

$$
a^{i, j + 1}_{k} = \begin{cases}
    a^{i, j}_{k} & \text{for } k \lt j \\
    \min \left\{ a^{i, j}_{j}, a^{i, j}_{j + 1} \right\} & \text{for } k = j \\
    \max \left\{ a^{i, j}_{j}, a^{i, j}_{j + 1} \right\} & \text{for } k = j + 1 \\
    a^{i, j}_{k} & \text{for } k \gt j + 1 \\
\end{cases}
$$

$$
a^{i, j}_{k} = \begin{cases}
    \min \left\{ \max \left\{ a^{i, j}_{k'} : k' \le k \right\}, a^{i, j}_{k + 1} \right\} & \text{for } k \lt j \\
    \max \left\{ a^{i, j}_{k'} : k' \le k \right\} & \text{for } k = j \\
    a^{i}_{k} & \text{for } k \gt j
\end{cases}
$$

$$
a^{i, j}_{k} = a^{n, j}
$$