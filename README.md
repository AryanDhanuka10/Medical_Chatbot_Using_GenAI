# 🩺 Medical Chatbot Using GenAI

[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)  
[![Flask](https://img.shields.io/badge/Flask-3.1.1-lightgrey.svg)](https://flask.palletsprojects.com/)  
[![Streamlit](https://img.shields.io/badge/Streamlit-Enabled-red.svg)](https://streamlit.io/)  
[![LangChain](https://img.shields.io/badge/LangChain-0.3.26-orange.svg)](https://www.langchain.com/)  
[![License](https://img.shields.io/badge/License-Apache_2.0-green.svg)](./LICENSE)  

---

## 🚀 Overview

The **Medical Chatbot** is an AI-powered assistant built using **Generative AI, LangChain, Pinecone, and LLMs**.  
It retrieves medical knowledge from indexed PDFs, processes queries, and provides concise, medically relevant answers.

You can interact with the chatbot using:

- 🖥 **Flask Web Interface**  
- 🌐 **Streamlit Chat UI**  
- ☁️ **AWS Deployed Dockerized Version** (CI/CD with GitHub Actions)

---

## ✨ Features

- 📄 **PDF Knowledge Base** → Medical documents are embedded and indexed using Pinecone.  
- 🤖 **LLM-Powered** → Uses `llama-3.3-70b` (via `ChatGroq`) for answering queries.  
- 💬 **Interactive Chat UI** → Flask (Bootstrap UI) and Streamlit (modern chat UI).  
- ☁️ **AWS CI/CD Pipeline** → Fully automated Docker image build & deploy with GitHub Actions.  
- 🔐 **Environment Variable Support** → `.env` for API keys (OpenAI, Pinecone, Groq).  

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/AryanDhanuka10/Medical_Chatbot_Using_GenAI
cd Medical_Chatbot_Using_GenAI

2️⃣ Create a Conda Environment
conda create -n medibot python=3.10 -y
conda activate medibot

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Configure Environment Variables

Create a .env file in the root directory:

PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxx"
GROQ_API_KEY = "xxxxxxxxxxxxxxxxxxxx"
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxx"

5️⃣ Store Embeddings in Pinecone
python store_index.py

6️⃣ Run Locally



👉 Streamlit App

streamlit run streamlit.py

App will run at: https://medicalchatbotusinggenai-aryan.streamlit.app/

🌐 Deployed Links

🚀 Streamlit Deployment → Click Here
 (update with your link)



🛠 Tech Stack

Backend: Python, Flask, Streamlit

AI/LLM: LangChain, ChatGroq, HuggingFace Embeddings

Database: Pinecone (Vector Database)

Deployment: Docker, AWS EC2, ECR, GitHub Actions (CI/CD)

📦 Docker Support

Build Docker image:

docker build -t medical-chatbot .


Run Docker container:

docker run -p 8080:8080 medical-chatbot

☁️ AWS CI/CD Deployment

The project includes a GitHub Actions workflow (.github/workflows/cicd.yaml) that:

Builds & pushes Docker image → Amazon ECR

Deploys container → AWS EC2 self-hosted runner

Exposes service at → http://<EC2-IP>:8080

Secrets to configure in GitHub:

AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

AWS_DEFAULT_REGION

ECR_REPO

PINECONE_API_KEY

OPENAI_API_KEY

GROQ_API_KEY

📂 Project Structure
├── app.py                # Flask Web App
├── streamlit.py          # Streamlit App
├── store_index.py        # Pinecone Embedding Store
├── src/
│   ├── helper.py         # Helper functions
│   ├── prompt.py         # System + user prompts
├── templates/chat.html   # Flask frontend (Bootstrap UI)
├── static/style.css      # Chat styling
├── requirements.txt      # Dependencies
├── Dockerfile            # Docker configuration
├── .github/workflows/    # CI/CD pipeline
└── README.md             # Project documentation

📜 License

This project is licensed under the Apache 2.0 License.
See the LICENSE
 file for details.

👨‍💻 Author

Aryan Dhanuka
📧 a9936067905@gmail.com

🌐 GitHub Profile : https://github.com/AryanDhanuka10?tab=repositories