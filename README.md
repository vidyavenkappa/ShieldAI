# ShieldAI

## Overview
This project is a backend implementation of an **agentic chatbot** using **FastAPI, LangGraph, ChromaDB, and SQLite**. The chatbot is designed to process cybersecurity-related queries by leveraging a structured framework that:

1. **Plans**: Determines whether to break down or process the query as a whole.
2. **Fetches Context**: Retrieves relevant cybersecurity data from ChromaDB.
3. **Generates a Response**: Uses Mistral or Gemini API for LLM-based answer generation.
4. **Validates the Response**: Ensures answer quality before delivering it to the user.

## Features
- **FastAPI-powered REST API & WebSockets for real-time responses**
- **LangGraph for structured agentic decision-making**
- **ChromaDB for vector-based data retrieval**
- **SQLite database for query logging**
- **Mistral/Gemini integration for LLM-based response generation**

## Tech Stack
- **Backend:** FastAPI, LangGraph, ChromaDB, SQLite
- **LLM:** Mistral or Gemini API
- **Database:** SQLite (for metadata), ChromaDB (for vector search)

## Installation

### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- pip
- Virtual environment (optional but recommended)

### Steps to Set Up
```sh
# Clone the repository
git clone <repo-url>
cd <repo-folder>

# Create a virtual environment and activate it
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the FastAPI server
uvicorn main:app --reload
```

## API Endpoints
### 1. Query Processing (POST /query)
**Description**: Takes a question as input, processes it using the agentic workflow, and returns a response.

**Request:**
```json
{
  "question": "What are the latest cybersecurity threats?"
}
```
**Response:**
```json
{
  "response": "Latest cybersecurity threats include X, Y, and Z."
}
```

### 2. WebSocket for Real-Time Chat (ws /ws)
**Description**: Enables real-time communication with the chatbot.

**Usage:** Connect via WebSocket and send messages directly. The server responds in real time.

## Future Improvements
- **Enhanced query decomposition** for more precise responses.
- **Improved validation framework** for response accuracy.
- **Frontend integration** with React and Tailwind.

## License
This project is licensed under the MIT License.

