# Day 05 - Tool / Function Calling

## What I learned
- Tool calling allows an LLM to request that an external function be executed.
- Gemini can decide when a tool is needed and provide the required arguments.
- The Python application executes the actual function.
- The tool result is returned to Gemini.
- Gemini can then use that result to generate the final response.

## What I built
A Tool Calling Calculator using Gemini and Python.

The calculator supports:
- Addition
- Subtraction
- Multiplication
- Division

I gave Gemini access to the calculator function and asked:
"What is 25 multiplied by 12?"

Gemini requested the calculator with the required arguments, Python executed the function, and the result was returned to Gemini.

## Tool Calling Flow

User → Gemini → Tool Request → Python Function → Tool Result → Gemini → Final Answer

## Key Learning
Gemini does not directly execute the Python function. It requests the tool call, while the Python application executes the function and returns the result.
