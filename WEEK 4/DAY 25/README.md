# Day 25 — Building a Graph from Text

## Project Overview

Today I learned how to convert extracted triples into a NetworkX graph.

The process starts with text, extracts facts as Subject-Relation-Object triples, and converts those triples into nodes and edges in a directed graph.

## Concepts Learned

- Subject, Relation, Object (Triples)
- Converting triples into graph structures
- Nodes and edges
- Directed graphs
- Relationship metadata
- NetworkX graph creation
- Graph visualization
- Graph analysis

## Text to Graph Pipeline

```text
Text
  ↓
Extract Relationships
  ↓
Subject → Relation → Object
  ↓
Triples
  ↓
NetworkX Graph
  ↓
Nodes + Relationship Edges
```

## Example

Given the text:

```text
Alice works at Google.
Google develops Gemini.
Alice uses Python.
```

The extracted triples are:

```text
(Alice, works_at, Google)
(Google, develops, Gemini)
(Alice, uses, Python)
```

These triples are converted into a directed graph:

```text
Alice ──works_at──> Google
Google ──develops──> Gemini
Alice ──uses──> Python
```

## Mini-Project

I created a knowledge graph using NetworkX from a set of extracted triples.

The graph contains four entities:

- Alice
- Google
- Gemini
- Python

and three relationships:

- Alice works at Google
- Google develops Gemini
- Alice uses Python

I also visualized the graph and analyzed its nodes and relationships.

## Technologies Used

- Python
- NetworkX
- Matplotlib
- Jupyter Notebook

## Key Takeaways

- A triple consists of a Subject, Relation, and Object.
- Subjects and objects become nodes in a graph.
- Relations are stored as edges between nodes.
- Directed graphs preserve the direction of relationships.
- Multiple triples can be combined to create a knowledge graph.
- NetworkX can be used to build, visualize, and analyze graphs.
- Converting text into structured triples is an important foundation for Knowledge Graphs and Graph RAG.

**Day 25 Complete! 🚀**