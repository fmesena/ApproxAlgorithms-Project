# Approximation Algorithms

## Authors
This project is the result of joint work with my friends, Diogo Ramalho, Joana Alves, and Tomás Vieira.

## Information about this repository
This the repository for the project of the Advanced Algorithms course.
The main idea of the project was to conduct an experimental evaluation of three different approximation algorithms for computing metrics in very big graphs. We have chosen the following metrics: Average Path Length (APL), Betweenness centrality, and Clustering Coefficient. 

For the APL, we implemented the Hyperanf approximation algorithm developed by Paolo Boldi, Marco Rosa, and Sebastiano Vigna in "Hyperanf: Approximating the neighbourhood function of very large graphs on a budget" [(see the paper here)](https://dl.acm.org/doi/10.1145/1963405.1963493), which heavily relies on the well known cardinality estimation technique developed by Flajolet et al in "Hyperloglog: The analysis of a near-optimal cardinality estimation algorithm" [(see the paper here)](https://hal.archives-ouvertes.fr/hal-00406166/).

For the Betweenness Centrality, we implemented the (exact) Brandes algorithm and the recent approximation algorithm developed by Matteo Riondato and Evgenios Kornaropoulos in "Fast approximation of betweenness centrality through sampling" [(see the paper here)](https://dl.acm.org/doi/abs/10.1145/2556195.2556224).

For the Clustering Coefficient, we implemented the (obvious) O(N^3)** algorithm and the algorithms developed by Siddharth Bhatia in "Approximate triangle count and clustering coefficient" [(see the paper here)](https://dl.acm.org/doi/10.1145/3183713.3183715).

**In this version of the code, the algorithm runs in O(N^4) because to check if the pair (u,v) is an arc we spend O(N) time, it can be easily changed to O(N^3) by previously build a hash table which given a pair (u,v) tells us whether (u,v) is an arc or not.**