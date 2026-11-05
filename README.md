# Learn LangChain

A hands-on learning project for exploring LangChain and LLM application development with Python and Jupyter notebooks.

The notebooks build concepts step by step, starting with basic model calls and progressing to tools, structured output, middleware, and human-in-the-loop workflows.

## Topics covered

- Chat model integration with OpenAI, Groq, and Google Gemini
- Streaming model responses
- Tools and tool calling
- LangChain messages and conversation state
- Structured output with `TypedDict` and Pydantic
- Agent middleware
- Human-in-the-loop approval workflows
- Environment variables and API key management

## Project structure

```text
src/learn_langchain/
├── 1-langchainintro.ipynb     # Introduction to LangChain agents
├── 2-modelIntegration.ipynb   # OpenAI, Groq, and Gemini models
├── 3-streaming.ipynb          # Streaming responses
├── 4-tools.ipynb              # Tool definitions and tool calling
├── 5-messages.ipynb           # LangChain message types
├── 6-structuredOutput.ipynb   # TypedDict and Pydantic schemas
├── 7-middleware.ipynb         # Agent middleware
└── 8-humanInLoop.ipynb        # Human approval workflows
```

## Requirements

- Python 3.14 or newer
- [`uv`](https://docs.astral.sh/uv/)
- API keys for the providers you want to use

## Setup

Clone the repository and enter the project directory:

```bash
git clone <your-repository-url>
cd Learn-Langchain
```

Create the virtual environment and install the project dependencies:

```bash
uv sync
source .venv/bin/activate
```

Register the environment as a Jupyter kernel if needed:

```bash
python -m ipykernel install --user \
  --name learn-langchain \
  --display-name "Learn-LangChain"
```

Open the notebooks in VS Code or Jupyter and select the `Learn-LangChain` kernel.

## Environment variables

Create a `.env` file in the project root. Add only the providers you intend to use:

```env
OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key
```

Never commit `.env` or API keys. The repository's `.gitignore` excludes environment files and virtual environments.

## Running the notebooks

From the project root:

```bash
source .venv/bin/activate
jupyter notebook
```

Run notebook cells from top to bottom after starting or restarting the kernel. Earlier cells usually define imports, environment variables, models, and tools used by later cells.

## Dependency management

This project uses `uv` and commits `uv.lock` so that dependencies can be reproduced consistently.

Add a dependency with:

```bash
uv add package-name
```

Update the environment after dependency changes with:

```bash
uv sync
```

## Notes

This is an educational project. The tools and integrations are intended for learning and experimentation; review generated output and do not use example tools for real-world actions without adding appropriate authentication, validation, logging, and approval controls.

## License

This project is for personal learning and experimentation. Add a license before distributing it publicly.
