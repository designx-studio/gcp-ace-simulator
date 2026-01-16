GCP ACE Exam Simulator

A production-ready Google Cloud Associate Cloud Engineer (ACE) exam simulator. This project uses a secure Node.js backend proxy to communicate with the Gemini 2.5 API, protecting your API keys and implementing rate limiting.

🚀 Quick Start

1. Prerequisites

Node.js installed

A Google Gemini API Key

2. Backend Setup

Navigate to the root directory.

Install dependencies:

npm install


Create a .env file:

GEMINI_API_KEY=your_actual_key_here
PORT=3000
ALLOWED_ORIGIN=http://localhost:8080
NODE_ENV=development


Start the server:

npm start


3. Frontend Setup

The frontend is a single HTML file. You can serve it using any local server (like live-server or http-server):

npx http-server ./public


🛡️ Security Features

Backend Proxy: Prevents leaking API keys to the client browser.

Rate Limiting: Restricts users to 10 exam generations per hour.

CORS Protection: Restricts API access to authorized domains.

Input Validation: Ensures only valid requests reach the AI model.