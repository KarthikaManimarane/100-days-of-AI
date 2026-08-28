# Day 12: LangGraph Intro - State Graph

## What I Learned

- What LangGraph is.
- What state means in a LangGraph workflow.
- What nodes are and how they update state.
- How edges define the flow between nodes.
- How `START` and `END` define the beginning and end of a graph.
- How `StateGraph` is used to build a state-based workflow.
- How `compile()` prepares the graph for execution.

## What I Built

A simple two-node LangGraph State Graph.

Node 1 changes the message to `"Hello"` and Node 2 receives that state and adds `" World"`.

## Flow

START
→ Node 1
→ Node 2
→ END

## State Flow

```text
Initial State
{"message": ""}

        ↓

Node 1
{"message": "Hello"}

        ↓

Node 2
{"message": "Hello World"}
