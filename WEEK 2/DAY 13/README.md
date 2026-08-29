# Day 13: LangGraph Conditional Edges

## What I Learned

- The difference between normal edges and conditional edges.
- How conditional edges allow a graph to branch.
- How a Python routing function can decide which path to take.
- How `add_conditional_edges()` is used in LangGraph.
- How multiple branches can be created from a decision.

## What I Built

A simple LangGraph State Graph that checks whether a number is greater than 5.

If the number is greater than 5, the graph goes to the `large_number` node.

Otherwise, it goes to the `small_number` node.

## Flow

START
→ Decision
→ Large Number → END

OR

START
→ Decision
→ Small Number → END

## Examples

```text
Input: 8
8 > 5 → Large number

Input: 3
3 > 5 → Small number
