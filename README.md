# Foundry-tutorial

A minimal example of calling a Microsoft (Azure AI) Foundry agent from Python.

## Setup

1. Create/activate the virtual environment (already created as `.venv`):
   ```bash
   # Windows (Git Bash)
   source .venv/Scripts/activate

   # Windows (PowerShell)
   .venv\Scripts\Activate.ps1
   ```
2. Install dependencies (already installed into `.venv`):
   ```bash
   pip install -r requirements.txt
   ```
3. Copy `.env.example` to `.env` (a blank `.env` is already included) and fill in:
   - `PROJECT_ENDPOINT` — your Azure AI Foundry project endpoint
   - `MODEL_DEPLOYMENT_NAME` — the deployed model to use (e.g. `gpt-4o`)
   - `AGENT_ID` — optional, leave blank to create a new agent each run
4. Authenticate with Azure, e.g. `az login`, so `DefaultAzureCredential` can pick up your credentials.

## Usage

Open `foundry_agent_demo.ipynb` in Jupyter/VS Code, select the **Python (Foundry-tutorial)** kernel, and run all cells. It creates (or reuses) an agent, sends it a message, and prints the conversation.
