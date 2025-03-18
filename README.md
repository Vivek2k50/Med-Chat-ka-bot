# Med-Chat-ka-bot
Don't read Med-Chat ka bot😒.. Please read Medical chatbot 


Overview

This project is a medical chatbot that provides answers based on information extracted from medical books and PDFs. The chatbot utilizes LangChain, FAISS, and HuggingFace's Mistral-7B-Instruct-v0.3 to create a question-answering system with context-aware retrieval.

Features

PDF Document Ingestion: Loads and processes PDFs to extract relevant text.

Chunking and Embeddings: Uses RecursiveCharacterTextSplitter to split text and HuggingFaceEmbeddings to generate vector embeddings.

FAISS Vector Store: Stores document embeddings for efficient retrieval.

Mistral-7B-Instruct LLM: Uses HuggingFace's Mistral-7B-Instruct-v0.3 for generating responses.

Custom Prompting: Ensures chatbot responses are strictly based on the provided documents.

Streamlit UI: Provides a user-friendly chat interface.

Installation

Prerequisites

Ensure you have the following installed:

Python 3.8+

Usage

Step 1: Load and Process PDFs

Place your medical PDFs in the data/ directory.

Run the script to process the documents and store embeddings:

python process_pdfs.py

Step 2: Run the Chatbot

streamlit run chatbot.py

Configuration

Set your HuggingFace API token 

HF_TOKEN=your_huggingface_token

Project Structure

medical-chatbot/
│── data/                     # Directory for storing PDF documents
│── vectorstore/              # Directory for FAISS vector database
│── process_pdfs.py           # Script to process PDFs and create embeddings
│── chatbot.py                # Streamlit app for chatbot interface
│── requirements.txt          # Required dependencies
│── .env                      # Environment variables
└── README.md                 # Project documentation

Future Improvements

Integrate more medical knowledge sources.

Enhance retrieval with better embeddings.

Add support for multiple languages.
