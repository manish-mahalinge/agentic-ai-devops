# Agentic AI for DevOps

An AI-powered DevOps assistant built with **LangChain** and **Ollama** that answers Docker and Kubernetes questions by executing real system commands through tool calling.

## Architecture

<p align="center">
  <img src="docs/architecture.png" alt="Architecture">
</p>

---

## Tech Stack

- Python
- LangChain
- Ollama
- Docker
- Kubernetes

---

## Features

- Query running Docker containers
- Query Kubernetes pods
- Local LLM using Ollama
- Intelligent tool calling
- Runs completely locally

---

## Project Structure

```text
.
├── agent.py
├── requirements.txt
├── README.md
└── docs/
    └── architecture.png
```

---

## Installation

```bash
git clone https://github.com/<your-username>/agentic-ai-devops.git

cd agentic-ai-devops

python -m venv venv

# Windows
venv\Scripts\activate

# Linux/macOS
source venv/bin/activate

pip install -r requirements.txt

ollama pull qwen3-coder:30b

python agent.py
```

---

## Example

```text
> Show all Kubernetes pods

> How many Docker containers are running?

> List all running Docker containers
```

---

## Demo

<p align="center">
  <img src="docs/demo.gif" alt="Demo">
</p>
