# t-distributed stochastic neighbor embedding

It is a nonlinear dimensionality reduction technique well-suited for embedding high-dimensional data for visualization in low
dimensional space of two- or three-dimensional point in such a way that similar objects are modeled by nearby points and
dissimilar objects are modeled by distant points with high probability.

## Algorithm
The t-SNE algorithm mainly comprises of two stages:
- First it constructs a probability distribution over pairs of high-dimensional objects in such a way that similar objects have a high
probability of being picked, whilst dissimilar points have an extremely small probability of being picked.
- Second, t-SNE defines a similar probability distribution over the points in the low-dimensional map, and it minimizes the [Kullback–Leibler
divergence](https://en.wikipedia.org/wiki/Kullback%E2%80%93Leibler_divergence) between the two distributions with respect to the locations 
of the points in the map.

### Stage-1 
Given a set of N dimensional points x1,x2...xN t-SNE first computes the probability p<sub>ij</sub> that are proportional to the similarity
of objects as follows:
