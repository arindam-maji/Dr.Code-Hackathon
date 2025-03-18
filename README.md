📚 AI Lead Management System
AI Lead Management System is a full-stack web application designed to streamline lead capturing, scoring, and sentiment analysis using AI. It consists of a ReactJS frontend, a FastAPI backend, and integrates machine learning models to process and analyze lead data efficiently.

🚀 Project Overview
Frontend: ReactJS with REST API integration for lead submission and results display.
Backend: FastAPI for lead capture, scoring, and sentiment analysis.
ML Models: Python-based models for lead scoring and sentiment analysis.
Database: SQL schema for storing lead data.
📂 Project Structure
bash
Copy
Edit
/AI_Lead_Management_Full
├── /backend
│   ├── /api
│   ├── /models
│   ├── /utils
│   ├── /venv
│   ├── main.py
│   └── /ml_models
│       ├── lead_scoring.py
│       └── sentiment_analysis.py
├── /database
│   └── schema.sql
├── /frontend
│   ├── /public
│   │   └── index.html
│   ├── /src
│   │   ├── /components
│   │   ├── /pages
│   │   ├── App.jsx
│   │   └── styles.css
│   ├── package.json
│   └── package-lock.json
└── README.md
🛠 Tech Stack
Frontend:
ReactJS
Axios for API communication
CSS for styling
Backend:
FastAPI (Python)
Uvicorn for ASGI server
Pandas, NumPy, and Scikit-learn for ML processing
Machine Learning Models:
Lead Scoring Model (lead_scoring.py)
Sentiment Analysis Model (sentiment_analysis.py)
⚙ Setup and Installation
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/AI_Lead_Management_Full.git
cd AI_Lead_Management_Full
2. Set Up Backend (FastAPI)
Navigate to the backend directory:
bash
Copy
Edit
cd backend
Create and activate a virtual environment:
bash
Copy
Edit
# Create virtual environment
python -m venv venv

# Activate virtual environment (Windows)
venv\Scripts\activate

# Activate virtual environment (Mac/Linux)
source venv/bin/activate
Install dependencies:
bash
Copy
Edit
pip install -r ../requirements.txt
Run the backend:
bash
Copy
Edit
python main.py
Backend will run at:

cpp
Copy
Edit
http://127.0.0.1:8000
3. Set Up Frontend (ReactJS)
Navigate to the frontend directory:
bash
Copy
Edit
cd ../frontend
Install dependencies:
bash
Copy
Edit
npm install
Run the frontend:
bash
Copy
Edit
npm start
Frontend will be available at:

arduino
Copy
Edit
http://localhost:3000
🧠 Usage
Open http://localhost:3000 in your browser.
Submit lead information through the form.
The backend processes the data and sends:
Lead score predictions.
Sentiment analysis of comments.
View the processed results on the UI.
🔥 API Endpoints
Base URL:
cpp
Copy
Edit
http://127.0.0.1:8000
1. Capture Lead
bash
Copy
Edit
POST /leads/capture
Request Body:
json
Copy
Edit
{
  "name": "John Doe",
  "email": "john@example.com",
  "comments": "Looking forward to connecting!"
}
Response:
json
Copy
Edit
{
  "message": "Lead captured successfully",
  "score": 85,
  "sentiment": "Positive"
}
🧪 Testing API Endpoints
Swagger Docs: http://127.0.0.1:8000/docs
Redoc Docs: http://127.0.0.1:8000/redoc
📊 Database Schema
sql
Copy
Edit
CREATE TABLE leads (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    comments TEXT,
    score INT,
    sentiment VARCHAR(20),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
🎯 Future Improvements
Add authentication and role-based access.
Improve ML models with larger datasets.
Integrate real-time lead notifications.
Deploy backend and frontend on cloud infrastructure.
🤝 Contributing
Fork the repository.
Create a new branch:
bash
Copy
Edit
git checkout -b feature-name
Commit your changes:
bash
Copy
Edit
git commit -m "Add feature"
Push to your branch:
bash
Copy
Edit
git push origin feature-name
Submit a pull request.
