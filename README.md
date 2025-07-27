Cyber‑Sane
Cyber‑Sane is an AI-powered personal assistant designed to represent a user's professional profile, skills, and experience. It uses large language models to simulate conversational interactions on a personal website or portfolio, allowing potential clients or employers to ask questions, receive responses, and leave contact details.

✨ Features
🧠 LLM-Powered Chatbot (Gemini 2.5 Pro)

📄 Parses résumé PDFs and professional summaries

🤖 Records user emails and logs unanswerable questions

🔔 Sends push notifications using Pushover API

🌐 Deployable via a Gradio-based web UI

🧰 Tech Stack
Python 3

OpenAI-compatible LLM API (e.g., Gemini via proxy)

pypdf for PDF parsing

gradio for UI

dotenv for managing secrets

requests for webhooks and API interactions


🚀 Setup Instructions
1. Clone the Repo
git clone https://github.com/sane2002/Cyber-Sane.git
cd Cyber-Sane

3. Create .env file
Create a .env file in the root folder with the following variables:
GOOGLE_API_KEY=your_google_api_key
PUSHOVER_TOKEN=your_pushover_app_token
PUSHOVER_USER=your_pushover_user_key

3. Install Requirements
pip install -r requirements.txt


5. Project Structure
Cyber-Sane/
├── app.py               # Main application script
├── requirements.txt     # Python dependencies
├── me/
│   ├── Resume.pdf       # Your personal résumé
│   └── summary.txt      # Your professional summary
└── .env                 # Environment variables (not committed)
🖥️ Usage
To launch the chatbot UI:
python app.py
This starts a Gradio interface where users can ask questions. The assistant replies based on résumé + summary context, logs unknown queries, and prompts for emails from interested users.

🔧 Customization
Replace me/Resume.pdf and me/summary.txt with your own.

Update prompt style or persona in the system_prompt() method.

Add more tool functions to expand capability.

📬 Contact Logging
All user emails are logged using record_user_details()

Unknown or out-of-scope questions are recorded via record_unknown_question()

Both trigger push notifications via Pushover
