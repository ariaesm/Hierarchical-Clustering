# Hierarchical Clustering, step by step

A Jupyter notebook that walks through agglomerative hierarchical clustering with SciPy, from a 10-point toy example to the Iris dataset.

**[Open the notebook →](hierarchical_clustering.ipynb)** (renders directly on GitHub, outputs included)

## What's inside

1. **Toy data:** build a dendrogram and read the merge history from `linkage`.
2. **Linkage methods:** single, complete, average and Ward on the same data, side by side.
3. **Choosing *k*:** cut the tree with `fcluster` and compare silhouette scores.
4. **Iris:** cluster 150 flowers without labels, then measure how well the clusters match the real species.

## Results on Iris (standardized features, 3 clusters)

| Linkage | Adjusted Rand Index | Silhouette |
| --- | --- | --- |
| single | 0.558 | 0.505 |
| complete | 0.573 | 0.450 |
| average | 0.562 | 0.480 |
| **ward** | **0.615** | 0.447 |

Ward recovers the species best. Single linkage has the highest silhouette but merges two species together. Internal metrics and agreement with ground truth don't always point the same way.

## Run it

```bash
pip install -r requirements.txt
jupyter notebook hierarchical_clustering.ipynb
```

## License

[MIT](LICENSE)
