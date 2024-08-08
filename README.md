# PDF-Agent


# Chat with Multiple PDFs

This Streamlit application allows you to upload multiple PDF documents and interact with them through a chatbot interface. By leveraging the power of LangChain, OpenAI, and FAISS, the app enables users to ask questions about the contents of the uploaded PDFs and receive intelligent responses.

## Features

- **Upload Multiple PDFs**: Upload one or more PDFs via the sidebar to process and analyze.
- **Text Extraction**: Extracts raw text from all pages of the uploaded PDFs.
- **Text Chunking**: Splits the extracted text into manageable chunks for better processing.
- **Conversational AI**: Engages in a conversation with the user, answering questions based on the content of the PDFs.
- **Persistent Chat Memory**: Maintains conversation history within the session for context-aware interactions.

## Usage

1. **Upload PDFs**: Use the sidebar to upload one or more PDF documents.
2. **Process the Documents**: Click the "Process" button to extract and process the text from the PDFs.
3. **Ask Questions**: Type your question in the text input box and press Enter. The chatbot will respond with information extracted from the uploaded documents.

## Project Structure

- `app.py`: Main application file containing the Streamlit app logic.
- `htmlTemplate.py`: Contains HTML templates used for rendering chat messages in the app.
- `requirements.txt`: Python dependencies required to run the application.

## How It Works

1. **PDF Text Extraction**: The `get_pdf_text` function reads the uploaded PDFs and extracts raw text.
2. **Text Chunking**: The `get_text_chunks` function splits the extracted text into chunks for easier processing by the AI model.
3. **Vector Store Creation**: The `getvector_store` function converts the text chunks into embeddings using OpenAI's API and stores them in a FAISS vector store for efficient retrieval.
4. **Conversation Chain**: The `get_conversation_chain` function creates a conversation chain that allows the AI model to interact with the user, utilizing the vector store for information retrieval.
5. **User Interaction**: The `handle_userinput` function processes user questions and returns answers based on the content of the PDFs.

## Dependencies

- `streamlit`
- `dotenv`
- `PyPDF2`
- `langchain`
- `langchain_community`
- `openai`
- `faiss`

- `requirements for this app: streamlit, pypdf2, langchain, python-dotenv, faiss-cpu, openai`

## Future Improvements

- **Enhanced PDF Parsing**: Improve the text extraction process to better handle complex PDF structures.
- **Support for Other Document Types**: Extend support to other document formats like Word, Excel, etc.
- **Advanced Question Handling**: Implement more sophisticated NLP techniques to handle a wider range of user queries.
