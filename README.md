# CapSense AI – Sentiment Analysis and Response Generation Application

**Developed for Capgemini** – As a team of developers, testers, and technical writers we developed CapSense AI in response to a customer-service problem and use case provided by Capgemini, the industry sponsor for our capstone project. Manual analysis of customer feedback and crafting personalized replies is a slow process prone to human error. Our system addresses this by leveraging AI to generate timely, empathetic responses, reducing daily operational hours.
**Impact:** Generated editable AI-powered responses with the potential to reduce customer support teams’ manual workload by approximately 80%.
See our original group repo here: https://github.com/CapSense/Capgemini_SentimentApp_Remake.

---
**Post-capstone edits to UI design 2026:**
<img width="2152" height="1360" alt="Demo app new design" src="https://github.com/user-attachments/assets/9f6105c4-bd13-48ff-afbe-06b3f74e03b7" />


## Overview

CapSense AI is an AI-powered Sentiment Analysis and Response Generation application designed to revolutionize customer service by analyzing customer feedback and generating empathetic, brand-aligned responses.

The system leverages machine learning for sentiment and emotion detection, sarcasm identification, and integrates advanced language models (OpenAI, then Phi-3, later Phi-4) to generate personalized responses. It enables batch processing of feedback, providing sentiment analysis while automating routine response generation and maintaining a consistent brand voice.

Our project showcases full-stack development, AI model integration, classifier model training, and practical experience deploying applications on Microsoft Azure.

---
## How It Works

**▶ Watch the demo of the sentiment analysis and response generation features**
[![Watch the demo of the sentiment analysis and response generation features](thumbnail.PNG)](https://drive.google.com/file/d/1hLhfb_w8bMp3_GzqWgtKudcqmytcW8Lk/view?usp=sharing)

As the above video demonstrates, CapSense AI uses a React and TypeScript frontend to collect customer feedback through CSV uploads. The frontend communicates with a Python Flask backend through REST APIs, where feedback is processed through sentiment, emotion, sarcasm, and aspect-based analysis. For instance, my custom Naïve Bayes classifier handles emotion detection, and a teammate's classifier model handles sarcasm detection, while Azure-hosted Phi models generate context-aware, empathetic responses. Results are returned to the frontend for visualization in an interactive sentiment analysis report and dashboard. The application and supporting services are deployed using Microsoft Azure.

## My Contributions

- **Frontend Development**  
  Built the responsive and interactive React frontend using Vite. Implemented:
  - CSV file upload for batch feedback.
  - Modular Sentiment Analysis Report UI with components for feedback classification, emotion, sarcasm, aspect-based sentiment, F-1 score, and AI-generated responses.
  - State management (UI changes) and API integration with Axios

- **Phi Model Integration**  
  - Initially integrated **Phi-3 Mini** model via Azure AI Foundry for context-aware, empathetic response generation after encountering constraints with OpenAI's ChatGPT.  
  - Updated payload format from OpenAI-style requests to Phi-compatible requests.  
  - Later upgraded to **Phi-4**, ensuring seamless response generation and fallback mechanisms.

- **Emotion Detection Model**  
  - Built and trained a **Naïve Bayes classifier** from scratch using 42,000+ customer feedback entries.  
  - Achieved **55.81% accuracy** across six primary emotions (anger, joy, fear, disgust, sadness, surprise).  
  - Integrated the model into the Flask backend for emotion classification.

- **Backend Integration & Deployment Support**  
  - Helped configure Flask APIs for batch processing (endpoints).  
  - Assisted in deploying the backend on **Azure Virtual Machines**, ensuring proper environment setup and port configuration. 
  - Helped debug server errors, install dependencies (e.g., NLTK), and ensure classifier functionality.

---

## Technologies Used

- **Frontend:** React, Vite, TypeScript, Bootstrap, Chart.js, Axios
- **Backend:** Python, Flask, Naïve Bayes (scikit-learn), NLTK, Hugging Face Transformers
- **AI Models:** OpenAI's GPT, Phi-3 Mini, Phi-4 (Azure AI Foundry via API)
- **Database:** Azure SQL, pyodbc
- **Deployment & Infrastructure:** Microsoft Azure App Service, Azure VM, Azure AI Foundry
- **Other Tools:** GitHub, GitHub Actions (CI/CD), PuTTy, WinSCP

---

## Key Features

- Sentiment Classification: Positive, Negative, Neutral  
- Emotion Detection: Anger, Joy, Fear, Disgust, Sadness, Surprise  
- Sarcasm Detection  
- AI-Generated Empathetic Responses via Phi models  
- Aspect-Based Sentiment Analysis  
- Batch Processing of CSV Feedback File  
- Dashboard for visualization and analysis

---

## Installation & Usage

**Prerequisites:** Python 3.x, npm, Git, IDE (VS Code or PyCharm), Microsoft Azure/Azure AI Foundry and the required Azure/AI credentials and environment variables.

1. **Clone the repository**
```bash
git clone https://github.com/vongaik/CapSense-AI.git
cd capSense-AI
```

2. **Install backend dependencies**
```bash
pip install -r requirements.txt
```

3. **Install frontend dependencies**
```bash
cd frontend
npm install
```

4. **Set environment variables**
```bash
PHI4_KEY=<your-phi4-key>
PHI4_ENDPOINT=<your-phi4-endpoint>
```

5. **Run Backend**
```bash
python app.py
```

6. **Run Frontend**
```bash
npm run dev
```

7. **Access the application** via browser at `http://localhost:3000`

---

## Key Achievements

- Developed a **full-stack AI application** handling both frontend and backend integration with my team.  
- Built a **custom Naïve Bayes emotion classifier** from scratch, achieving an effective result without relying on heavy transformers.  
- Integrated **Phi-3/Phi-4 models** for dynamic, context-aware response generation.  
- Successfully deployed the system on **Azure Virtual Machines**, demonstrating cloud deployment and environment management skills.  
- Collaborated effectively with my team while resolving deployment and integration challenges and managing time-zone differences.

---


## Testing & User Documentation
- ![User Documentation](<CapSense User Documentation.docx>) – Instructions for using the application.
- ![Testing Report](<Comprehensive Testing Report.docx>) – Detailed testing procedures, test cases, and results.

---

**CapSense AI** reflects my hands-on experience in **full-stack development, machine learning, NLP, AI model integration, and cloud deployment**, while giving me practical experience working on a real-world industry-sponsored project.

