# Day 08 - LangChain Basic Chain
 
## What I learned

- What LangChain is and how it helps connect components in an LLM application.
- How to create a reusable PromptTemplate.
- How to connect a PromptTemplate to a Gemini LLM.
- How the pipe operator `|` creates a chain.
- How `invoke()` runs the chain with user input.

## What I built

A simple text summarizer using LangChain and Gemini.

The user enters text, and the application sends it through a reusable prompt template and Gemini to generate a summary.

## Pipeline

User Input
→ PromptTemplate
→ Gemini LLM
→ Summary

## Key Concepts

### PromptTemplate

A reusable prompt containing placeholders such as `{text}`.

### LLM

The Gemini model that receives the formatted prompt and generates the response.

### Chain

The prompt and LLM are connected using:

`chain = prompt | llm`

### Invoke 

The chain is executed using:

`chain.invoke({"text": user_text})`

## Technologies Used

- Python
- LangChain
- Google Gemini
- PromptTemplate
