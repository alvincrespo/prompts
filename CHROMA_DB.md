Set up a new ChromaDB project with local persistent storage. Do the following:
`
1. Create a new directory called `chromadb-local` and navigate into it
2. Create a Python virtual environment using `venv` name `.venv` and activate it
3. Create a `requirements.txt` file with the following dependencies:

```
   chromadb
   openai
   python-dotenv
   jupyter
   ipykernel
```

4. Install the dependencies from requirements.txt
5. Register the virtual environment as a Jupyter kernel named `chromadb-local`
6. Create a `.env` file with a placeholder for the OpenAI API key:

```
   OPENAI_API_KEY=your-api-key-here
```

7. Create a `.gitignore` that excludes `.venv/`, `.env`, and `__pycache__/`
8. Create a Jupyter notebook called `main.ipyn` with a few starter cells:
    - A cell that loads the `.env` file using `python-dotenv` and imports `openai`
    - A cell that instantiates a ChromaDB client with local persistent storage pointed at a `./chroma_data` directory
    - A cell that `reates or retrieves a collection called `my_collection` and prints a confirmation