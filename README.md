# AI-Exercise-Posture-Detection
AI-powered exercise posture detection system using computer vision to analyze body movements in real-time. It tracks key joints, evaluates form during workouts, and provides feedback to improve accuracy, enhance performance, and reduce injury risk without the need for a personal trainer.

🧠 AI Exercise Posture Detection

FastAPI + MediaPipe + WebSocket | Real-time Posture Analysis

This project is an AI-powered exercise posture detection system that uses your webcam to analyze body movements in real-time. It streams video frames to a FastAPI backend via WebSocket and uses MediaPipe Pose to detect and evaluate posture.

🚀 Features
Real-time posture detection using webcam
WebSocket-based fast frame streaming
Body landmark detection with MediaPipe
Lightweight FastAPI backend
Easy local setup

📁 Project Structure
ai-exercise-app/
├── main.py   # FastAPI backend

├── requirements.txt             # Python dependencies

├── ai_engine/

│   ├── __init__.py

│   └── pose_analyzer.py         # Pose detection logic

├── static/

│   └── index.html               # Frontend webcam client

└── uploads/ (optional)

🛠️ Requirements
Python 3.10 or 3.11
❗ Do NOT use Python 3.13 (MediaPipe not supported)
⚙️ Setup Instructions
1️⃣ Clone or Create Project
cd path/to/your/projects
mkdir ai-exercise-app && cd ai-exercise-app

Add all required files (main.py, requirements.txt, etc.)

2️⃣ Create Virtual Environment

Windows:

py -3.10 -m venv ai_posture_env
.\ai_posture_env\Scripts\activate
3️⃣ Install Dependencies
pip install -r requirements.txt

If missing, create requirements.txt:

fastapi
uvicorn
mediapipe
opencv-python
websockets
aiofiles
python-multipart
4️⃣ Run Backend Server
uvicorn main:app --reload

Open in browser:

http://127.0.0.1:8000
5️⃣ Start Webcam Client
http://localhost:8000/static/index.html

Allow camera access.
Frames will be sent every 300ms to the backend.

📡 How It Works
index.html captures webcam frames
Frames are sent via WebSocket to FastAPI
Backend decodes frames and processes them using MediaPipe
Pose landmarks are detected and response is sent back
🧪 Debug Tips
Check backend logs if WebSocket disconnects
Ensure base64 image format is correct (remove header)
Add print statements in WebSocket handler
🚀 Future Improvements
Draw landmarks on frontend (Canvas)
Add posture feedback (e.g., “bend knees more”)
Mobile camera integration
Performance analytics dashboard
