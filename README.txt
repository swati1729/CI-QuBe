Combinatorial Instances for Quantum Benchmarking (CI-QuBe, 'see-cube') is a library of interesting instances to test and benchmark quantum algorithms for combinatorial problems.

Those wishing to cite the repository may use the following BibTex entry:
@article{CI-QuBe2021,
title={CI-QuBe},
author={Reuben Tate and Swati Gupta},
journal={GitHub repository},
publisher={GitHub},
howpublished={\url{https://github.com/swati1729/CI-QuBe}}
year={2021}
}

Each instance consists of a .txt file corresponding to a graph. For each .txt file, the first few lines may consist of comments; each comment will start with the character "#". The first non-comment line will then consist of two integers with a single space between them of the form "n m" where n is the number of nodes in the instance and m is the number of edges. After this, there will be m more lines, one for each edge, of the form "u v w" to denote that there is an edge from u to v with weight w. In the case that the graph is a unit weight graph, w will simply be 1.

The instances are grouped into various folders which we describe below:

-Karloff: These are the instances discussed in Karloff's paper [1]. Karloff shows that there is a sequence of graphs whose GW approximation ratio approaches 0.878; these are the graphs at the beginning of such a sequence using the construction Karloff proposes. Each file is of the form "Karloff_m_t_b.txt" which corresponds to an instance J(m,t,b) as described in Karloff's paper.

-ratio912: These are graphs in the MQLIB instance library [2] all have a 0.912 approximation ratio with respect to GW. For these instances, the optimal cut is also always 2/3 of the total number of edges.

-hard (heuristics): These are instances in the MQLIB instance library [2] where no heuristic was able to achieve 99.9% of the optimal solution within 5% of the alloted runtime. Most of these instances have a combination of positive and negative weighted-edges with weights with very large magnitude can appear but with vanishingly small frequency.

-SRG: These are all (strongly-regular) graphs that are pseudo-geometric with respect to generalized quadrangles of order (3,t), i.e., GQ(3,t). This consists of 2 non-isomorphic strongly-regular graphs with parameters (n,k,lambda,nu) = (16, 6, 2, 2), 28 non-isomorphic strongly-regular graphs with parameters (n,k,lambda,nu) = (40, 12, 2, 4), 167 non-isomorphic strongly-regular graphs with parameters (n,k,lambda,nu) = (64, 18, 2, 6), and 1 non-isomorphic strongly-regulars graph with parameters (n,k,lambda,nu) = (112, 30, 2, 10). For all but 13 instances (strongly_regular_40_11.txt, strongly_regular_40_12.txt, ..., strongly_regular_40_23.txt) in the folder, it can be shown that Max-Cut(G) = (2/3)|E|; this fact, along with other properties of pseudo-geometric graphs with respect to order (3,t), can be used to prove that the (instance-specific) Goemans-Williamson approximation ratio achieved is 0.912 for all but the 13 graphs.

-instanceLibrary: These are the instances of up to 19 nodes that were used in our paper "Bridging  classical and quantum with SDP initialized warm-starts for QAOA" [3]. Instead of just using Erdös-Renyí graphs for example (which have predictable properties with respect to Max-Cut), we used a large variety of graphs coming from a variety of random graph models (e.g. Erdös-Renyí, Barabasi Albert, Dual of Barabasi-Albert, Watts-Strogatz, Newman-Watts-Strogatz, and random regular graphs). These models were used to generate unit-weight graphs, after which, for each unit-weight graph, we create an additional 3 weighted graphs by applying different edge-weight distributions, some of which allowing for both positive and negative edge weights. The precise details for how these instances were constructed can be found in [3].

ACKNOWLEDGEMENT
This  material  is  based  upon  work  supported  by the  Defense  Advanced  Research  Projects  Agency (DARPA)  under  Contract  No.HR001120C0046.


References:
[1] Howard Karloff,   “How   good   is   the   Goemans–Williamson MAX-CUT algorithm?” SIAM Journalon Computing 29, 336–350 (1999).
[2] Iain Dunning, Swati Gupta, and John Silberholz. 2018. What works best when? A systematic evaluation of heuristics for Max-Cut and QUBO. INFORMS Journal on Computing 30, 3 (2018), 608–624.
[3] Reuben Tate, Majid Farhadi, Creston Herold, Greg Mohler, and  Swati  Gupta,  “Bridging  classical and quantum with SDP initialized warm-starts for QAOA,” arXiv preprint arXiv:2010.14021  (2020).
[4] Reuben  Tate, Bryan  Gard, Greg  Mohler, and  Swati  Gupta, "Classically-inspired Mixers for QAOA beat Goemans-Williamson for Max-Cut at Low Circuit Depths", working paper (2021). 
