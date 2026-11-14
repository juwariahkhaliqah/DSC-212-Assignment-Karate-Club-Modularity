Modularity on the Karate Club Graph

DSC212 – Graph Theory research assignment, Juwariah Khaliqah (IMS25101)

This notebook applies Newman's spectral modularity method to Zachary's Karate Club graph, using NumPy and NetworkX. A community is split using the signs of the leading eigenvector of its modularity matrix block, and it is left alone once that eigenvalue is 0 or less. After every split I redrew the graph and recomputed degree, betweenness, closeness and clustering for each node inside its own community, since computing them on the full graph would never change.

The first split gave Q = 0.372 and matched the real division of the club for 33 of 34 members (only member 9 was misplaced). Three more splits brought Q up to 0.409, ending with communities of 13, 10, 5, 5 and 1 members. Most of the gain came from the first cut. Splitting into smaller groups also changed the centrality scores a lot, with betweenness shifting the most, and the clustering coefficient was the least useful for picking out leaders.
