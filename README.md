# Conversation Management System with Groq API

This project implements a conversation management system with two main tasks:

## Task 1: Conversation History Management with Summarization
A system that maintains conversation history with automatic summarization and truncation capabilities.

### Features:
- Maintains running conversation history between user and assistant
- Implements automatic summarization to keep conversations concise
- Supports multiple truncation methods:
  - By number of conversation turns (last n messages)
  - By character length
  - By word count
- Performs periodic summarization after every k-th conversation exchange
- Stores summaries as system messages in the conversation history

### Usage:
Run the chat interface and interact with the AI assistant. The system will automatically:
- Manage conversation history length
- Summarize conversations every 3 exchanges
- Provide commands to view history and manually trigger summarization

## Task 2: JSON Schema Classification & Information Extraction
A system that extracts structured information from conversations using OpenAI function calling with Groq API.

### Features:
- Defines a JSON schema to extract 5 user details: name, email, phone, location, and age
- Uses OpenAI function calling for structured data extraction
- Validates extracted information against the schema
- Demonstrates parsing of 3 sample conversations with validation results

### Schema Definition:
The system extracts the following information:
- `name` (string): User's full name
- `email` (string): User's email address  
- `phone` (string): User's phone number
- `location` (string): User's location or address
- `age` (integer): User's age

## Setup Instructions

1. **Install Dependencies**:
```bash
pip install openai python-dotenv
```

2. **API Configuration**:
   - The project uses Groq API with OpenAI-compatible SDK
   - API key is included in the notebook for testing

3. **Run the System**:
   - Execute the notebook cells in sequence
   - For Task 1: Run the chat interface to interact with the assistant
   - For Task 2: Run the demonstration to see information extraction from sample conversations

## Technical Details

- **Framework**: Standard Python with OpenAI client (no additional frameworks)
- **API**: Groq API with OpenAI-compatible interface
- **Model**: llama-3.3-70b-versatile
- **Function Calling**: OpenAI-style function calling for structured data extraction

## Sample Outputs

The system demonstrates:
- Conversation history management with automatic summarization
- Information extraction from sample conversations
- Validation of extracted data against JSON schema
- Error handling for schema validation failures

