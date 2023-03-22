# CMPS 2200 Reciation 5
## Answers

**Name:** Tyler Simms


Place all written answers from `recitation-06.md` here for easier grading.







- **1b.**

Sorted lists:
|   n |   qsort-fixed-pivot |   qsort-random-pivot |   selection-sort |
|-----|---------------------|----------------------|------------------|
|   1 |               0.009 |                0.011 |            0.005 |
|  10 |               0.054 |                0.049 |            0.010 |
|  50 |               0.697 |                0.282 |            0.082 |
| 100 |               3.698 |                0.740 |            0.359 |
| 200 |               9.675 |                1.503 |            1.253 |
| 300 |              66.063 |                2.672 |            2.512 |
| 400 |              94.875 |                4.343 |            5.666 |
| 500 |             109.143 |                4.426 |            6.938 |
| 750 |             282.436 |                7.329 |           17.968 |
| 900 |             396.145 |                9.358 |           68.521 |

Random lists (unsorted):
|   n |   qsort-fixed-pivot |   qsort-random-pivot |   selection-sort |
|-----|---------------------|----------------------|------------------|
|   1 |               0.785 |                0.026 |            0.018 |
|  10 |               0.062 |                0.070 |            0.017 |
|  50 |               0.287 |                0.354 |            0.128 |
| 100 |               0.515 |                0.609 |            0.343 |
| 200 |               1.456 |                1.582 |            1.403 |
| 300 |               2.150 |                2.442 |            2.772 |
| 400 |               2.885 |                3.018 |            4.774 |
| 500 |               3.207 |                4.495 |           12.418 |
| 750 |               6.777 |                8.279 |           55.911 |
| 900 |               8.202 |                9.962 |           84.258 |

The asymptotic bound for Selection sort is O(n^2). The asymptotic bound for Quicksort with a fixed pivot and Quicksort with a random pivot is O(nlogn) when the input list is random. When the input list is sorted, the asymptotic bound for Quicksort with a fixed pivot is O(n^2) because this situation is the worst case scenario. The empirical runtimes for the algorithms match the asymptotic behavior. The Changing the type of input list affected the performance of some of these alorithms more than others. Quicksort with a fixed pivot improved significantly when the list changed from being sorted to random. When the list was sorted, Quicksort with a fixed pivot had an approximate running time of around 300 to 400 milliseconds. When the list was random, the running time decreased to regularly be under 10 milliseconds. Quicksort with a random pivot and Selection sort had almost no difference when the input list changed. If anything, the average running time for these two algorithms slightly increased when the input list changed from sorted to random.

- **1c.**

Sorted lists:
|   n |   qsort-random-pivot |   tim-sort |
|-----|----------------------|------------|
|   1 |                0.019 |      0.003 |
|  10 |                0.339 |      0.004 |
|  50 |                0.334 |      0.003 |
| 100 |                0.741 |      0.006 |
| 200 |                1.612 |      0.008 |
| 300 |                2.461 |      0.010 |
| 400 |                3.399 |      0.010 |
| 500 |                4.778 |      0.013 |
| 750 |                8.149 |      0.016 |
| 900 |               10.436 |      0.018 |

Random lists (unsorted):
|   n |   qsort-random-pivot |   tim-sort |
|-----|----------------------|------------|
|   1 |                0.011 |      0.002 |
|  10 |                0.065 |      0.002 |
|  50 |                0.453 |      0.005 |
| 100 |                0.846 |      0.010 |
| 200 |                1.662 |      0.021 |
| 300 |                2.514 |      0.040 |
| 400 |                3.539 |      0.044 |
| 500 |                4.182 |      0.052 |
| 750 |                7.056 |      0.089 |
| 900 |                8.240 |      0.115 |

My fastest sorting algorithm is definitely Quicksort with a random pivot when considering both the running times using a sorted list and a random list. Based on the tables, Timsort is still much faster than Quicksort with a random pivot. Timsort never took more than 0.12 milliseconds in either table.