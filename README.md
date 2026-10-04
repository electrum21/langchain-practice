# Introduction to LangChain

This repository contains my notes, experiments, and modified examples from the LangChain Academy **Introduction to LangChain** course. It is primarily a collection of Jupyter notebooks covering the progression from basic LangChain concepts to more advanced, production-oriented agent patterns.

## Original Repository and Acknowledgements

This project is based on the [LangChain Academy Introduction to LangChain repository](https://github.com/langchain-ai/lca-lc-foundations) and its accompanying [Introduction to LangChain course](https://academy.langchain.com/courses/foundation-introduction-to-langchain-python).

The original repository provided the course structure, example notebooks, exercises, and project ideas used as the foundation for this work. The concepts and teaching materials remain the work of the LangChain team. Many thanks to them for making these materials available for learning and experimentation.

## Why I Created This Version

The original course examples are designed around models from OpenAI and Anthropic. I wanted to work through the material without needing a paid OpenAI or Anthropic subscription, so I adapted the examples to use a Gemini model available through Google's free tier.

This repository is therefore not a separate implementation of LangChain. It is my learning-focused adaptation of the original course material, with provider-specific model changes and personal explanations added to make the notebooks easier for me to understand and revisit.

## Model Provider Modifications

I replaced the OpenAI- and Anthropic-specific model usage where necessary with Gemini-based model calls. This included updating model initialization, imports, and related examples so that the same LangChain and LangGraph concepts could be demonstrated with a different provider.

The goal of these changes was to keep the behavior and learning objectives of the examples as close as possible to the original while removing the requirement for an OpenAI or Anthropic subscription. Some provider-specific behavior can differ between models, especially around structured output, tool calling, multimodal inputs, and response formatting. The notebooks reflect the adjustments needed for the Gemini-based setup.

The repository may still use other services where they are part of a particular example, such as search, tracing, or external tools. The main language-model dependency, however, was changed to Gemini for my experiments.

## Course Modules and Projects

### Module 1: Creating Agents

The first module introduces the building blocks used to create LangChain agents:

- Foundational chat models and model invocation
- Prompt templates and message handling
- Tool definitions and tool calling
- Web search and external tool integration
- Short-term memory and conversation state
- Multimodal messages and image input
- A personal chef agent project combining models, tools, and memory

These notebooks helped me understand how an agent receives a request, decides when a tool is needed, uses the tool result, and produces a final response.

### Module 2: Advanced Agents

The second module focuses on the context and coordination required by more capable agents:

- Model Context Protocol (MCP)
- Connecting agents to an MCP server
- Runtime context and dependency access
- State management
- Multi-agent system design
- A wedding planner project that coordinates specialized agents
- Bonus examples using retrieval-augmented generation (RAG)
- A bonus SQL agent example

The notes in this module focus on how information moves through an agent system, how state differs from runtime context, and how separate agents can be combined around a larger task.

### Module 3: Production-Ready Agents

The third module explores patterns for making agents more useful in realistic applications:

- Middleware and agent customization
- Managing long conversations and message history
- Human-in-the-loop workflows
- Dynamic models
- Dynamic prompts
- Dynamic tools
- An email assistant project
- An Agent Chat UI example

These notebooks helped me understand how an agent can be controlled, interrupted, extended, and adapted at runtime instead of relying on a single fixed prompt and model configuration.

## What I Learned

I wrote personal notes across the notebooks in all three modules rather than keeping the repository as a collection of unchanged course examples. The notes explain both the code and the ideas behind it, including:

- How LangChain represents messages, prompts, model responses, and tool calls
- How agents decide between responding directly and invoking tools
- How short-term memory and graph state support multi-step conversations
- How multimodal inputs can be passed to a model
- How MCP makes tools and resources available through a common protocol
- How runtime context can provide dependencies without placing everything in agent state
- How multiple specialized agents can be coordinated to solve one task
- How middleware can intercept and customize agent execution
- How to manage long message histories and control context size
- How human approval can be inserted into an agent workflow
- How prompts, models, and tools can be selected dynamically
- How LangGraph supports durable, stateful agent workflows

The notebooks are intended to show the reasoning behind the examples, not just their final output. My notes capture questions, observations, and explanations that I found useful while learning each concept.

## Personal Notes

I also made personal notes while watching the KodeKloud videos and completing the KodeKloud labs. These notes are available in the [`notes/`](C:/Users/tjmja/Documents/Projects/langchain-practice/notes) folder and can be previewed as HTML here:

- [LangChain notes](https://htmlpreview.github.io/?https://github.com/electrum21/langchain-practice/blob/main/notes/langchain-notes.html)
- [LangGraph notes](https://htmlpreview.github.io/?https://github.com/electrum21/langchain-practice/blob/main/notes/langgraph-notes.html)

## Repository Structure

The main learning material is organized by module:

```text
notebooks/
├── module-1/
│   ├── foundational models, prompting, tools, memory
│   └── multimodal messages and personal chef project
├── module-2/
│   ├── MCP, runtime context, state, and multi-agent systems
│   └── wedding planner, RAG, and SQL examples
└── module-3/
    ├── message management, HITL, middleware, and dynamic agents
    └── email assistant and Agent Chat UI
```

Overall, this repository serves as a record of my progress through the course, the changes required to use Gemini's free tier, and the notes I made while learning how LangChain and LangGraph can be used to build agentic applications.
