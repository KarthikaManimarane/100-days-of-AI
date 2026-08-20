# Day 04 - Structured Output + Pydantic

## What I learned
- Structured output makes LLM responses predictable and easier for programs to process.
- JSON is a structured data format.
- Pydantic allows us to define expected data structures and validate incoming data.
- Pydantic does not train the LLM or change its underlying knowledge.

## What I built
An AI Resume Extractor using Gemini and Pydantic.

The project takes unstructured resume text and asks Gemini to extract:
- Name
- Email
- Skills
- Education
- Experience

Gemini returns the information as structured JSON, which is then validated using a Pydantic model.

## Validation Test
I tested both valid and invalid data.

Valid data matched the Pydantic schema successfully.

For invalid data, such as providing a string where `list[str]` was expected, Pydantic raised a `ValidationError`.

## Conclusion
This project demonstrated how structured LLM output and Pydantic validation can make AI-generated data more predictable and reliable for Python applications.
