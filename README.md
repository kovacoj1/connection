# Connection

Recently, our team was faced with a problem outside of our expertise, and that under a tight deadline. In the heat of the moment, it seemed unreasonable to try to understand the underlying problem thoroughly. Instead, we opted for a mere brute-force approach, randomly trying different solutions or hypotheses.

This experience led me to the following question:
> Given a balanced binary tree of height $n$ (meaning there are $2^n - 1$ nodes), we pick any node uniformly at random and color it. What is the average number of nodes one needs to color until there's a path from the root to one of the leaf nodes?

In mathematical literature, this problem is known as percolation on trees, which has been studied extensively; however, there is no closed-form solution. We can, luckily, simulate the process at least for small values of $n$.

![Expected fraction of nodes colored until a root-to-leaf path is complete](percolation.png)

The decreasing fraction of the tree that needs to be colored does not compensate for the exponential growth in the number of nodes. My initial hypothesis was that for a small enough $n$, one would be better off with just randomly executing tests, hoping for a lucky streak of trial and error. However, it seems to be always advantageous to understand the underlying structure of the problem.

TODO: learning curve and initial threshold vs cost of random testing

---
The accompanying code can be found in this [jupyter notebook](connection.ipynb).
