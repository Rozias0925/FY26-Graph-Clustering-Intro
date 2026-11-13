# Graph Laplacians and Spectral Clustering

## For admissions reviewers

**Project type:** Exploratory research presentation authored by Chun-Hao Wen (geometry, urban networks, and MRI). **What this demonstrates:** graph modeling, feature-design decisions, spectral linear algebra, and interpretation across domains. **Evidence:** [presentation](https://rozias0925.github.io/FY26-Graph-Clustering-Intro/) and [poster](TWSIAM_poster.pdf). **Reproducibility:** the underlying analyses are not distributed; the visuals are illustrative rather than quantitative segmentation benchmarks.


This research presentation explores how graph Laplacians and spectral clustering can organize data from three settings: 3D geometry, the Taipei MRT network, and brain MRI images. It explains how graph construction and feature design affect the resulting partitions. This repository contains the presentation website and poster, but not the underlying analysis or segmentation code.

[Read the research presentation](https://rozias0925.github.io/FY26-Graph-Clustering-Intro/) · [View the poster](TWSIAM_poster.pdf) · [Researcher profile](https://rozias0925.github.io/Rozias-Website/index_en.html)

## Research question

How can a common spectral framework be adapted to datasets whose meaningful relationships are not captured by raw Euclidean coordinates alone?

The project follows a shared pipeline: define nodes and relationships, construct a weighted similarity graph, form its Laplacian, obtain a spectral representation, and cluster that representation. The application-specific work lies in deciding what a node represents and which features should determine similarity.

## Applications and methodological focus

| Setting | What the presentation examines |
| --- | --- |
| Stanford Bunny geometry | Face-level geometric features, including position and surface orientation, and their effect on mesh partitions. |
| Taipei MRT network | How fare-based and geographic similarity produce different station groupings. |
| Brain MRI images | Superpixel-based graph construction and intensity- and shape-related features for exploratory segmentation. |

The mathematical discussion connects the graph Laplacian to the smoothness energy

$$
f^\top Lf = \frac{1}{2}\sum_{i,j}w_{ij}(f_i-f_j)^2,
\qquad L=D-W.
$$

This provides a common language for examining how strongly connected observations are represented in the spectral embedding.

## Interpretation and limitations

The examples are exploratory demonstrations, not evidence that one graph construction is universally preferable. Partitions depend on the feature representation, similarity scale, and clustering choices. MRT groupings do not establish a causal account of urban development. The MRI illustrations are not a clinically validated diagnostic system or a substitute for quantitative segmentation evaluation.

## Public materials and local viewing

- `index.html`: research narrative, mathematical explanation, and result illustrations.
- `TWSIAM_poster.pdf`: accompanying research poster.
- PNG assets: figures displayed in the presentation.

To view the website locally, open `index.html`, or serve the repository with:

```bash
python -m http.server 8000 --bind 127.0.0.1
```

Then visit `http://127.0.0.1:8000/`. The page presents existing results; it does not rerun the research analyses.

## Authorship

Presentation website and accompanying explanatory text by **Chun-Hao Wen (文君豪)**, Department of Mathematics, National Taiwan Normal University. The linked research poster retains its original credits.
