[![Build Status](https://travis-ci.org/alexanderGugel/gr-a-ph.svg?branch=master)](https://travis-ci.org/alexanderGugel/gr-a-ph)

gr-a-ph
=======

Graph-based programming for JavaScript

### Design Principles

gr-a-ph implements a unidirectional multigraph-based eventing system and
framework. The core components of the proposed system are:

- Nodes

  Nodes a the underlying foundation of gr-a-ph. They are stateless by design,
  have no direct side effects and are built around a single asynchronous
  function (called "process"). Nodes are not aware of their in- or outputs.
  They emit a certain set of events, but don't filter them. They do not
  distinguish between the source of the event.

- Edges

  Edges filter events. Edges in the context of gr-a-ph are fundamentally
  different from traditional edges: Instead of connecting exactly two nodes,
  they describe a relationship between n nodes (similar to a
  [Hypergraph](http://en.wikipedia.org/wiki/Hypergraph)).

- Graph

  A graph in terms of gr-a-ph is an object storing a reference to exactly one
  "entry node".

### Further Reading

- [Hypergraph](http://en.wikipedia.org/wiki/Hypergraph)
- [Multigraph](http://en.wikipedia.org/wiki/Multigraph)
