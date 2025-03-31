# Project on API
1. Tech Stack
Backend: Python (FastAPI or Flask)

Deployment: Vercel (using Serverless Functions) or a cloud platform like AWS Lambda

LLM Integration: OpenAI GPT API or a fine-tuned local model

Storage: Temporary in-memory storage or cloud storage (for handling file uploads)

Repository: GitHub with an MIT License

2. API Implementation
The API should:

Accept a POST request with:

A question as a form field

An optional file upload

Process the question:

If it's text-based → Use LLM to generate an answer

If it's file-based → Extract the relevant data, then return the answer

Return the answer in a JSON format
