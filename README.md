# Analysis of Bubble Sort

The following pseudo-code of bubble sort is based on the flow chart in [*The Art of Computer Programming: Sorting and Searching*]().

$$
\begin{aligned}
    & \texttt{bubble-sort(} a_{1}, a_{2}, \cdots, a_{n} \texttt{):} \\
    & \qquad \texttt{for } i \texttt{ from } 1 \texttt{ to } n - 1 \texttt{ inclusive:} \\
    & \qquad \qquad \texttt{for } j \texttt{ from } 1 \texttt{ to } n - i \texttt{ inclusive:} \\
    & \qquad \qquad \qquad \texttt{if } a_{j} \gt a_{j + 1} \texttt{ then:} \\
    & \qquad \qquad \qquad \qquad \texttt{swap } a_{j}, a_{j + 1} \\
\end{aligned}
$$

According to [*Bubble Sort: An Archaeological Algorithmic Analysis*](), a widely described optimization of bubble sort is to terminate when the latest pass contains no swaps.

$$
\begin{aligned}
    & \texttt{optimized-bubble-sort(} a_{1}, a_{2}, \cdots, a_{n} \texttt{):} \\
    & \qquad \texttt{for } i \texttt{ from } 1 \texttt{ to } n - 1 \texttt{ inclusive:} \\
    & \qquad \qquad \texttt{let } t \texttt{ be } \bot \\
    & \qquad \qquad \texttt{for } j \texttt{ from } 1 \texttt{ to } n - i \texttt{ inclusive:} \\
    & \qquad \qquad \qquad \texttt{if } a_{j} \gt a_{j + 1} \texttt{ then:} \\
    & \qquad \qquad \qquad \qquad \texttt{swap } a_{j}, a_{j + 1} \\
    & \qquad \qquad \qquad \qquad \texttt{let } t \texttt{ be } \top \\
    & \qquad \qquad \texttt{if } t = \top \texttt{ then:} \\
    & \qquad \qquad \qquad \texttt{break} \\
\end{aligned}
$$

To bubble sort a random permutation, [Howard Demuth's Ph.D. thesis]() proves the expected number of the passes required is

$$
n + 1 - \sum_{1 \leq k \leq n} \frac{k ! k^{n - k}}{n !}
$$

And [*The Art of Computer Programming: Sorting and Searching*]() shows

$$
\sum_{1 \leq k \leq n} \frac{k ! k^{n - k}}{n !} = \sqrt{\frac{\pi n}{2}} - \frac{2}{3} + \frac{11}{24} \sqrt{\frac{\pi}{2 n}} + \frac{4}{135 n} - \frac{71}{1152} \sqrt{\frac{\pi}{2 n^{3}}} + \mathrm{O} \left( \frac{1}{n^{2}} \right)
$$

![](./logo.png)