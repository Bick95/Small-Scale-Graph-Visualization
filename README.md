# Small-Scale-Graph-Visualization
A little tool to render directed graphs on a rather small scale.

An empty Graph Class can be created by:

```python
g = Graph()
```

Then, either individual nodes can be added 

```python
g.add_node(node, attribute)
```

and individual edges by

```python
g.add_edge((edge1, edge2), attribute)
```

A batch of nodes can be added by 

```python
g.add_nodes(nodes, attributes)
```
where `nodes` is a list of node IDs. `attributes` is a list of satellite data per node.

Alternatively, you can can call 

```python
g.add_nodes(nodes)
```

where , in this case, no attributes are provided and `nodes` is a list of nodes. Alternatively, `nodes` can be a dictionary with keys being nodes and values the attributes, which are later labeled as node-labels.

Similarly, in 

```python
g.add_edges(edges, attributes)
```
attributes may be provided optionally (the same input pattern applies as for assigning a batch of nodes), only that this time every edge is a tuple of the format `(node1, node2)`.

Graph visualizations can be obtained by calling 

```python
g.visualize(html_flag)
```

where `html_flag==True` determines that the function returns a `matplotlib.pyplot.figure()` and `html_flag==True` determines that the function simply shows the respective plot without returning anything. 

Graph visualization parameters can be adjusted in the code. 

An example visialization looks as follows:

![expl_img][img_link]

[img_link]: https://github.com/Bick95/Small-Scale-Graph-Visualization/blob/master/img/example.png "Example Visualization"
