# Day 07 - Smart Assistant CLI

## What I learned
- How to combine Gemini with structured JSON output.
- How Pydantic validates structured LLM output.
- How validated data can be passed to a Python function.
- How LLM applications can combine extraction, validation, and tool execution.

## What I built
A Smart Assistant CLI that accepts natural-language calendar requests.

For example:

"Meeting with Priya tomorrow at 2 PM about the project"

The assistant extracts the event details, converts them into JSON, validates them with Pydantic, and passes the validated data to a calendar function.

## Pipeline

User Request
→ Gemini
→ Structured JSON
→ Pydantic Validation
→ Calendar Function
→ Event Created

## Key Learning
The project combines structured output from Day 4 with the tool/function execution concepts from Day 5.

The calendar function is simulated in Python and does not connect to a real calendar service.
