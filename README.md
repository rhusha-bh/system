# 🤟 Deep Learning Based Real-Time Sign Language Recognition

A real-time Sign Language Recognition system using **Deep Learning, PyTorch, FastAPI, OpenCV, and HTML/CSS/JavaScript**.

---

# 📋 Requirements

Before running the project, make sure the following are installed:

* Python 3.10 or later
* pip
* Git *(Optional)*
* Webcam

---

# 📁 Project Structure

```text
Project/
│
├── requirements.txt
├── .venv/
├── src/
│   ├── backend/
│   │   ├── main.py
│   │   └── model.pth
│   │
│   ├── frontend/
│   │   └── html/
│   │       └── recognition.html
│   │
│   └── training/
│       └── train.py
```

---

# 🚀 Installation Guide

## Step 1 - Open PowerShell

Open **Windows PowerShell** or the **VS Code Terminal**.

Navigate to the project directory.

```powershell
cd C:\Users\<YourUsername>\Desktop\Project
```

> Replace `<YourUsername>` with your Windows username.

---

## Step 2 - Create a Virtual Environment *(First Time Only)*

```powershell
python -m venv .venv
```

This creates a virtual environment named **.venv**.

---

## Step 3 - Activate the Virtual Environment

```powershell
cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1
```

If activation is successful, your terminal will display:

```text
(.venv)
```

before the command prompt.

---

## Step 4 - Install Required Packages *(First Time Only)*

```powershell
pip install -r C:\Users\<YourUsername>\Desktop\Project\requirements.txt
```

Wait until all required packages are installed.

---

## Step 5 - Train the Model *(Optional)*

Run this step **only if `model.pth` is missing** or you want to retrain the model.

```powershell
cd C:\Users\<YourUsername>\Desktop\Project\src\training

python train.py
```

The training process will generate:

```text
Project
└── src
    └── backend
        └── model.pth
```

> **Note:** If `model.pth` already exists, you can skip this step.

---

# ▶️ Running the Application

The project requires **two terminals**.

---

## Terminal 1 - Start Backend Server

Open a new PowerShell window.

Activate the virtual environment.

```powershell
cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1
```

Navigate to the backend folder.

```powershell
cd src\backend
```

Start the FastAPI server.

```powershell
uvicorn main:app --host 127.0.0.1 --port 8000 --reload
```

If everything is working correctly, you should see something similar to:

```text
INFO: Uvicorn running on http://127.0.0.1:8000
Application startup complete.
```

Keep this terminal running.

---

## Terminal 2 - Start Frontend

Open another PowerShell window.

Activate the virtual environment.

```powershell
cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1
```

Navigate to the frontend folder.

```powershell
cd src\frontend
```

Start the HTTP server.

```powershell
py -m http.server 5500
```

You should see:

```text
Serving HTTP on 0.0.0.0 port 5500...
```

Keep this terminal running.

---

# 🌐 Open the Application

Open your web browser and visit:

```text
http://127.0.0.1:5500/html/recognition.html
```

Allow camera permission when prompted.

The application will begin recognizing sign language gestures in real time.

---

# 🔄 Running the Project Next Time

After the initial setup, you only need to run the following commands.

## Terminal 1

```powershell
cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1

cd src\backend

uvicorn main:app --host 127.0.0.1 --port 8000 --reload
```

---

## Terminal 2

```powershell
cd C:\Users\<YourUsername>\Desktop\Project

.\.venv\Scripts\Activate.ps1

cd src\frontend

py -m http.server 5500
```

Then open:

```text
http://127.0.0.1:5500/html/recognition.html
```

---

# ⚠️ Common Issues

## Virtual Environment Not Activated

Run:

```powershell
.\.venv\Scripts\Activate.ps1
```

---

## PowerShell Execution Policy Error

If PowerShell blocks activation, run:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Then activate the virtual environment again.

```powershell
.\.venv\Scripts\Activate.ps1
```

---

## Missing Packages

Install all dependencies again.

```powershell
pip install -r requirements.txt
```

---

## WebSocket Warning

If you receive the warning:

```text
No supported WebSocket library detected
```

Install:

```powershell
pip install "uvicorn[standard]"
```

or

```powershell
pip install websockets wsproto
```

---

## Backend Not Starting

Ensure you are inside the following directory:

```text
src/backend
```

before running:

```powershell
uvicorn main:app --reload
```

---

## Frontend Not Opening

Verify that the HTTP server is running on **port 5500**, then open:

```text
http://127.0.0.1:5500/html/recognition.html
```

---

# 📝 Notes

* Keep both backend and frontend terminals running while using the application.
* Ensure your webcam is connected.
* Allow browser camera permission when prompted.
* Retrain the model only if `model.pth` is missing or needs updating.
* Do not close either terminal while the application is running.

---
