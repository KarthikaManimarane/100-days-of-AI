# Day 21 — RAG Chatbot on Documents

## Project Overview

Today I built a basic RAG (Retrieval-Augmented Generation) chatbot that answers questions using information from PDF documents.

The project uses Gemini for embeddings and answer generation, and Chroma as the vector database.

## What I Built

The chatbot can:

- Load PDF documents
- Extract text from PDF pages
- Split documents into smaller chunks
- Generate Gemini embeddings
- Store embeddings and document text in Chroma
- Retrieve relevant chunks for a user question
- Generate answers using Gemini
- Show the source PDF and page number

## RAG Pipeline

PDF → Text Extraction → Chunking → Gemini Embeddings → Chroma → Retrieval → Gemini → Answer

## Technologies Used

- Python
- PyPDF
- LangChain
- Gemini
- ChromaDB
- Jupyter Notebook

## Current Document

The project was tested using a Class 5 English Marigold PDF.

The document contains 32 pages and was split into 78 chunks.

## Key Learnings

- How to build a basic RAG pipeline
- How embeddings enable semantic search
- How Chroma stores and retrieves document embeddings
- How metadata can track document sources and pages
- How retrieved context can be passed to an LLM
- How to build an interactive document chatbot

## Future Improvement

The chatbot can be extended to work with 15–20 PDF documents and retrieve information across multiple documents.

**Day 21 Complete! 🚀**