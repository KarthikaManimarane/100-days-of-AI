# Day 06 - Prompt Injection Basics

## What I learned
- Prompt injection is an attempt to manipulate an LLM through untrusted input.
- A naive prompt does not explicitly defend against instructions inside user-provided content.
- A guarded prompt tells the model to treat user-provided content as untrusted data.
- Guarded prompts can reduce risk but do not guarantee complete security.

## What I built
A small experiment comparing a naive prompt with a guarded prompt.

The same customer review contained a prompt injection attempt asking the model to reveal system instructions and confidential information.

## Result
Gemini resisted the injection in both the naive and guarded tests and continued summarizing the review.

This showed that a prompt injection is an attack attempt, not a guarantee that the model will actually follow the malicious instruction.

## Key Learning
Prompt-level defenses are useful, but they should not be treated as a complete security solution.
