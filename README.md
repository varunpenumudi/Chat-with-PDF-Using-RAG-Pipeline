# Chat with PDF Using RAG Pipeline  

This repository contains a Python implementation of a **Retrieval-Augmented Generation (RAG) pipeline** that allows users to interact with semi-structured data in PDF files. The pipeline extracts text and image data, processes it, and enables efficient question answering using embeddings and a language model.  

## Features  
- Extracts text and images from PDF files.  
- Applies OCR on images to retrieve embedded text.  
- Converts extracted data into vector embeddings for similarity-based retrieval.  
- Uses the Groq LLM to generate detailed and context-aware responses.  

## How It Works  
1. **Data Extraction**:  
   - Extracts text from PDFs using `PyPDFLoader`.  
   - Retrieves images from PDFs with `PyMuPDF` and processes them using Tesseract OCR.  

2. **Embedding and Storage**:  
   - Embeds text chunks and image texts using HuggingFace embeddings.  
   - Stores embeddings in a Chroma vector database.  

3. **Question Answering**:  
   - Retrieves relevant data using the query's embedding.  
   - Uses Groq LLM to generate a response based on the retrieved context.  

## Setup  
1. open the PDF_RAG_pipeline.ipynb from the repo
2. ![image](https://github.com/user-attachments/assets/dd7025dd-31fb-4abf-81b8-b4f0e04799dc)
3. Run the cells
4. Add your Groq LLM API key in the script when prompted.  

## Usage  
Run the script and interact with the pipeline:  
```python  
get_resp("Your question here")  
```  

## Example Queries  
- "Tell me about the US GDP?"  
- "What is the unemployment rate?"  
- "When to use a Line Graph, Pie Chart, or Bar Graph?"  
