📦 ZIP Resume Analyzer (Hugging Face + LangChain + Streamlit)

A Streamlit-based web application that allows users to upload a ZIP file containing multiple resumes (PDF/DOCX) and automatically extracts structured candidate information using Hugging Face LLMs with LangChain.

🚀 Features

📁 Upload a ZIP file containing multiple resumes

📄 Supports PDF and DOCX resume formats

🤖 Uses Mistral-7B-Instruct model via Hugging Face API

🧠 Extracts structured resume data:

Candidate Name

Email Address

Technical Skills

Professional Summary

📊 Displays extracted data in JSON format

🔐 Secure API key handling using .env

⚡ Simple and interactive Streamlit UI

🛠 Tech Stack

Python

Streamlit – Web interface

LangChain – Prompt orchestration

Hugging Face Hub – LLM inference

Mistral-7B-Instruct-v0.2 – Language model

Pydantic – Structured output validation

PyPDF – PDF parsing

python-docx – DOCX parsing

📂 Project Structure
zip-resume-analyzer/
│── app.py
│── .env
│── requirements.txt
│── README.md

⚙️ Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/your-username/zip-resume-analyzer.git
cd zip-resume-analyzer

2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate   # Windows

3️⃣ Install Dependencies
pip install -r requirements.txt


requirements.txt

streamlit
python-dotenv
langchain
langchain-core
langchain-huggingface
huggingface-hub
pydantic
pypdf
python-docx

🔑 Environment Variables

Create a .env file in the project root:

hf=YOUR_HUGGINGFACE_API_KEY


👉 Get your API key from:
https://huggingface.co/settings/tokens

▶️ Running the Application
streamlit run app.py


Open in browser:

http://localhost:8501

🧪 How It Works

User uploads a ZIP file with resumes

App extracts files into a temporary directory

Text is read from PDF/DOCX files

LangChain sends resume text to Hugging Face LLM

Model returns structured data validated by Pydantic

Results displayed as JSON per resume

📸 Sample Output
{
  "name": "John Doe",
  "email": "john.doe@gmail.com",
  "skills": ["Python", "SQL", "Power BI"],
  "summary": "Detail-oriented data analyst with experience in data visualization."
}

⚠️ Notes

Large resumes may affect response time

Ensure Hugging Face API quota is available

Internet connection required for model inference

🔮 Future Enhancements

Resume ranking & scoring

Skill normalization

Export results to Excel/CSV

Chunking for large resumes

Support for more file formats
