# Day 24 — Relation Extraction

## Project Overview

Today I learned how to extract relation triples (subject, relation, object) from unstructured text using Gemini.

## Concepts Learned

- What relation extraction is
- The (subject, relation, object) triple structure
- Why direction matters in a relation (connects to directed graphs, Day 22)
- Prompting Gemini for structured triple output as JSON
- Migrating from the deprecated google.generativeai package to the new google-genai SDK
- Wrapping the flow into a reusable extract_relations(text) function

## Mini-Project

I extracted relation triples from a paragraph about Marie Curie.

**Example Output:**

- Marie Curie --discovered--> radium
- Marie Curie --worked at--> University of Paris
- Marie Curie's research --influenced--> CERN's later work on radioactivity

I then tested the reusable function on a new paragraph about Larry Page and Google.

## Technologies Used

- Python
- google-genai (new Gemini SDK)
- gemini-3.6-flash
- json module

## Key Learning

Relation triples are the missing piece after entity extraction (Day 23). Entities become nodes, relation triples become the directed edges between them. Together they form a complete pipeline for building a knowledge graph from raw text — a core building block toward my Graph RAG goal.

**Day 24 Complete! 🚀**