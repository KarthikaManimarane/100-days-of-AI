# 100 Days of AI

A daily practice log building toward Agentic AI, LangChain/LangGraph, and RAG systems — one small concept a day, one medium project every Sunday.

**Start Date:** August 17, 2026
**Author:** Karthika Manimarane
**GitHub:** [KarthikaManimarane](https://github.com/KarthikaManimarane)
**LinkedIn:** [KarthikaManimarane](https://www.linkedin.com/in/karthikamanimarane/)
---
## Week 1: Prompting & LLM Fundamentals

| Day | Heading (for README/commit) | What to build |
|---|---|---|
| Day 01 | Zero-Shot vs Few-Shot Prompting | Same task, call Gemini both ways, compare outputs |
| Day 02 | Chain-of-Thought Prompting | Same task with/without "think step by step" |
| Day 03 | System Prompts vs User Prompts | 3 different system personas, same user input |
| Day 04 | Structured Output with Pydantic | Force Gemini to return valid JSON matching a schema |
| Day 05 | Tool Calling / Function Calling | Gemini decides when to call a calculator or weather function |
| Day 06 | Prompt Injection Basics | Naive vs guarded prompt, understand the risk |
| **Day 07** | **PROJECT: Smart Assistant CLI** | CLI tool combining structured output + tool calling (e.g., extracts calendar event details from natural text → valid JSON) |

## Week 2: Agents & LangChain

| Day | Heading | What to build |
|---|---|---|
| Day 08 | LangChain Intro — Basic Chain | First chain: prompt → LLM → output |
| Day 09 | LangChain Memory | Chatbot that remembers previous turns |
| Day 10 | LangChain Tools | Wrap a Python function as a callable tool |
| Day 11 | Agent Executor Basics | Agent picks between 2 tools |
| Day 12 | LangGraph Intro — State Graph | Simple 2-node state graph |
| Day 13 | LangGraph Conditional Edges | Agent branches based on a decision |
| **Day 14** | **PROJECT: Email Assistant in LangGraph** | Rebuild your n8n Email Assistant's logic in code |

## Week 3: Vector Databases & RAG

| Day | Heading | What to build |
|---|---|---|
| Day 15 | Embeddings Basics | Generate embeddings for 5 sentences, compare similarity |
| Day 16 | Chroma Vector DB Setup | Store and query embeddings locally |
| Day 17 | Chunking Strategies | Split a PDF into chunks, test chunk size effects |
| Day 18 | Basic RAG Pipeline | Retrieve chunks + generate an answer with Gemini |
| Day 19 | RAG Evaluation | Simple script scoring answer relevance |
| Day 20 | Metadata Filtering in Retrieval | Filter vector search by document tags |
| **Day 21** | **PROJECT: RAG Chatbot on Documents** | Working RAG chatbot over 15-20 real PDFs (foundation for Graph RAG) |

---

## Week 4: Knowledge Graphs

| Day | Heading | What to build |
|---|---|---|
| Day 22 | Graph Theory Basics for AI | NetworkX intro — nodes, edges, simple graph in Python |
| Day 23 | Entity Extraction with Gemini | Extract entities (people, orgs, concepts) from a paragraph |
| Day 24 | Relation Extraction | Extract "X → relation → Y" triples from text using Gemini |
| Day 25 | Building a Graph from Text | Convert extracted triples into a NetworkX graph |
| Day 26 | Graph Querying | Traverse the graph to answer simple questions ("who is connected to X?") |
| Day 27 | Visualizing Graphs | Use matplotlib/pyvis to visualize your knowledge graph |
| **Day 28** | **PROJECT: Knowledge Graph from a Document Set** | Build a full KG from 10-15 documents (your syllabus or a topic set) |

## Week 5: Graph RAG (Hybrid Retrieval)

| Day | Heading | What to build |
|---|---|---|
| Day 29 | Combining Vector + Graph Retrieval | Design: when to use vector search vs graph traversal |
| Day 30 | Query Routing | Script that decides which retrieval method fits a given question |
| Day 31 | Graph-Augmented Answers | Pull graph context into a Gemini prompt alongside vector chunks |
| Day 32 | Multi-hop Reasoning | Answer a question requiring 2+ graph hops |
| Day 33 | Combining Sources in One Prompt | Merge vector + graph context cleanly for generation |
| Day 34 | Testing Edge Cases | Try queries that break naive RAG but work with graph context |
| **Day 35** | **PROJECT: Multi-Modal Graph RAG v1** | This is your actual resume project — get a working end-to-end version live |

## Week 6: Multi-Agent Systems

| Day | Heading | What to build |
|---|---|---|
| Day 36 | Multi-Agent Concepts | Read/understand researcher-writer-critic style patterns |
| Day 37 | LangGraph Multi-Node Graphs | 3+ node graph with distinct agent roles |
| Day 38 | Agent Communication | Pass state/messages between two agents |
| Day 39 | Supervisor Pattern | One agent routes tasks to sub-agents |
| Day 40 | Error Handling in Agent Chains | Retry/fallback logic when a step fails |
| Day 41 | Human-in-the-loop Pattern | Agent pauses for approval before an action |
| **Day 42** | **PROJECT: Researcher + Writer Multi-Agent System** | Two agents collaborate on a small research-and-summarize task |

## Week 7: Tool Use & Protocols

| Day | Heading | What to build |
|---|---|---|
| Day 43 | API Integration Patterns | Wrap a public API (weather, news) as an agent tool |
| Day 44 | Model Context Protocol (MCP) Basics | Read the spec, understand tool/resource concepts |
| Day 45 | Building a Simple MCP-style Wrapper | Basic tool-exposure wrapper in Python |
| Day 46 | Webhook-triggered Agents | Agent that reacts to an incoming webhook payload |
| Day 47 | Rate Limiting & Retries | Add resilience to your API-calling agent |
| Day 48 | Authentication Patterns (OAuth basics) | Understand token-based auth for real APIs |
| **Day 49** | **PROJECT: Multi-Tool Agent** | Agent with 3+ tools (API + calculator + search) choosing the right one per query |

## Week 8: Evaluation & Observability

| Day | Heading | What to build |
|---|---|---|
| Day 50 | Why Evaluate LLM Systems | Read on hallucination, relevance, faithfulness metrics |
| Day 51 | Building a Test Set | Create 10-15 labeled Q&A pairs for your RAG system |
| Day 52 | Simple Scoring Script | Score answers against expected outputs |
| Day 53 | LangSmith or Manual Tracing | Log agent steps for debugging |
| Day 54 | Cost & Latency Tracking | Measure token usage and response time per query |
| Day 55 | Comparing Model Choices | Run same task on 2 different models, compare cost/quality |
| **Day 56** | **PROJECT: Evaluation Pipeline for Your Graph RAG** | Add a real eval suite to your Week 5 project |

## Week 9: Autonomous Agents (Competitor Monitoring)

| Day | Heading | What to build |
|---|---|---|
| Day 57 | Web Scraping Basics | Pull data from a public webpage with Python |
| Day 58 | Structured Extraction from Scraped Data | Use Gemini to extract structured info from raw scraped text |
| Day 59 | Change Detection | Detect what changed between two scrapes of the same page |
| Day 60 | Summarization for Reports | Summarize multiple sources into one digest |
| Day 61 | Scheduling Basics | Run a script on a schedule (cron or Python scheduler) |
| Day 62 | Alerting | Send a Slack/email alert when something notable is found |
| **Day 63** | **PROJECT: Autonomous Competitor Agent v1** | Your second resume project — first working version live |

## Week 10: Extending the Competitor Agent

| Day | Heading | What to build |
|---|---|---|
| Day 64 | Multi-Source Monitoring | Track 2-3 competitor sources instead of one |
| Day 65 | Sentiment/Signal Scoring | Score how "significant" a detected change is |
| Day 66 | Historical Tracking | Store past results, compare trends over time |
| Day 67 | Report Generation | Auto-generate a formatted weekly report |
| Day 68 | Dashboard Basics | Simple Flask page showing latest findings |
| Day 69 | Edge Case Testing | Handle broken pages, empty results gracefully |
| **Day 70** | **PROJECT: Competitor Agent v2 (Polished)** | Full pipeline: monitor → analyze → report → alert |

## Week 11: Deployment Fundamentals

| Day | Heading | What to build |
|---|---|---|
| Day 71 | Docker Basics | Write a Dockerfile for one of your existing projects |
| Day 72 | Containerizing a Flask App | Package your KANMANI app in Docker |
| Day 73 | Environment Variables & Secrets | Manage API keys safely, not hardcoded |
| Day 74 | FastAPI Basics | Rebuild one small tool as a FastAPI endpoint |
| Day 75 | API Documentation | Add Swagger/OpenAPI docs to your FastAPI app |
| Day 76 | Local Deployment Testing | Run your containerized app end-to-end locally |
| **Day 77** | **PROJECT: Containerize & Deploy One Agent** | Take any prior project, fully Dockerized and documented |

## Week 12: Cloud Basics

| Day | Heading | What to build |
|---|---|---|
| Day 78 | Cloud Concepts Refresher | Revisit your AWS Academy basics — S3, EC2, Lambda |
| Day 79 | Deploying a Simple App to the Cloud | Host a basic script/app on a free-tier cloud service |
| Day 80 | Cloud Storage for Documents | Store your RAG document set in cloud storage |
| Day 81 | Environment Config for Cloud | Manage secrets/config for a cloud-hosted app |
| Day 82 | Basic Monitoring | Check logs/uptime for your deployed app |
| Day 83 | Cost Awareness | Understand free-tier limits so nothing surprises you |
| **Day 84** | **PROJECT: Deploy Your RAG Chatbot to the Cloud** | A live, shareable link for your Graph RAG project |

## Week 13: Advanced Agent Patterns

| Day | Heading | What to build |
|---|---|---|
| Day 85 | Streaming Responses | Build a chatbot that streams tokens instead of waiting for full output |
| Day 86 | Caching for LLM Calls | Add a simple cache layer to avoid redundant API calls |
| Day 87 | Parallel Tool Calls | Agent that calls 2 tools simultaneously, merges results |
| Day 88 | Self-Correcting Agents | Agent that checks its own output and retries if wrong |
| Day 89 | Long-Context Handling | Summarize/compress context when input exceeds a token limit |
| Day 90 | Guardrails & Input Validation | Add Pydantic-based validation to reject bad agent inputs |
| **Day 91** | **PROJECT: Self-Correcting Research Agent** | Agent that answers, checks its own answer against sources, and retries if unsupported |

## Week 14: Applied Mini-Projects

| Day | Heading | What to build |
|---|---|---|
| Day 92 | Resume Screener Agent | Small agent that scores a resume against a JD (very on-theme for you) |
| Day 93 | Interview Question Generator | Agent that generates likely interview questions from a JD |
| Day 94 | Job Description Summarizer | Agent that extracts must-have vs nice-to-have skills from any JD |
| Day 95 | Personal Study Tracker Bot | Agent that logs and summarizes your own daily learning (meta, but useful) |
| Day 96 | Voice-to-Text Mini Agent | Use Whisper (you already know this) + Gemini to build a voice note summarizer |
| Day 97 | Multi-Language Support | Add French/Tamil response support to any earlier agent, using your language skills |
| **Day 98** | **PROJECT: Personal Job-Hunt Copilot** | Combines Day 92-94 into one tool: paste a JD, get skill-match score + likely questions |

## Days 99–100: Final Builds

| Day | Heading | What to build |
|---|---|---|
| Day 99 | Slack Bot Integration | Wrap any earlier agent as a Slack bot (ties back to your Lead Qualification project) |
| **Day 100** | **PROJECT: Capstone — Combine Two Prior Agents** | Pick your 2 favorite agents from the last 99 days and combine them into one larger system |

---
