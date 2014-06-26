Dijkstra's Algorithm
--------------------

Initialize

- Start with a weighted graph and an empty list of checked nodes
- Select a start node
- Initialize the distance and precursor node for eadch node in the list of weighted nodes based on the start node and the followning three rules:
   - the precursor of the start node is itself and its distance is zero.
   - for any node that is not connected to the start node, the precursor is itself and its distance is infinite.
   - for any node that is connected to the start node, the precursor is the start node and the distance is the weight of the edge connecting the node to the start node.

Iterate on the following steps

- Select a non-checked node with minimal distance as the new current node (if none we're done)
- Add this new current node to the checked list
- For each node connected to the current node, recalculate its distance and precursor as follows:
   - If the sum of the distance to the current node and the weight of the connecting edge is less than the distance of the node, set its distance to this new distance and its precursor to the current node.
   - otherwise leave it as is.

When the algorithm terminates, we can find an optimal path to any node by tracing back through the sequence of precursors.  The distance to any node is stored with the node.
