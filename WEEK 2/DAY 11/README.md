# Day 11: Agent Executor Basics

## What I Learned

- What an agent is in an LLM application.
- How an agent can decide when to use a tool.
- How an agent works together with tools and an LLM.
- How `create_agent()` creates an agent that manages the tool-calling loop.
- How the tool result is returned to the LLM to generate the final answer.

## What I Built

A simple calculator agent using Gemini and a LangChain `add` tool.

The user asks a calculation question. The agent decides to use the `add` tool, the tool executes the calculation, and the result is returned to Gemini for the final response.

## Flow

User
→ Agent
→ Gemini decides to use tool
→ Add Tool
→ Tool Result
→ Gemini
→ Final Answer

## Key Code

```python
@tool
def add(a: int, b: int) -> int:
    """Add two numbers."""
    return a + b

agent = create_agent(
    model=llm,
    tools=[add],
    system_prompt="You are a helpful calculator assistant. Use the add tool when needed."
)
