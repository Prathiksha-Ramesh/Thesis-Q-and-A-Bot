# Thesis Q&A Bot

This project is a Streamlit-based application that allows users to ask questions about a collection of PDF documents. The system uses advanced natural language processing (NLP) models, including Groq's Gemma model and Google's Generative AI embeddings, to retrieve and provide accurate answers based on the content of the uploaded documents.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [License](#license)
- [Contributing](#contributing)

## Overview

This application processes PDF documents stored in a directory, splits them into manageable text chunks, and creates vector embeddings for efficient retrieval. Users can ask questions about the documents, and the system will provide answers based on the context of the documents.

## Features

- **Document Ingestion**: Load and process PDF documents from a specified directory.
- **Text Chunking**: Split document text into smaller, manageable chunks for processing.
- **Vector Embeddings**: Generate vector embeddings using Google's Generative AI model for efficient document retrieval.
- **Question Answering**: Use Groq's Gemma model to answer questions based on the content of the documents.
- **Interactive Interface**: User-friendly interface built with Streamlit for asking questions and processing documents.

## Installation

### Prerequisites

- Python 3.7 or higher
- Git

### Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/thesis-qa-bot.git
    cd thesis-qa-bot
    ```

2. Create a virtual environment and activate it:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up environment variables:

    - Create a `.env` file in the root directory with the following content:

      ```
      GROQ_API_KEY=your_groq_api_key
      GOOGLE_API_KEY=your_google_api_key
      ```

    - Replace `your_groq_api_key` and `your_google_api_key` with your actual API keys.

5. Place your PDF documents in the `./Article` directory.

## Usage

To run the application:

```bash
streamlit run app.py
```
## How It Works:

- **Document Embeddings**: Click the "Documents embeddings" button to process the PDF documents and create a vector store database.
- **Ask Questions**: Enter your question in the input box, and the system will retrieve and display the most relevant answer based on the document content.

### Example:

- **Upload PDFs**: Place your PDF files in the `./Article` directory.
- **Process Files**: Click on "Documents embeddings" to process the PDFs.
- **Ask Questions**: Type your question in the input box, and the system will provide a detailed answer.

## Project Structure

- `app.py`: Main application file that handles the Streamlit interface and core functionality.
- `requirements.txt`: Lists all the dependencies required to run the project.
- `.env`: Environment variables file (not included in the repository; must be created by the user).
- `Thesis/`: Directory where your thesis PDF documents are stored.

## Dependencies

The project uses the following dependencies:

- `streamlit`: For building the interactive user interface.
- `langchain_groq`: For integrating Groq's Gemma model.
- `langchain_google_genai`: For generating embeddings using Google Generative AI.
- `faiss-cpu`: For efficient similarity search using vector embeddings.
- `python-dotenv`: For managing environment variables.
- `PyPDF2`: For extracting text from PDF files.
- `langchain_community`: Community-driven components for LangChain.

For a full list of dependencies, please refer to the `requirements.txt` file.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.
