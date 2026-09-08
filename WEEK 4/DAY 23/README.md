# Day 23 — Entity Extraction with Gemini

## Project Overview

Today I learned how to extract entities (people, organizations, concepts) from unstructured text using Gemini.

## Concepts Learned

- What entity extraction (NER) is
- Designing a prompt with a fixed entity schema (PERSON, ORG, CONCEPT)
- Requesting structured JSON output from an LLM
- Cleaning Gemini's response (removing ```json code fences) before parsing
- Parsing text into Python objects with json.loads()
- Wrapping the flow into a reusable extract_entities(text) function

## Mini-Project

I extracted entities from a paragraph about Marie Curie.

**Example Output:**

- Marie Curie → PERSON
- physicist → CONCEPT
- chemist → CONCEPT
- radioactivity → CONCEPT
- University of Paris → ORG
- CERN → ORG

I then tested the reusable function on a new paragraph about Google's founders.

## Technologies Used

- Python
- google.generativeai (Gemini)
- gemini-3.6-flash
- json module

## Key Learning

Extracted entities become the nodes of a future knowledge graph, connecting directly to Day 22's graph theory. This is a core building block toward my Graph RAG goal.

**Day 23 Complete! 🚀**