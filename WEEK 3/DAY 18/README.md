# Day 18 - Basic RAG Pipeline

## Objective

Build a basic Retrieval-Augmented Generation (RAG) pipeline using a PDF document, Gemini embeddings, Chroma, and Gemini.

## What I Built

The pipeline follows this flow:

PDF → Chunks → Embeddings → Chroma → Retrieval → Gemini → Answer

## Steps

1. Loaded a PDF using `PyPDFLoader`.
2. Split the document into 48 chunks using `RecursiveCharacterTextSplitter`.
3. Generated 3072-dimensional embeddings using Gemini.
4. Stored the chunks and embeddings in a persistent Chroma vector database.
5. Converted user questions into embeddings.
6. Retrieved the most relevant chunks from Chroma.
7. Passed the retrieved context to Gemini.
8. Generated answers using only the retrieved document context.

## Technologies Used

- Python
- LangChain
- Gemini
- Gemini Embeddings
- Chroma
- PyPDF

## Example Questions

### Question 1
What are the three severity levels?

**Answer:** Minor, Moderate, Severe.

### Question 2
What are the four primary vehicle damage categories?

**Answer:** Scratches, Dents, Cracks, and Broken components.

## Key Takeaways

- RAG allows an LLM to answer questions using information from a specific document.
- Embeddings represent text as numerical vectors.
- Chroma stores and retrieves vector embeddings.
- Retrieval provides relevant context to the LLM.
- The LLM generates the final answer using the retrieved context.

## Conclusion

Today I built a complete basic RAG pipeline that connects document retrieval with Gemini generation. This is the foundation for building document question-answering systems.

**Day 18 Complete! 🚀**
