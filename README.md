# 🧠 Recursive Language Model (RLM) 

A hands-on implementation of a **Recursive Language Model (RLM)** built from scratch using **Python**, **OpenRouter**, and a custom **Python REPL**. This project demonstrates how Recursive Language Models overcome long-context limitations by generating, executing, and refining Python code through an iterative reasoning loop.

---

## 📖 About the Project

Traditional Large Language Models (LLMs) struggle with long-context reasoning because all information must fit within the model's context window. Recursive Language Models (RLMs) address this limitation by allowing the model to generate Python code, execute it in a REPL, observe the results, and continue reasoning until the correct answer is found.

In this project, I implemented an end-to-end RLM that stores large contexts outside the prompt, executes model-generated code, supports recursive sub-LLM calls, and iteratively solves long-context reasoning tasks.

---

## ✨ Features

- 📄 Generate large synthetic datasets for long-context evaluation
- 🐍 Custom Python REPL for code execution
- 💾 Store large context outside the LLM prompt
- ⚡ Execute LLM-generated Python code
- 📤 Capture execution outputs automatically
- 🤖 Recursive Language Model (RLM) Agent Loop
- 🔄 Recursive sub-LLM calls using `llm_query()`
- 🎯 `FINAL()` mechanism for returning answers
- 📊 Evaluate long-context reasoning performance
- 🧩 Modular and beginner-friendly implementation

---

# 📚 What I Learned

By building this project, I gained hands-on experience with:

- 🧠 Understanding the architecture and workflow of **Recursive Language Models (RLMs)**.
- 📖 Understanding why traditional **Large Language Models (LLMs)** struggle with long-context reasoning.
- 🐍 Building a custom **Python REPL (Read-Eval-Print Loop)** for executing AI-generated code.
- 💾 Managing large contexts outside the LLM prompt for efficient reasoning.
- ⚙️ Designing an iterative **Reason → Execute → Observe** agent loop.
- 🤖 Enabling LLMs to generate, execute, and refine Python code.
- 🔄 Implementing recursive sub-LLM calls using `llm_query()`.
- 📤 Capturing execution outputs and using them as feedback for further reasoning.
- 🎯 Implementing the `FINAL()` mechanism to return validated answers.
- 📊 Evaluating Recursive Language Models on long-context reasoning tasks.
- 🛠️ Building an end-to-end Recursive Language Model from scratch.
- 🚀 Understanding how code execution improves the reasoning capabilities of modern AI agents.

---

## 🏗️ Project Workflow

```text
                 User Query
                      │
                      ▼
             Recursive Language Model
                      │
          Generates Python Code
                      │
                      ▼
              Execute Inside REPL
                      │
                      ▼
             Capture Execution Output
                      │
                      ▼
          More Reasoning Required?
               │              │
             Yes              No
               │              │
               ▼              ▼
      Recursive Sub-LLM     FINAL(answer)
               │
               └──────────────► Repeat
```

---

## 🛠️ Tech Stack

- Python
- Google Colab
- OpenRouter API
- Gemini / OpenAI Compatible Models
- Python REPL
- Regular Expressions (`re`)
- JSON
- Context Managers (`contextlib`)

---

## 📂 Project Structure

```text
Recursive-Language-Model/
│
├── RLM_MODEL.ipynb          # Complete notebook implementation
├── README.md
└── Documatation

```

---

## 🎯 Key Concepts Covered

- Recursive Language Models (RLM)
- Long-Context Reasoning
- Read-Eval-Print Loop (REPL)
- Iterative Agent Loops
- Program-Aided Reasoning
- Recursive AI Agents
- Code Execution by LLMs
- Recursive Sub-Agent Calls
- Execution Feedback Loops
- Context Management

---

## 🚀 Future Improvements

- Secure sandboxed code execution
- Multi-agent collaboration
- Parallel recursive reasoning
- Memory optimization
- Support for external tools and APIs
- Visualization of the reasoning process

---

## 📚 References

- Recursive Language Models (RLM) Research Paper
- OpenRouter API Documentation
- Python Documentation

---

## ⭐ Support

If you found this project helpful, consider giving it a **⭐ Star**. It motivates me to build and share more AI, LLM, and Agentic AI projects.
