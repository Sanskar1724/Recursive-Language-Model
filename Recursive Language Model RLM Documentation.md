# Recursive Language Model (RLM) Documentation

## Overview

This project implements a simplified **Recursive Language Model (RLM)** from scratch. Instead of asking an LLM to solve a problem directly, the model is allowed to generate Python code, execute it, inspect the results, and continue reasoning until it reaches the correct answer.

The implementation closely follows the ideas presented in the RLM paper while remaining simple enough to understand in a Google Colab notebook.

---

# Architecture

```text
                  User Query
                      │
                      ▼
               RLM Agent Loop
                      │
      ┌───────────────┴───────────────┐
      ▼                               ▼
Generate Python Code           Conversation History
      │
      ▼
Execute inside REPL
      │
      ▼
Capture Output
      │
      ▼
Need More Reasoning?
      │
 ┌────┴─────┐
 │          │
Yes        No
 │          │
 ▼          ▼
llm_query() FINAL(answer)
 │
 ▼
Sub-LLM
```

---

# Components

## 1. Synthetic Dataset

A large synthetic dataset is generated to simulate long-context reasoning problems.

Purpose:

- Create thousands of records
- Hide useful information
- Produce ground-truth answers

---

## 2. Python REPL

The REPL acts as the execution environment.

Responsibilities:

- Store the long context
- Execute Python code
- Capture print output
- Store FINAL answers
- Support recursive sub-LLM calls

---

## 3. RLM Agent Loop

The agent loop controls the reasoning process.

Workflow:

1. Receive a task
2. Ask the LLM to generate Python code
3. Execute the code
4. Observe the output
5. Continue reasoning
6. Return FINAL(answer)

---

## 4. Recursive Calls

Instead of solving everything itself, the agent can delegate work.

```python
llm_query(query, sub_context)
```

The sub-agent receives only the relevant context, reducing token usage.

---

## Execution Cycle

```text
Prompt
   │
   ▼
Generate Code
   │
   ▼
Execute Code
   │
   ▼
Observe Output
   │
   ▼
Reason Again
   │
   ▼
FINAL()
```

---

# Advantages

- Better long-context reasoning
- Deterministic computation
- Lower hallucination rate
- Recursive problem decomposition
- Efficient context handling

---

# Limitations

- Slower than a single LLM call
- Requires code execution
- Depends on reliable tool access
- More implementation complexity

---

# Applications

- Large document analysis
- Data exploration
- Research assistants
- Agentic AI systems
- Code generation
- Multi-step reasoning
- Enterprise knowledge retrieval

---

# Repository Structure

```
RLM/
│
├── RLM_MODEL.ipynb
├── README.md
└── DOCUMENTATION.md
```

---

# Learning Outcomes

After completing this notebook, you will understand:

- Why long-context reasoning fails
- How Recursive Language Models work
- REPL-based reasoning
- Iterative agent loops
- Recursive sub-LLM execution
- Program-aided reasoning
- Modern agent architectures