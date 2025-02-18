# Cotton Disease Detection & Recommendation System

🚀 **Overview**  
The **Cotton Disease Detection & Recommendation System** is a web application designed to help farmers by detecting various cotton diseases and recommending suitable fertilizers and crop choices based on critical factors like soil temperature, pH, nitrogen levels, and other agricultural parameters. The system leverages machine learning for disease detection and provides real-time recommendations, empowering farmers with insights to optimize crop health and productivity.

🎯 **Key Features**

- **Cotton Disease Detection**: Identifies diseases like aphids, armyworms, bacterial blight, cotton boll rot, and more, from images of cotton plants.
- **Fertilizer Recommendations**: Suggests appropriate fertilizers based on soil parameters (temperature, pH, nitrogen, etc.).
- **Crop Recommendations**: Provides crop suggestions tailored to the current soil conditions.
- **No Database Storage**: The project does not store any user data, ensuring privacy.
- **Interactive Interface**: The frontend is designed with React for a user-friendly experience.

🏗️ **Tech Stack**

- **Frontend**: React
- **Backend**: FastAPI
- **Machine Learning**: InceptionV3 (for disease detection)
- **Image Processing**: OpenCV, Pillow
- **Fertilizer and Crop Recommendations**: Based on soil parameters
- **Hosting**: Vercel (Frontend), any suitable cloud provider for FastAPI backend

📌 **API Endpoints**

- **Disease Detection Endpoint**  
  `POST /detect-disease` → Accepts an image of a cotton plant and returns the detected disease.
- **Fertilizer Recommendation Endpoint**  
  `POST /recommend-fertilizer` → Accepts soil parameters and returns recommended fertilizers.
- **Crop Recommendation Endpoint**  
  `POST /recommend-crop` → Accepts soil conditions and returns crop recommendations.

📂 **Project Structure**

````bash
backend/
├── app/
│   ├── main.py          # FastAPI application
│   ├── model.py         # Model loading and prediction logic
│   └── utils.py         # Helper functions for image processing and recommendations
├── requirements.txt     # Backend dependencies
└── Dockerfile           # Docker configuration for backend

frontend/
├── src/
│   ├── components/      # React components for UI
│   ├── pages/           # React pages
│   └── styles/          # Styling using CSS
├── public/              # Static assets
└── package.json         # Frontend dependencies

# Setup & Installation

## Prerequisites
Before you start, ensure you have the following installed on your machine:
- Python 3.8+
- Node.js 14+
- npm (Node Package Manager)
- Git

## 1. Clone the Repository
Start by cloning the repository to your local machine:
```bash
git clone https://github.com/VedankWakalkar/Cotton_Disease_Detection
cd cotton-disease-detection

Backend Setup (FastAPI)
Navigate to the backend directory:

cd backend
Install the backend dependencies using pip:

pip install -r requirements.txt
Run the FastAPI backend server:

uvicorn app.main:app --reload
Your backend server should now be running locally at http://localhost:8000.

Frontend Setup (React)
Navigate to the frontend directory:

cd frontend
Install the frontend dependencies using npm:

npm install
Start the React development server:

npm start
Your frontend application should now be running at http://localhost:3000.

Accessing the Application
Open your browser and go to http://localhost:3000 to access the frontend.
The backend is available at http://localhost:8000.
````
