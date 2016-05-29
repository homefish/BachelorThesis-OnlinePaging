# An efficient implementation of the Optimal Paging Algorithm

This is my thesis that I wrote for my bachelor's degree in Computer Science.
I implemented a data structure that computes the cost of the optimal offline paging
algorithm efficiently.

##Abstract
In this Bachelor thesis we designed a new data structure denoted as LTrees
which keeps track of the costs that are incurred by the optimal offline paging
algorithm OPT [1]. We analyze LTrees and show that for a page-set
size m it answers the question whether a requested page is in OPT's cache
in O(alpha(2m)) amortized time, which is virtually constant since the inverse
Ackermann function alpha is smaller than 5 for any practical input size. This
presents an improvement over other approaches that require O(log(m)) [2]
and O(log(k)) [3] time, where k is the cache size. The space required by
LTrees is theta(m).
Using real-world traces we have examined how LTrees behaves in comparison
to a timestamp based implementation [12] which we refer to as TStamp.
The experiments demonstrate that the runtime for LTrees is robust towards
different cache sizes, whereas the runtime for TStamp can dramatically increase.
Our data structure can be used as a subroutine for the page replacement
algorithm RLRU [2]. Another application is the calculation of the empirical
competitive ratio [7].
