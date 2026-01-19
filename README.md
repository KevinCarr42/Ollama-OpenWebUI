# Ollama + Open WebUI Docker Setup

A Docker Compose setup for running Ollama with Open WebUI interface.

## Requirements

- Docker & Docker Compose
- NVIDIA GPU with drivers installed
- NVIDIA Container Toolkit

## Quick Start

### Start the services

```bash
docker-compose up -d
```

### Stop the services

```bash
docker-compose down
```

### Rebuild (if needed)

```bash
docker-compose build --no-cache
docker-compose up -d
```

## Accessing the UI

Open WebUI is available at: **http://localhost:3000**

## Adding New Models

1. Click on your Profile Icon / Name in the bottom-left corner of the screen.
2. Select Admin Panel.
3. Click the Settings tab on the left sidebar, then select Connections.
4. You will see a section for Ollama. Click the Manage icon (or look for the "Pull a model from Ollama.com" box).
5. Go to ollama.com/library to find a model name (e.g., llama3:8b or qwen2.5-coder:14b).
6. Paste that exact name into the text box and click the Pull Model icon (the small downward arrow).
7. A progress bar will appear showing the download status.

### Popular Models

| Model | Size | Use Case |
|-------|------|----------|
| `llama3.1:8b` | ~4.7GB | General purpose |
| `mistral:7b` | ~4.1GB | General purpose |
| `qwen2.5-coder:14b` | ~9GB | Coding |
| `deepseek-coder-v2:16b` | ~9GB | Coding |

Find more models at: https://ollama.com/library

## Data Persistence

- Models are stored in `./ollama_models`
- WebUI data is stored in a Docker volume `openwebui_data`
