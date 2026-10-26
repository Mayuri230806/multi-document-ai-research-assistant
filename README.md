# Multi-Document AI Research Assistant

An AI-powered research assistant built using **Retrieval-Augmented Generation (RAG)** that allows users to upload multiple documents and ask questions across them. The system retrieves relevant information from the uploaded documents and generates evidence-based answers with source references.

## Overview

Researching information across multiple PDFs and text documents can be time-consuming. This project aims to simplify the process by providing a single interface where users can upload documents, ask questions, and receive answers grounded in their own data.

The application uses a RAG pipeline to retrieve relevant document passages before passing them to a Large Language Model (LLM) for answer generation.

## Key Features

- **Multi-Document Support:** Upload PDF, Markdown, and TXT files.
- **Document Ingestion:** Extract text and preserve document metadata.
- **Text Chunking:** Split documents into smaller, overlapping text chunks.
- **Embedding Generation:** Convert text chunks into numerical vectors.
- **Semantic Search:** Retrieve relevant passages based on the meaning of a query.
- **Vector Database:** Store and search document embeddings using ChromaDB.
- **Context-Aware Answers:** Generate answers using retrieved document evidence.
- **Source Citations:** Display source filenames, PDF page numbers when available, and supporting text.
- **Hallucination Reduction:** Encourage evidence-based answers and indicate when sufficient information cannot be found.

*Features will be marked complete as they are implemented and tested.*

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | Web application interface |
| PyMuPDF | PDF text extraction |
| LangChain Text Splitters | Text chunking |
| Sentence Transformers | Embedding generation |
| ChromaDB | Vector storage and retrieval |
| Ollama | Local LLM integration |

## RAG Architecture

The application follows this pipeline:

1. **Document Ingestion:** Load documents and extract their text.
2. **Chunking:** Divide extracted text into smaller passages.
3. **Embedding Generation:** Convert each passage into a vector representation.
4. **Vector Storage:** Store embeddings, text chunks, and source metadata in ChromaDB.
5. **Query Embedding:** Convert the user's question into a vector.
6. **Retrieval:** Find the most relevant document chunks using vector similarity.
7. **Answer Generation:** Provide retrieved context to the LLM to generate a grounded response.
8. **Source Attribution:** Display supporting passages and source references alongside the answer.

## Project Structure

```text
multi-document-ai-research-assistant/
│
├── app.py
├── ingestion.py
├── chunking.py
├── embeddings.py
├── vector_store.py
├── retrieval.py
├── generation.py
├── requirements.txt
├── .gitignore
├── data/
└── README.md
```

## Learning Objectives

Through this project, I aim to develop practical knowledge of:

- Retrieval-Augmented Generation (RAG)
- Document ingestion and text preprocessing
- Chunk size and chunk overlap
- Text embeddings and semantic similarity
- Vector databases and similarity search
- LLM prompting and context grounding
- Source attribution and hallucination reduction
- Building and testing end-to-end AI applications

## Future Improvements

- Conversational memory for follow-up questions
- Metadata filtering by document and page
- Hybrid search combining keyword and vector retrieval
- Reranking retrieved passages
- RAG evaluation using retrieval and answer-quality metrics
- Deployment as a web application

## Author

**Mayuri Mangal**
