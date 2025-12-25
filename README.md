_A demonstration of **prompt chaining** and **LangGraph agentic workflows** using Groq’s LLaMA models._

Python project that showcases **prompt chaining** using a state-based workflow with **LangGraph**. It takes a topic, generates a story premise, enhances it, and then applies a creative twist — each step being handled by a different prompt. The project shows how to use **graphs to chain prompts**, manage state, and control flow between nodes.

---

## 🚀 What This Project Demonstrates
| Concept | Explanation |
|---------|--------------|
| **Prompt Chaining** | Each step uses a new prompt to improve/refine previous output |
| **LangGraph** | Builds a graph with nodes that run sequentially/conditionally |
| **LLM Integration** | Uses Groq API + LLaMA 3.1 for fast inference |
| **State Management** | Data (story) flows across nodes as a dictionary |

---

## 🧠 Workflow Overview

```mermaid
graph TD
    A[Topic Input] --> B[Prompt 1: Generate Story]
    B -->|If conflict| B
    B -->|If OK| C[Prompt 2: Improve Details]
    C --> D[Prompt 3: Add Plot Twist]
    D --> E[Final Story Output]
