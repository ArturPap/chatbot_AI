AI-Powered Chatbot with RAG
Overview

This project implements an AI-powered chatbot leveraging Large Language Models (LLM) and Retrieval-Augmented Generation (RAG) for contextual responses. Built with Python, it integrates Hugging Face transformers, LangChain for RAG, SQLite for conversation storage, and Pandas for data analysis, meeting the requirements for a Data Scientist role focused on generative AI.
Features

    LLM Integration: Uses distilgpt2 for response generation, configurable for other transformer models.
    RAG Capability: Indexes documents (e.g., PDFs) with FAISS and Hugging Face embeddings for context-aware responses.
    Conversation Storage: Stores user inputs and responses in SQLite for persistence.
    Data Analysis: Analyzes conversation history with Pandas, providing insights like response length.
    Error Handling & Logging: Robust logging and exception handling for reliability.
    Asynchronous Processing: Utilizes asyncio for efficient response generation.

Requirements

    Python 3.8+
    Libraries:
        transformers
        langchain
        langchain-community
        faiss-cpu
        torch
        pandas
        numpy
        PyPDF2
        sentence-transformers
    Optional: CUDA-enabled GPU for faster processing

Installation

    Clone the repository:
    bash

git clone <repository-url>
cd <repository-folder>
Create a virtual environment (optional but recommended):
bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:
bash
pip install -r requirements.txt
Or install individually:
bash

    pip install transformers langchain langchain-community faiss-cpu torch pandas numpy PyPDF2 sentence-transformers
    Ensure a sample PDF (sample_knowledge_base.pdf) is available for RAG or modify the file path in the script.

Usage

    Run the chatbot:
    bash

    python AI_Powered_Chatbot_with_RAG.py
    The script loads documents, processes a sample query ("What is machine learning?"), and outputs the response and conversation analysis.
    Modify main() for custom inputs or integrate with a UI.

Project Structure

    AI_Powered_Chatbot_with_RAG.py: Main script with chatbot logic.
    chatbot_data.db: SQLite database for conversation history.
    sample_knowledge_base.pdf: Sample document for RAG (not included).
    requirements.txt: List of dependencies.
    README.md: Project documentation.

Troubleshooting

    ModuleNotFoundError: No module named 'langchain_community': Install the langchain-community package:
    bash

pip install -U langchain-community
Missing PDF File: The script expects sample_knowledge_base.pdf. Provide a valid PDF or update the file path in load_documents.
Indentation Issues: Ensure consistent 4-space indentation. Use a linter like flake8:
bash

    pip install flake8
    flake8 AI_Powered_Chatbot_with_RAG.py

Future Improvements

    Integrate advanced frameworks like LlamaIndex or Haystack for enhanced LLM workflows.
    Add Reinforcement Learning for response optimization.
    Support real-time document uploads and multi-user sessions.

License

MIT License
Contact
