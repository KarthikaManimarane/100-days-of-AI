# Day 26 — Graph Querying

## Project Overview

Today I learned how to query and traverse a NetworkX graph to answer simple questions about entities and their relationships.

I learned how to find connected nodes, retrieve relationships, and find paths between entities.

## Concepts Learned

- Graph querying
- Graph traversal
- Direct connections
- Successor nodes
- Relationship queries
- Shortest paths
- Checking whether a path exists
- Reusable graph query functions

## Example Graph

```text
Alice ──works_at──> Google
Google ──develops──> Gemini
Alice ──uses──────> Python
```

## Graph Queries

I used NetworkX to answer questions such as:

- Who is connected to Alice?
- What does Alice use?
- What does Google develop?
- Is there a path from Alice to Gemini?

For example, the direct connections of Alice are:

```text
Google
Python
```

The shortest path from Alice to Gemini is:

```text
Alice → Google → Gemini
```

## Mini-Project

I created a simple graph query system using NetworkX.

The system can find connected nodes, search for specific relationships, and traverse the graph to find paths between entities.

## Technologies Used

- Python
- NetworkX
- Jupyter Notebook

## Key Takeaways

- Graphs can be queried to retrieve useful information.
- Successors can be used to find directly connected nodes in a directed graph.
- Graph traversal allows us to move from one entity to another.
- Shortest paths can reveal how entities are connected.
- Reusable functions make graph queries easier to perform.
- Graph querying is an important foundation for Knowledge Graphs and Graph RAG.

**Day 26 Complete! 🚀**