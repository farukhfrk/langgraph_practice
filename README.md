# LangGraph Practice Repository

A comprehensive practice repository for learning LangGraph, a framework for building stateful, multi-actor applications with LLMs.

## 📚 Overview

This repository contains practice notebooks demonstrating various LangGraph concepts and workflows:

- **0_test_installation.ipynb** - Verifies LangGraph and LangChain installation
- **1_bmi_workflow.ipynb** - Simple state graph workflow calculating BMI and categorizing health status
- **2_simple_llm_workflow.ipynb** - Basic LLM integration with LangGraph for question-answering
- **3_prompt_chaining.ipynb** - Advanced workflow for prompt chaining (outline → blog post → summary)

## 🚀 Getting Started

### Prerequisites

- Python 3.9 or higher
- OpenAI API key (for LLM-based workflows)
- pip package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone git@github.com:farukhfrk/langgraph_practice.git
   cd langgraph_practice
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv myenv
   ```

3. **Activate the virtual environment**
   
   On Windows:
   ```bash
   myenv\Scripts\activate
   ```
   
   On macOS/Linux:
   ```bash
   source myenv/bin/activate
   ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Configure environment variables**
   ```bash
   cp .env.example .env
   # Edit .env and add your OpenAI API key
   ```

## 📓 Notebooks Explained

### 0. Test Installation
Verifies that LangGraph and LangChain are properly installed.
```bash
jupyter notebook 0_test_installation.ipynb
```

### 1. BMI Workflow
A simple state machine that:
- Accepts weight and height as inputs
- Calculates BMI using a computational node
- Categorizes health status (Underweight, Normal, Overweight, Obesity)
- Demonstrates graph visualization

```bash
jupyter notebook 1_bmi_workflow.ipynb
```

### 2. Simple LLM Workflow
A basic LLM integration demonstrating:
- Loading environment variables
- Creating a ChatOpenAI model
- Building a simple workflow with LLM as a node
- Asking questions to the LLM

```bash
jupyter notebook 2_simple_llm_workflow.ipynb
```

### 3. Prompt Chaining
An advanced workflow showing:
- Creating an outline for a blog post
- Generating a full blog post from the outline
- Summarizing the generated blog post
- Multi-step LLM prompt chaining

```bash
jupyter notebook 3_prompt_chaining.ipynb
```

## 🔧 Key Concepts Covered

### State Management
- TypedDict for defining state schemas
- State persistence across workflow steps

### Graph Construction
- StateGraph for building directed acyclic graphs
- Nodes and edges definition
- START and END markers

### LLM Integration
- ChatOpenAI model initialization
- Prompt formatting
- Response extraction

### Workflow Execution
- Graph compilation
- Initial state setup
- Workflow invocation
- Output state retrieval

## 📦 Dependencies

Key packages used:
- **langgraph**: Workflow orchestration framework
- **langchain**: LLM interaction library
- **langchain-openai**: OpenAI integration for LangChain
- **python-dotenv**: Environment variable management
- **ipython**: Interactive notebook environment
- **jupyter**: Notebook server

See `requirements.txt` for complete dependency list.

## 🛠️ Development

### Adding New Workflows

1. Create a new notebook: `N_workflow_name.ipynb`
2. Import required libraries:
   ```python
   from langgraph.graph import StateGraph, START, END
   from langchain_openai import ChatOpenAI
   from typing import TypedDict
   ```
3. Define your state schema as a TypedDict
4. Create workflow nodes as functions
5. Build and compile the graph
6. Test with sample data

### Best Practices

- Always use TypedDict for type hints
- Add comments explaining each node's purpose
- Test workflows with sample data before integration
- Use graph visualization for debugging
- Handle errors gracefully in production

## 📝 Notes

- Ensure your OpenAI API key is set in the `.env` file
- Do not commit `.env` file to version control
- Each notebook can be run independently
- Outputs may vary based on LLM responses

## 🎓 Learning Resources

- [LangGraph Documentation](https://langgraph.dev/)
- [LangChain Documentation](https://python.langchain.com/)
- [OpenAI API Reference](https://platform.openai.com/docs/api-reference)

## 📄 License

This project is created for educational purposes.

## 🤝 Contributing

Feel free to fork this repository and add more LangGraph examples!

---

**Created**: June 2026  
**Status**: Practice/Educational Repository
