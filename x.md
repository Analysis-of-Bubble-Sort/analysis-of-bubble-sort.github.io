the number of the passes is almost $n - \mathrm{o} \left( n \right)$

the number of the passes is almost $n - \omega \left( 1 \right)$

the number of the passes is almost $n - \Theta \left( \sqrt{n} \right)$

$$
\lim_{n \to \infty} \mathrm{p} \left( n - \varepsilon n \leq m \leq n - \delta \right) = 1
$$

$$
\lim_{\lambda \to \infty, \nu \to 0} \lim_{n \to \infty} \mathrm{p} \left( n - \lambda \sqrt{n} \leq m \leq n - \nu \sqrt{n} \right) = 1
$$

$$
\mathrm{p} \left( m \leq k - 1 \right) = \frac{k !}{n !} k^{n - k}
$$

$$
\begin{aligned}
    \mathrm{p} \left( m \geq n - \varepsilon n \right) & = \mathrm{p} \left( m \geq n - \varepsilon n \right) \\
    & = 1 - \mathrm{p} \left( m \lt n - \varepsilon n \right) \\
    & = 1 - \mathrm{p} \left( m \leq n - \varepsilon n - 1 \right) \\
    & = 1 - \frac{\left( n - \varepsilon n \right) !}{n !} \left( n - \varepsilon n \right)^{\varepsilon n} \\
    & \geq 1 - \left( \left( \frac{1 - \varepsilon}{1 - \eta} \right)^{\eta} \right)^{n}
\end{aligned}
$$

$$
\begin{aligned}
    \frac{\left( n - \varepsilon n \right) !}{n !} \left( n - \varepsilon n \right)^{\varepsilon n} & = \prod_{n - \varepsilon n + 1 \leq k \leq n} \frac{n - \varepsilon n}{k} \\
    & \leq \prod_{n - \eta n + 1 \leq k \leq n} \frac{n - \varepsilon n}{k} \\
    & \leq \prod_{n - \eta n + 1 \leq k \leq n} \frac{n - \varepsilon n}{n - \eta n} \\
    & = \left( \frac{n - \varepsilon n}{n - \eta n} \right)^{\eta n} \\
    & = \left( \left( \frac{1 - \varepsilon}{1 - \eta} \right)^{\eta} \right)^{n} \\
\end{aligned}
$$

$$
0 \lt \eta \lt \varepsilon
$$

$$
\begin{aligned}
    \frac{\left( n - \delta \right) !}{n !} \left( n - \delta \right)^{\delta} & = \prod_{n - \delta + 1 \leq k \leq n} \frac{n - \delta}{k} \\
    & \geq \prod_{n - \delta + 1 \leq k \leq n} \frac{n - \delta}{n} \\
    & = \left( \frac{n - \delta}{n} \right)^{\delta} \\
    & = \left( 1 - \frac{\delta}{n} \right)^{\delta} \\
\end{aligned}
$$