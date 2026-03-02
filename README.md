# NPFL087 2026 — DSPy notebook setup

This repository contains a Jupyter notebook in [notebooks/01_DSPy_Intro.ipynb](notebooks/01_DSPy_Intro.ipynb).

## Prerequisites

- [uv](https://docs.astral.sh/uv/getting-started/installation/)
- VS Code with:
	- **Python** extension
	- **Jupyter** extension

## Install dependencies with uv

From the repository root:

```bash
uv sync
```

This creates a local virtual environment and installs all dependencies from `pyproject.toml`.

## Run the notebook in VS Code

1. Open this folder in VS Code.
2. Open [notebooks/01_DSPy_Intro.ipynb](notebooks/01_DSPy_Intro.ipynb).
3. Select the kernel from this project environment:
	 - Use **Python: Select Interpreter** and choose `.venv` created by `uv sync`.
	 - In the notebook kernel picker, select the same interpreter.
4. Run cells from top to bottom.

Optional (if you want to start a local Jupyter server manually):

```bash
uv run jupyter lab
```

## Google Colab alternative

You can also run the notebook in Google Colab:

1. Upload [notebooks/01_DSPy_Intro.ipynb](notebooks/01_DSPy_Intro.ipynb) to Colab.
2. Install required packages in a first Colab cell (uncomment it):

```python
!pip install dspy cytoolz pandas rich sacrebleu tqdm zstandard
```

3. Upload any required local data files (for example files from `data/`) to the Colab runtime, or mount Google Drive and adjust paths.

> Note: Colab runtime is ephemeral, so packages and uploaded files are reset when the session restarts.
