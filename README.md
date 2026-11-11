# IndustryGPT – Banking Information Assistant

## Project Overview

IndustryGPT is a domain-specific banking chatbot developed using **Retrieval-Augmented Generation (RAG)**. It answers banking-related questions by retrieving relevant information from a banking PDF document and generating context-based responses using a pre-trained language model.

## System Architecture

The application follows a RAG-based architecture consisting of the following components:

1. **Document Loading:** Loads and extracts text from the banking PDF using PyPDFLoader.
2. **Text Splitting:** Divides the extracted text into smaller chunks using RecursiveCharacterTextSplitter.
3. **Embedding Generation:** Converts text chunks into numerical vector representations using Sentence Transformers (`all-MiniLM-L6-v2`).
4. **Vector Database:** Stores embeddings in FAISS for efficient similarity-based retrieval.
5. **Information Retrieval:** Converts the user's query into an embedding and retrieves relevant document chunks.
6. **Relevance Check:** Applies a distance-based threshold to filter irrelevant queries.
7. **Response Generation:** Uses the retrieved context and the FLAN-T5 pre-trained language model to generate answers.
8. **User Interface:** Uses Streamlit to provide an interactive chatbot interface.

## Technologies Used

- Python
- LangChain
- PyPDF
- Sentence Transformers
- FAISS
- Hugging Face Transformers
- FLAN-T5

## Conclusion

IndustryGPT demonstrates the practical implementation of Retrieval-Augmented Generation in the banking domain. By combining document processing, semantic search, vector similarity retrieval, and a pre-trained language model, the application provides context-based answers from banking documents. This project explores the application of Large Language Models (LLMs) and RAG techniques to develop domain-specific conversational AI systems.
