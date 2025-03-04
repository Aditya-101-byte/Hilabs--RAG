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


