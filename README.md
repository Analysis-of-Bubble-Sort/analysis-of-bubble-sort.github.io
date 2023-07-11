# Analysis of Bubble Sort

We focus mainly on analyzing the bubble sort of a randomly shuffled sequence.

[Wiki for Analysis of Bubble Sort](wiki)

The most popular version of bubble sort is to terminate after a pass without swaps, while the earliest version is to terminate after $n - 1$ passes, where $n$ is the number of the elements to be sorted.

The time complexity of the most popular version is $\Theta \left( n^{2} \right)$ on average, $\Theta \left( n^{2} \right)$ in the worst case and $\Theta \left( n \right)$ in the best case, while the time complexity of the earliest version is $\Theta \left( n^{2} \right)$ in every case.

However, our research shows that the earliest version might be more efficient than the popular version in almost every case, because determining whether there are no swaps in the latest pass might take too much time, depending on the efficiency of comparisons.

```cpp
// the most popular version
// to terminate after a pass without swaps
for (int i = n - 1; i >= 1; i--) {
    bool swapped = false;
    for (int j = 1; j <= i; j++) {
        if (a[j] > a[j + 1]) {
            swap(a[j], a[j + 1]);
            swapped = true;
        }
    }
    if (!swapped) {
        break;
    }
}
```

```cpp
// the earliest version
// to terminate after n-1 passes
for (int i = n - 1; i >= 1; i--) {
    for (int j = 1; j <= i; j++) {
        if (a[j] > a[j + 1]) {
            swap(a[j], a[j + 1]);
        }
    }
}
```

![](./logo.png)