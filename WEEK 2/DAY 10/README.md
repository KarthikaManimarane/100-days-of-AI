# Day 10 - LangChain Tools

## What I learned
 
- How to turn a Python function into a LangChain tool using `@tool`.
- How tool descriptions and input schemas help the LLM understand a tool.
- How `bind_tools()` makes tools available to Gemini.
- How the LLM can decide which tool to use.
- How Python executes the selected tool and returns its result to the LLM.

## What I built

A simple tool-using assistant with a Python addition tool.

The user asks Gemini a calculation question. Gemini selects the `add` tool, LangChain executes the Python function, and the result is returned to Gemini for the final response.

## Flow

User
→ Gemini
→ Tool Call
→ LangChain Tool
→ Python Function
→ Tool Result
→ Gemini
→ Final Answer

## Key Code

```python
@tool
def add(a: int, b: int) -> int:
    """Add two numbers."""
    return a + b

llm_with_tools = llm.bind_tools([add])
