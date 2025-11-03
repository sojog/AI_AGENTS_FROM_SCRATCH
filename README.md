# AI Agents From Scratch

Building intelligent AI agents without any frameworks - understanding the core building blocks.

## Overview

This project demonstrates how to build AI agents from the ground up, without relying on frameworks like LangChain or AutoGPT. By understanding each building block, you'll learn how agents really work under the hood.

## The 7 Building Blocks

### 1. **Intelligence** (`1-intelligence.py`)
The foundation - connecting to a Large Language Model (LLM) to get intelligent responses.
- Basic LLM integration
- Simple prompt → response pattern
- Understanding model capabilities

### 2. **Memory** (`2-memory.py`)
Making the agent remember previous conversations.
- Conversation history management
- Context retention across multiple turns
- Building stateful interactions

### 3. **Tools** (`3-tools.py`)
Giving the agent the ability to perform actions in the real world.
- Function calling / tool use
- External API integration
- Extending agent capabilities beyond text generation

### 4. **Validation** (`4-validation.py`)
Ensuring the agent produces structured, reliable outputs.
- Schema validation
- Type checking
- Parsing and verifying LLM responses

### 5. **Control** (`5-control.py`)
Directing the agent's decision-making flow.
- Deterministic routing
- Conditional logic
- Multi-step workflows

### 6. **Recovery** (`6-recovery.py`)
Handling errors gracefully and retrying when things go wrong.
- Error detection
- Automatic retry logic
- Fallback strategies

### 7. **Feedback** (`7-feedback.py`)
Adding human-in-the-loop for critical decisions.
- Human approval workflows
- Interactive decision points
- Safety and oversight mechanisms

## Quick Start

### Prerequisites
- Python 3.8+
- Ollama installed locally

### Installation

1. **Install Ollama** (see [INSTRUCTIONS.md](INSTRUCTIONS.md) for detailed setup)
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

2. **Download a model**
```bash
ollama pull llama3.2
# or for a smaller/faster model:
ollama pull gemma3:270m
```

3. **Install Python dependencies**
```bash
pip install -r requirements.txt
```

### Running Examples

Run each building block in order to understand the progression:

```bash
python BUILDING_STEPS/1-intelligence.py
python BUILDING_STEPS/2-memory.py
python BUILDING_STEPS/3-tools.py
python BUILDING_STEPS/4-validation.py
python BUILDING_STEPS/5-control.py
python BUILDING_STEPS/6-recovery.py
python BUILDING_STEPS/7-feedback.py
```

## Why Build From Scratch?

### Understanding > Abstraction
- **Learn the fundamentals**: Frameworks hide complexity. Building from scratch reveals how agents work.
- **Debug with confidence**: When you understand the internals, fixing issues becomes easier.
- **Customize freely**: No framework constraints - build exactly what you need.

### No Black Boxes
- See exactly how prompts are constructed
- Understand token management and context windows
- Control every aspect of the agent's behavior

### Framework Independence
- Not locked into any specific framework's patterns
- Easy to migrate or integrate with any system
- Lightweight and minimal dependencies

## Architecture Philosophy

Each building block is:
- **Independent**: Can be understood and used separately
- **Composable**: Combine blocks to create more complex agents
- **Transparent**: No hidden magic, all logic is visible
- **Minimal**: Only essential code, no unnecessary abstractions

## Project Structure

```
AI_AGENTS_FROM_SCRATCH/
├── BUILDING_STEPS/
│   ├── 1-intelligence.py    # Basic LLM integration
│   ├── 2-memory.py          # Conversation memory
│   ├── 3-tools.py           # External tool calling
│   ├── 4-validation.py      # Output validation
│   ├── 5-control.py         # Flow control
│   ├── 6-recovery.py        # Error recovery
│   └── 7-feedback.py        # Human feedback
├── requirements.txt         # Python dependencies
├── INSTRUCTIONS.md          # Detailed Ollama setup
└── README.md               # This file
```

## Key Concepts

### Agent = Intelligence + Structure
An AI agent is more than just an LLM. It's:
- Intelligence (LLM responses)
- Memory (conversation context)
- Tools (ability to act)
- Control (decision logic)
- Reliability (validation & recovery)
- Safety (human oversight)

### Progressive Complexity
Start simple, add complexity only when needed:
1. Start with basic intelligence
2. Add memory when you need context
3. Add tools when you need actions
4. Add validation when you need reliability
5. Add control when you need routing
6. Add recovery when you need robustness
7. Add feedback when you need oversight

## Use Cases

This approach is perfect for:
- **Learning**: Understand how AI agents work
- **Prototyping**: Quick experiments without framework overhead
- **Custom solutions**: Build exactly what you need
- **Education**: Teaching others about agent architectures
- **Debugging**: When frameworks fail, understanding helps

## Next Steps

1. Run each example in order
2. Read the code - it's simple and commented
3. Modify and experiment
4. Combine building blocks for your use case
5. Build something amazing!

## Local & Private

Using Ollama means:
- ✅ Everything runs on your machine
- ✅ No API costs
- ✅ Complete privacy
- ✅ No rate limits
- ✅ Works offline

## Contributing

This is an educational project. Feel free to:
- Add more examples
- Improve documentation
- Share your own building blocks
- Report issues or suggest improvements

## Resources

- [Ollama Documentation](https://github.com/ollama/ollama)
- [Ollama Models Library](https://ollama.com/library)
- [Setup Instructions](INSTRUCTIONS.md)

---

**Built with ❤️ to demystify AI agents**

*No frameworks. No magic. Just code.*

