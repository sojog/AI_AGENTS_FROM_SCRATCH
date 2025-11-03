
# Ollama Setup Guide

This project has been updated to use **Ollama** instead of OpenAI/ChatGPT. Ollama allows you to run language models locally on your own computer.

## Installing Ollama

### macOS
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

Or download directly from [ollama.com](https://ollama.com)

### Linux
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### Windows
Download the installer from [ollama.com](https://ollama.com)

## Downloading the Model

After installing Ollama, you need to download a model. The code uses `llama3.2` by default:

```bash
ollama pull llama3.2
```

### Recommended Alternative Models

- **llama3.2** (default) - Balanced, good performance
- **gemma3:270m** - Smaller and faster
- **mistral** - Excellent alternative to llama
- **phi3** - Small but performant model

To use another model:
```bash
ollama pull mistral
```

## Starting the Ollama Server

Ollama runs as a local server on port 11434. After installation, the server should start automatically.

To check if the server is running:
```bash
curl http://localhost:11434/api/version
```

To manually start the server (if needed):
```bash
ollama serve
```

## Installing Python Dependencies

```bash
pip install -r requirements.txt
```

## Running the Examples

### 1. Intelligence (Basic intelligence)
```bash
python 1-intelligence.py
```

### 2. Memory (Conversational memory)
```bash
python 2-memory.py
```

### 3. Tools (External tools integration)
```bash
python 3-tools.py
```

### 4. Validation (Structured schema validation)
```bash
python 4-validation.py
```

### 5. Control (Deterministic flow control)
```bash
python 5-control.py
```

### 6. Recovery (Error handling and retry)
```bash
python 6-recovery.py
```

### 7. Feedback (Human approval)
```bash
python 7-feedback.py
```

## Changing the Model

All functions accept a `model` parameter to change the model used:

```python
from intelligence import basic_intelligence

# Use the default model (llama3.2)
result = basic_intelligence("What is AI?")

# Use a different model
result = basic_intelligence("What is AI?", model="mistral")
```

## Troubleshooting

### Error: Connection refused
Make sure the Ollama server is running:
```bash
ollama serve
```

### Error: Model not found
Download the model first:
```bash
ollama pull llama3.2
```

### Slow performance
- Use a smaller model: `gemma3:270m`
- Check system resources (RAM, CPU)
- Consider using GPU if available

## Differences from OpenAI

1. **Local execution**: Everything runs on your computer, no API costs
2. **Privacy**: Your data stays local
3. **Customization**: You can use various open-source models
4. **Performance**: Depends on your hardware

## Additional Resources

- [Ollama Documentation](https://github.com/ollama/ollama)
- [API Reference](https://github.com/ollama/ollama/blob/main/docs/api.md)
- [Available Models](https://ollama.com/library)


