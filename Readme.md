# Gemma Model Document Q&A

## Overview

Gemma Model Document Q&A is a Streamlit application that allows users to upload a set of PDFs, save them into a vector database, and retrieve context-based answers from them. The application utilizes LangChain, FAISS, and Google's Generative AI for embedding and retrieval. This README will guide you through setting up and using the application with your own APIs, including Groq and Google.

## Features

- Load and process PDF documents
- Generate vector embeddings for document chunks **Locally**
- Query the documents for context-based answers
- Utilize Groq and Google Generative AI for powerful language processing

## Requirements
1. Make sure you have the following libraries installed. These are listed in the `requirements.txt` file
2. Add your own API keys for both Groq and Google to the .env file
   ```text
      GROQ_API_KEY="your_groq_api_key"
      GOOGLE_API_KEY="your_google_api_key"
   ```
4. Create a file to add your own data in (data in my case) and make sure you modify the path to it in the code```st.session_state.loader=PyPDFDirectoryLoader("./data")```
5. Add your own documents in pdf format in the created folder ```"./data"```
6. Run the streamlit app by running this command ```stramlit run main.py``` in the terminal

## Using the Application
Launch the App: Open your browser and navigate to the local Streamlit server (usually http://localhost:8501).

Embed Documents: Click the "Documents Embedding" button to process the PDFs and create the vector store database.

Ask Questions: Enter your question in the text input field and click enter. The application will retrieve the context-based answer from the processed documents.

## Usefull Links:
LangChain: [LangChain Documentation](https://api.python.langchain.com/en/latest/langchain_api_reference.html).
FAISS: [FAISS Documentation](https://github.com/facebookresearch/faiss)
Streamlit: [Streamlit Documentation](https://docs.streamlit.io/)
PyPDF2: [PyPDF2 Documentation](https://pypdf2.readthedocs.io/en/3.x/)

Feel free to fork the project, make improvements, and contribute back! If you encounter any issues, please open an issue on the GitHub repository.
