# Retrieval-Augmented Generation (RAG) Implementation

## Overview

This notebook demonstrates the implementation of a Retrieval-Augmented Generation (RAG) pipeline using OpenAI embeddings and FAISS vector database. RAG combines the retrieval of relevant documents and generative language models to enhance the accuracy and relevance of responses.

## Key Components

### 1. Document Preprocessing
- Reads PDF documents from a specified directory.
- Converts PDF files into plain text.
- Splits text into manageable chunks for embedding.

### 2. Embedding Generation
- Utilizes OpenAI's embedding model to convert text chunks into vector embeddings.

### 3. FAISS Indexing
- Stores embeddings in a FAISS vector store for efficient similarity-based retrieval.
- Enables quick retrieval of relevant document chunks based on query similarity.

### 4. RAG Querying
- Processes user queries by retrieving the most relevant document chunks.
- Utilizes OpenAI's Chat Completion API (GPT model) to generate contextually accurate answers based on retrieved chunks.

## Dependencies
- Python libraries: `openai`, `PyPDF2`, `faiss-cpu`, `numpy`

## Setup
1. Install dependencies:
```bash
pip install openai PyPDF2 faiss-cpu numpy
```

2. Set up your OpenAI API key:
```python
import openai
openai.api_key = "your-api-key"
```

## Usage
- Ensure your PDF documents are placed in the specified directory.
- Execute notebook cells sequentially to preprocess documents, create embeddings, store embeddings in FAISS, and query the system.

## Customization
- Adjust the chunk size for document splitting based on your document type.
- Fine-tune retrieval parameters or switch embedding models according to requirements.



