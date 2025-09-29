# LangChain Web Search Agent

This project creates a custom **ReAct-style LangChain agent** that uses **GPT-4** and the **Tavily Web Search** tool to answer user queries.

## Prerequisites

* Python **3.12+**
* [Tavily API Key](https://docs.tavily.com/)
* OpenAI API Key (for GPT-4)
* [`uv`](https://github.com/astral-sh/uv) for fast dependency management (recommended)

## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/sidharth-rashwana/langchain-websearch-agent.git
cd langchain-websearch-agent
```

### 2. Create a `.env` File

```bash
touch .env
```

Add your API keys:

```env
OPENAI_API_KEY=<OPENAI-API-KEY>
LANGSMITH_TRACING=true
LANGSMITH_ENDPOINT=https://api.smith.langchain.com
LANGSMITH_API_KEY=<API-KEY>
LANGSMITH_PROJECT=<PROJECT-NAME>
TAVILY_API_KEY=<TAVILY-API-KEY>
```

### 3. Install Dependencies

Using `uv` (recommended):

```bash
uv venv
source .venv/bin/activate
uv sync
```

## Usage

Run the script and enter a question when prompted:

```bash
python main.py
```

Example:

```
What do you want to look for? What are the latest developments in fusion energy?
```

The agent will:

1. Use GPT-4 to interpret your query.
2. Search the web via Tavily.
3. Return a clean, structured summary based on your custom Pydantic schema.

## License

This project is licensed under the **MIT License**.
