# Day 27 — Visualizing Graphs

## Project Overview

Today I learned how to visualize a knowledge graph using Matplotlib and PyVis.

I used the NetworkX graph created from text-based relationships and explored both static and interactive graph visualization.

## Concepts Learned

- Graph visualization
- Matplotlib
- PyVis
- NetworkX graph visualization
- Directed graph visualization
- Relationship labels
- Interactive graph visualization
- Static vs interactive visualization

## Knowledge Graph

The graph represents relationships between Alice, Google, Gemini, and Python:

```text
Alice ──works_at──→ Google
Google ──develops──→ Gemini
Alice ──uses──────→ Python
```

## Matplotlib Visualization

I used Matplotlib with NetworkX to create a static visualization of the knowledge graph.

The visualization includes:

- Nodes
- Directed edges
- Node labels
- Relationship labels

Matplotlib is useful for creating simple and static graph visualizations.

## PyVis Visualization

I used PyVis to create an interactive HTML visualization of the same knowledge graph.

The interactive graph allows users to:

- Drag nodes
- Zoom in and out
- Move around the graph
- Explore relationships
- View the graph interactively

The visualization was saved as:

`knowledge_graph.html`

## Matplotlib vs PyVis

| Feature | Matplotlib | PyVis |
|---|---|---|
| Visualization | Static | Interactive |
| Move nodes | No | Yes |
| Zoom | Limited | Yes |
| Hover interaction | No | Yes |
| Relationship labels | Yes | Yes |
| Best for | Analysis & learning | Exploring knowledge graphs |

## Mini-Project

I visualized a small knowledge graph using both Matplotlib and PyVis.

The graph represents relationships between Alice, Google, Gemini, and Python.

Matplotlib was used to create a static visualization, while PyVis was used to create an interactive HTML visualization.

## Technologies Used

- Python
- NetworkX
- Matplotlib
- PyVis
- Jupyter Notebook

## Key Takeaways

- NetworkX graphs can be visualized using different Python libraries.
- Matplotlib is useful for static graph visualization.
- PyVis provides interactive graph visualization.
- Relationship labels make graph connections easier to understand.
- Interactive visualization is useful for exploring knowledge graphs.
- Knowledge graph visualization is an important part of understanding Graph RAG systems.

**Day 27 Complete! 🚀**