# Chatbot RAG

This project is a retrieval-augmented generation (RAG) chatbot built during the IBM GenAI learning journey. It allows a user to upload a PDF document and ask questions about its content using an LLM and vector search workflow.

## Project purpose

The app demonstrates how to:

- ingest PDF documents
- split documents into chunks
- generate embeddings for semantic search
- store those embeddings in Chroma
- answer user questions using a retrieval-based LLM workflow

## Main files

- [server.py](server.py) – Flask backend serving the app interface and routes
- [worker.py](worker.py) – document processing, embeddings, vector store creation, and retrieval logic
- [server_exercise.py](server_exercise.py) – exercise/alternate version of the server logic
- [worker_huggingFace.py](worker_huggingFace.py) – Hugging Face-based worker implementation
- [Worker_completed.py](Worker_completed.py) – completed version of the worker logic
- [static/script.js](static/script.js) – frontend interaction logic
- [static/style.css](static/style.css) – styling for the app
- [templates/index.html](templates/index.html) – HTML front end

## Technologies used

- Python
- Flask
- LangChain
- Chroma
- Hugging Face Embeddings
- PyPDFLoader
- IBM watsonx / WatsonxLLM
- RetrievalQA

## How it works

1. The user uploads a PDF file.
2. The document is loaded and split into chunks.
3. Embeddings are generated for each chunk.
4. Chroma stores the vectorized document data.
5. The user asks a question.
6. The retriever finds the most relevant chunks.
7. The LLM uses those chunks to generate a grounded answer.

## Example run

```bash
pip install -r requirements.txt
python server.py
```

Then open the app in the browser and upload a PDF document to start asking questions.

## Learning outcome

This project introduced the core RAG pattern: combining document retrieval with LLM-powered answer generation for question answering over custom content.

