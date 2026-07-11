# Agentic AI for DevOps

A simple AI agent that answers Docker and Kubernetes questions by executing real system commands.

The project uses **LangChain** for tool calling and **Ollama** to run a local LLM. Instead of hallucinating infrastructure data, the agent retrieves live information using `docker` and `kubectl`.

---

## Architecture

<p align="center">
  <img src="docs/architecture.png" alt="Architecture" width="900">
</p>

---

## Features

- Query running Docker containers
- Query Kubernetes pods
- Local LLM using Ollama
- LangChain tool calling
- No external API required
- Runs completely on your machine

---

## Tech Stack

- Python
- LangChain
- Ollama
- Docker
- Kubernetes
- kubectl

---

## Project Structure

```text
.
├── agent.py
├── requirements.txt
├── README.md
└── docs
    └── architecture.png
```

---

## Prerequisites

- Python 3.10+
- Docker
- kubectl
- Ollama

---

## Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/agentic-ai-devops.git

cd agentic-ai-devops
```

Create a virtual environment

```bash
python -m venv venv
```

Activate it

**Windows**

```bash
venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Pull a Model

Start Ollama

```bash
ollama serve
```

Download the model

```bash
ollama pull qwen3-coder:30b
```

You can also use smaller models such as

- qwen3:8b
- qwen2.5:7b
- llama3.2

Just update the model name inside `agent.py`.

---

## Run

```bash
python agent.py
```

---

## Example

```
Ask your Kubernetes Agent a Question:

> show me all pods

> how many docker containers are running?

> list all running containers

> show pods from all namespaces
```

---

## Available Tools

### Docker

```bash
docker ps
```

### Kubernetes

```bash
kubectl get pods -A
```

The LLM decides which tool to execute based on the user's question.

---

## Repository Layout

```text
agent.py
requirements.txt
README.md
```

---

## Future Improvements

- Docker images
- Docker logs
- Kubernetes deployments
- Kubernetes services
- Helm support
- Jenkins integration
- Terraform integration
- AWS support

---

If you have any suggestions or improvements, feel free to open an issue or submit a pull request.
