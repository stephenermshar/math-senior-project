Persistent homology is a tool for understanding the shape of a data set.
For instance, if a data set is a collection of points in two dimensional space, then it can be graphed.
We can easily look at the graph and see whether the data clumps together in certain places, or if it forms more interesting shapes, like a loop.
We can graph data in one and three dimensions as well, but with dimensions four and higher we're no longer able to intuitively and visually observe the data directly.

In section () we'll explore Homology, which gives us tools to understand structures analogous to holes in a shape, regardless of the dimension in which the shape is embedded.
When we use Persistent Homology, we'll be converting our data into a form where we can apply tools from homology to understand it.
There are a variety of ways to convert data into a form where homology can be applied, most of which, including the one we'll explore in section (), rely the choice of a scale parameter.
This scale parameter is used to determine whether points in the data set are related to each other based on the distance between them.
We'll want to understand the structure of the data at multiple scales, so we'll look at its homology along a range of scales.
If a structure revealed by homology persists on a wide range of scales then we can feel more confident that this structure is a good approximation for the shape of the data.
In section () we'll look at different ways of visualizing a data set's homological structure along a range of scales.

Persistent Homology has been used in a wide variety of fields as a data analysis tool, and has some potential applications outside of data analysis as well.
In section () we'll look at some of these uses, and potentially provide a simple demonstration of an insight that can be gathered using persistent homology.


To calculate homology on our data we'll first need to convert it into a simplicial complex. A Simplicial complex is just a collection of sets of points from our dataset. Each of these sets of points is called an n-simplex. To keep track of signs later on we'll give each simplex an orientation, which will be denoted by the order in which its points are listed. In this paper we'll arbitrarily choose to list the points in increasing order of the point's label.The resulting simplicial complex will be a graph-like structure, where pairs of connected points are connected by a line, triples by a triangle, four points by a tetrahedron, and so on.

There are many ways of constructing simplicial complexes from data, but we'll focus on one of the more intuitive and original methods used, the cech complex.

[cech complex definition]

(should I explain the cech complex or expect the reader to labor over the definition if they're confused?)
