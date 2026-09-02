# Day 16: Chroma Vector DB Setup

## Objective

Store and query text embeddings locally using Chroma Vector Database.

## What I Learned

- What a vector database is
- How to create a Chroma client
- How to create a Chroma collection
- How to generate embeddings using Gemini
- How to store documents and their embeddings in Chroma
- How to perform semantic similarity search
- How vector distance is used to rank results
- Why stored and query embeddings must have matching dimensions

## Workflow

Text
↓
Gemini Embeddings
↓
3072-dimensional vectors
↓
Chroma Vector Database
↓
Store documents + embeddings
↓
Convert query into an embedding
↓
Search Chroma
↓
Retrieve similar documents

## Example Query

Query:

"I want to learn about AI"

Top matching documents included:

- I love learning artificial intelligence.
- I enjoy studying AI and machine learning.
- Python is my favorite programming language.

A different query about food was also used to verify semantic search.

## Important Debugging Lesson

Initially, Chroma created 384-dimensional embeddings automatically, while Gemini generated 3072-dimensional embeddings.

This caused a dimension mismatch error.

The issue was fixed by explicitly generating embeddings with Gemini and passing those embeddings to Chroma.

## Key Takeaways

Chroma can be used as a local vector database for storing and retrieving embeddings. Semantic search allows us to find information based on meaning rather than relying only on exact keyword matches.

**Day 16 Complete! 🚀**
