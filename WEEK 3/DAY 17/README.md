# Day 17: Chunking Strategies

## Objective

Split a PDF into smaller chunks and test how different chunk sizes affect the number of chunks.

## PDF Used

AI-Based Vehicle Damage and Safety Analysis

The PDF contains 5 pages and discusses vehicle damage detection, YOLOv10, severity classification, and the Kanmani chatbot.

## What I Learned

- How to load a PDF using PyPDFLoader
- How to extract text from PDF pages
- What text chunking means
- How to use RecursiveCharacterTextSplitter
- What chunk size means
- What chunk overlap means
- How different chunk sizes affect the number of chunks

## Chunking Experiment

| Chunk Size | Chunk Overlap | Number of Chunks |
|------------|---------------|------------------|
| 200        | 20            | 129              |
| 500        | 50            | 48               |
| 1000       | 100           | 26               |

## Observations

Smaller chunk sizes produced more chunks, while larger chunk sizes produced fewer chunks.

A chunk size of 200 characters produced 129 chunks.

A chunk size of 500 characters produced 48 chunks.

A chunk size of 1000 characters produced 26 chunks.

## Chunk Overlap

Chunk overlap allows some text from one chunk to appear in the next chunk.

This helps preserve context when information is split between two chunks.

## Key Takeaways

Chunking is an important step in preparing documents for applications such as RAG.

Very small chunks may contain less context, while very large chunks may contain unnecessary information. Choosing an appropriate chunk size helps balance context and retrieval precision.

**Day 17 Complete! 🚀**
