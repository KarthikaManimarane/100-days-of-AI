# Day 20 - Metadata Filtering in Retrieval

## Objective

Learn how metadata filtering can be used to control which documents are considered during vector retrieval using Chroma.

## What I Built

I created a small Chroma collection containing four vehicle-damage-related documents.

Each document was assigned metadata describing its section:

| Document | Metadata |
|---|---|
| YOLOv10 is used for vehicle damage detection. | technology |
| The system classifies damage as minor, moderate, or severe. | severity |
| The model achieved a mAP of 88.7%. | results |
| The chatbot helps users understand vehicle damage reports. | chatbot |

## Step 1 - Create Documents and Metadata

Each document was paired with metadata:

```python
metadata = [
    {"section": "technology"},
    {"section": "severity"},
    {"section": "results"},
    {"section": "chatbot"}
]
```

The metadata acts like a tag attached to each document.

## Step 2 - Store Documents in Chroma

The documents and metadata were stored in a Chroma collection:

```python
collection.add(
    ids=[f"doc_{i}" for i in range(len(documents))],
    documents=documents,
    metadatas=metadata
)
```

## Step 3 - Retrieve Using Metadata Filtering

I used the `where` parameter to restrict retrieval to documents belonging to a specific section.

Example:

```python
results = collection.query(
    query_texts=[query],
    n_results=2,
    where={"section": "severity"}
)
```

This means Chroma searches only documents where `section = severity`.

## Experiment

I tested the question:

**What was the model performance?**

### With Metadata Filtering

The retrieval used `where={"section": "severity"}`.

Even though the question was about model performance, Chroma was restricted to the severity section.

It returned:

> The system classifies damage as minor, moderate, or severe.

This demonstrated that the metadata filter restricts which documents can participate in retrieval.

### Without Metadata Filtering

I then removed the `where` filter so Chroma could search the entire collection.

The query could then retrieve the document related to model performance.

## Retrieval Flow

### Without Filtering

Question → Semantic Search → Search All Documents → Results

### With Metadata Filtering

Question → Semantic Search + Metadata Filter → Filtered Documents → Results

## Key Takeaways

- Metadata provides additional information about stored documents.
- Chroma can filter retrieval using metadata.
- The `where` parameter controls which documents are included in a search.
- Metadata filtering can restrict semantic search to a specific category or section.
- Semantic similarity and metadata filtering can be combined.
- Metadata filtering gives more control over the retrieval process.

## Technologies Used

- Python
- Chroma
- Vector Search
- Metadata Filtering

## Conclusion

Today I learned how to use metadata filtering with Chroma to control vector retrieval. I created documents with section-based metadata and compared retrieval with and without a metadata filter.

The experiment showed that a metadata filter can prevent semantically relevant documents from other sections from being returned when they do not match the specified metadata condition.

**Day 20 Complete! 🚀**