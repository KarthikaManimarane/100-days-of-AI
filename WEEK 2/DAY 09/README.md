# Day 09 - LangChain Memory Chatbot
 
## What I learned

- Conversation history allows an LLM application to use previous turns.
- `HumanMessage` represents user messages.
- `AIMessage` represents AI responses.
- A history list can store the conversation between the user and AI.
- The stored history is passed back to the LLM with each new message.

## What I built

An interactive chatbot using LangChain and Gemini that remembers previous turns in the conversation.

The chatbot stores each user message and AI response in a history list and sends that history to Gemini when generating the next response.

## Conversation Flow

User Message
→ Add to History
→ Gemini receives History
→ AI Response
→ Add AI Response to History
→ Continue Conversation

## Key Code

```python
history.append(HumanMessage(content=user_message))

response = llm.invoke(history)

ai_text = response.content[0]["text"]

history.append(AIMessage(content=ai_text))
