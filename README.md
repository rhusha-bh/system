Deep Learning Based Real-Time Sign Language Recognition
Requirements

Before running the project, make sure the following are installed:

Python 3.10 or later
pip
Git (optional)
Webcam
Project Folder
Project/
│
├── requirements.txt
├── .venv/
├── src/
│   ├── backend/
│   │     ├── main.py
│   │     └── model.pth
│   │
│   ├── frontend/
│   │     └── html/
│   │           └── recognition.html
│   │
│   └── training/
│         └── train.py
STEP 1 - Open PowerShell

Open Windows PowerShell or VS Code Terminal.

Navigate to the project folder.

cd C:\Users\<YourUsername>\Desktop\Project

Replace <YourUsername> with your Windows username.

STEP 2 - Create Virtual Environment (First Time Only)
python -m venv .venv

This creates a virtual environment named .venv.

STEP 3 - Activate Virtual Environment
cd C:\Users\<YourUsername>\Desktop\Project
.\.venv\Scripts\Activate.ps1

If activated successfully, the terminal will show:

(.venv)

before the command prompt.

STEP 4 - Install Required Packages (First Time Only)
pip install -r C:\Users\<YourUsername>\Desktop\Project\requirements.txt

Wait until all packages are installed.

STEP 5 - Train the Model (Optional)

Run this only if model.pth is missing or you want to retrain the model.

cd C:\Users\<YourUsername>\Desktop\Project\src\training

python train.py

This creates:

Project
└── src
    └── backend
        └── model.pth

If model.pth already exists, skip this step.

STEP 6 - Start Backend Server

Open a new terminal.

Activate the virtual environment again.

cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1

Navigate to backend.

cd src\backend

Run FastAPI.

uvicorn main:app --host 127.0.0.1 --port 8000 --reload

If successful, you should see something similar to:

INFO: Uvicorn running on http://127.0.0.1:8000
Application startup complete.

Keep this terminal running.

STEP 7 - Start Frontend

Open another terminal.

Activate the virtual environment.

cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1

Navigate to the frontend folder.

cd src\frontend

Start the HTTP server.

py -m http.server 5500

You should see:

Serving HTTP on 0.0.0.0 port 5500...

Keep this terminal running.

STEP 8 - Open the Application

Open your browser and go to:

http://127.0.0.1:5500/html/recognition.html

Allow camera permission when prompted.

The application will start detecting sign language gestures.

Running the Project Next Time

Only perform these steps:

Terminal 1
cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1

cd src\backend

uvicorn main:app --host 127.0.0.1 --port 8000 --reload
Terminal 2
cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1

cd src\frontend

py -m http.server 5500

Open:

http://127.0.0.1:5500/html/recognition.html
Common Issues
Virtual Environment Not Activated

Run:

.\.venv\Scripts\Activate.ps1
Execution Policy Error

If PowerShell blocks activation:

Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

Then activate again.

Missing Packages

Install requirements again:

pip install -r requirements.txt
WebSocket Warning

If you see:

No supported WebSocket library detected

Install:

pip install "uvicorn[standard]"

or

pip install websockets wsproto
Backend Not Starting

Ensure you are inside:

src/backend

before running:

uvicorn main:app --reload
Frontend Not Opening

Make sure the HTTP server is running on port 5500 and open:

http://127.0.0.1:5500/html/recognition.html
Notes
Keep both backend and frontend terminals running while using the application.
Ensure the webcam is connected and browser camera permissions are granted.
Retraining the model is only required if model.pth is missing or updated.
Do not close the backend or frontend terminals while the application is in use.
