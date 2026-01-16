☁️ GCP ACE Exam Simulator

A production-ready, AI-powered practice platform for the Google Cloud Associate Cloud Engineer (ACE) certification. This simulator uses the Gemini 2.5 API to synthesize dynamic, scenario-based questions across all GCP domains.

✨ Key Features

🎯 Domain-Specific Sets: Choose between full practice exams or focused drills in IAM, Networking, Compute, and Storage.

🤖 AI Question Synthesis: Uses Gemini 2.5 Flash to generate unique questions on the fly, ensuring no two practice sessions are identical.

📊 Progress Tracking: Integrated localStorage persistence to track your exam history and average score.

🛡️ Production Security: Secure Node.js backend proxy hides your API keys and prevents client-side exposure.

⏱️ Realistic Environment: Timed exam interface with progress indicators and detailed rationale for every answer.

🏗️ Architecture

Frontend: Single-page application (SPA) built with Tailwind CSS.

Backend: Express.js proxy with express-rate-limit for DDoS/Abuse protection.

Intelligence: Google Gemini 2.5 API for high-fidelity technical content generation.

🚀 Quick Start

1. Prerequisites

Node.js installed (v16+)

A Google Gemini API Key

2. Backend Setup

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env # Or create manually


Edit .env:

GEMINI_API_KEY=your_key_here
PORT=3000
ALLOWED_ORIGIN=http://localhost:8080
NODE_ENV=development


Start the proxy:

npm start


3. Frontend Setup

Serve the public folder using any local server (e.g., VS Code Live Server or npx http-server):

npx http-server ./public -p 8080


☁️ Deployment (Vercel)

This project is configured for easy deployment as a Monorepo or separate services.

Backend: Deploy the root folder to Vercel. It will automatically detect the server.js (ensure you add your Environment Variables in the Vercel Dashboard).

Frontend: Update the API_ENDPOINT in index.html to point to your live backend URL.

🛡️ Security Features

Backend Proxy: Prevents leaking API keys to the client browser.

Rate Limiting: Restricts users to 10 exam generations per hour to manage costs.

CORS Protection: Restricts API access only to your authorized frontend domain.

Input Validation: Sanitizes request payloads before forwarding to Google APIs.

📄 License

Distributed under the MIT License. See LICENSE for more information.
