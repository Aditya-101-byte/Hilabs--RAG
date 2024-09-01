# Hilabs--RAG

# Retrieval-Augmented Generation (RAG) AI System

## Overview:
This repository provides a solution for creating a Retrieval-Augmented Generation (RAG) based AI system capable of answering questions about personal or work-related information.
The system leverages a combination of large language models (LLMs) and vector databases to generate accurate and contextually relevant responses based on the provided data.

## Objectives:
Load Personal Data: Use resume or other relevant documents stored in the data/ folder.
Data Processing: Split documents into chunks and index them in a vector database.
Query Handling: Use Streamlit for user queries, retrieve relevant context from the vector database, and generate answers using LLMs.

# Installation
## Follow these steps to set up the environment and run the RAG-based AI system:

## Clone the Repository:

git clone repository-url

cd repository-directory

## Create and Activate a Conda Environment:

conda create --name rag-system python=3.9
conda activate rag-system

## Install Dependencies:

Ensure you have a requirements.txt file in your repository. Install the required dependencies:
pip install -r requirements.txt

## Install Ollama from the ollama website

Download and Serve LLM Models
Pull the LLM model and start the Ollama server:
ollama pull llama3
ollama serve

##Prepare Data:
make a directory named "data" which contains all the pdf
make a directory named "chroma" 
Place your PDF files or other relevant data into the data/ folder.
Run the Streamlit Application
Start the Streamlit application to interact with the AI system:

streamlit run app.py


# Code description:

__init__:

Initializes the RAG system with paths for data and the vector database. It also sets up the language model and the prompt template used for generating answers.
_setup_collection:

Loads documents from the specified directory, splits them into chunks, assigns unique IDs to these chunks, and then adds them to the vector database if they are not already present. It also persists the database changes.
_get_chunk_ids:

Generates unique IDs for each chunk based on its source and page number. This helps in managing and identifying chunks within the database.
_retrieve_context_from_query:

Retrieves relevant context from the vector database based on the user's query. This context is used to help answer the query.
_get_prompt:

Creates a prompt for the language model using the retrieved context and the user’s question. The prompt is formatted according to the predefined template.
answer_query:

Uses the language model to generate a response based on the prompt created. It formats and returns the response to the user.
_load_documents:

Loads PDF documents from the specified directory and prepares them for processing.
_document_splitter:

Splits loaded documents into manageable chunks for efficient indexing and retrieval.
_get_embedding_func:

Retrieves the function used to generate embeddings for the document chunks using the specified model.
_initialize_vectorDB:

Initializes the vector database and sets it up to store document embeddings. This allows for efficient similarity searches and context retrieval.
