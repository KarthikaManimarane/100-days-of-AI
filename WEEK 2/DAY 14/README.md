# Day 14: Project - Email Assistant in LangGraph

## What I Built

I rebuilt the basic logic of an Email Assistant using LangGraph and Gemini.

The assistant classifies emails into three categories:

- Important
- Normal
- Spam

Based on the classification, the workflow takes a different action.

## Workflow

```text
Email
  ↓
Gemini Classification
  ↓
Conditional Routing
  ├── Important → Draft Reply
  ├── Normal → Archive
  └── Spam → Ignore
