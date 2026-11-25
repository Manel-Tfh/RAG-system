# Simple RAG System for PDF Question Answering

A Retrieval-Augmented Generation (RAG) system that allows users to ask questions about PDF documents and receive answers based on the information retrieved from those documents.

The project combines semantic search with a Large Language Model (LLM) to generate context-aware answers while providing source references.

## Project Overview

Traditional language models may generate answers without having access to the specific documents a user wants to consult.

This project addresses that limitation by implementing a RAG pipeline:

1. Extract text from PDF documents.
2. Divide the extracted text into smaller chunks.
3. Generate vector embeddings for each chunk.
4. Store the embeddings in a FAISS vector index.
5. Retrieve the most relevant chunks when a question is asked.
6. Provide the retrieved context to an LLM to generate an answer.

## Architecture

**PDF Documents → Text Extraction → Text Chunking → Embeddings → FAISS Vector Search → Context Retrieval → Qwen LLM → Answer**

## Technologies Used

- **Python** — Main programming language.
- **PyMuPDF** — PDF text extraction.
- **Sentence Transformers** — Text embedding generation.
- **FAISS** — Efficient similarity search.
- **Qwen2.5-3B-Instruct** — Language model for answer generation.
- **Hugging Face Transformers** — Model loading and inference.
- **Gradio** — Interactive user interface.
- **Google Colab** — Development and execution environment.

## Models

**Embedding model**

`paraphrase-multilingual-MiniLM-L12-v2`

Used to convert text chunks and user questions into vector representations.

**Language model**

`Qwen/Qwen2.5-3B-Instruct`

Used to generate answers based on the retrieved document context.

## How to Run

The project is designed to run in Google Colab.

1. Open `SimpleRAG.ipynb` in Google Colab.
2. Upload your PDF documents into the notebook's expected `documents` directory.
3. Run the notebook cells in order.
4. Allow the notebook to extract and process the PDF content.
5. Wait for the embedding and FAISS index creation.
6. Load the language model.
7. Launch the Gradio interface.
8. Ask questions about your uploaded documents.

**Note:** The original notebook uses CUDA for embedding generation. A GPU-enabled runtime is therefore recommended.

## Main Features

- PDF document ingestion.
- Automatic text extraction.
- Text chunking with overlapping sections.
- Semantic vector embeddings.
- Similarity-based document retrieval.
- Context-based answer generation.
- Source and page information for retrieved content.
- Interactive Gradio interface.

## Repository Structure

```text
Simple-RAG-System/
│
├── SimpleRAG.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## Future Improvements

- Support multiple document formats.
- Improve document chunking strategies.
- Experiment with different embedding models.
- Compare retrieval strategies.
- Evaluate answer quality and retrieval accuracy.
- Improve the user interface.

## Author

TEFFAHI MANEL ZINEB

## Project Type

Academic / Personal Project — Retrieval-Augmented Generation (RAG)
