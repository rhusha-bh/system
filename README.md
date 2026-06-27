````markdown
# 🤟 Deep Learning Based Real-Time Sign Language Recognition

A real-time Sign Language Recognition system developed using **PyTorch, FastAPI, OpenCV, and Deep Learning**. The application captures hand gestures through a webcam and predicts sign language characters in real time using a trained deep learning model.

---

## 📌 Features

- 🔤 Real-time Sign Language Recognition
- 📷 Live Webcam Detection
- 🧠 Deep Learning Model (PyTorch)
- ⚡ FastAPI Backend
- 🌐 Browser-Based Frontend
- 🎯 Fast and Accurate Predictions
- 💻 Simple Local Deployment

---

## 🛠 Technologies Used

- Python
- PyTorch
- FastAPI
- Uvicorn
- OpenCV
- NumPy
- Pillow
- HTML
- CSS
- JavaScript

---

# 📂 Project Structure

```text
Project/
│
├── requirements.txt
├── .venv/
│
├── src/
│   │
│   ├── backend/
│   │   ├── main.py
│   │   ├── model.pth
│   │   └── ...
│   │
│   ├── frontend/
│   │   └── html/
│   │       └── recognition.html
│   │
│   └── training/
│       ├── train.py
│       └── ...
│
└── README.md
````

---

# 🚀 Getting Started

## 1️⃣ Clone the Repository

```powershell
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

Open the project folder.

```powershell
cd Project
```

---

## 2️⃣ Create a Virtual Environment

Run the following command only once.

```powershell
python -m venv .venv
```

---

## 3️⃣ Activate the Virtual Environment

### Windows PowerShell

```powershell
.\.venv\Scripts\Activate.ps1
```

If activated successfully, your terminal should display:

```text
(.venv)
```

---

## 4️⃣ Install Dependencies

Run this command only once.

```powershell
pip install -r requirements.txt
```

---

## 5️⃣ Train the Model (Optional)

Skip this step if **model.pth** already exists.

```powershell
cd src\training

python train.py
```

The trained model will be saved as:

```text
src/backend/model.pth
```

---

# ▶ Running the Application

Open **two terminal windows**.

---

## 🖥 Terminal 1 – Start Backend

Activate the virtual environment.

```powershell
cd Project

.\.venv\Scripts\Activate.ps1
```

Go to the backend folder.

```powershell
cd src\backend
```

Run the FastAPI server.

```powershell
uvicorn main:app --host 127.0.0.1 --port 8000 --reload
```

If everything is working correctly, you should see:

```text
INFO:     Uvicorn running on http://127.0.0.1:8000
INFO:     Application startup complete.
```

Leave this terminal running.

---

## 🌐 Terminal 2 – Start Frontend

Activate the virtual environment.

```powershell
cd Project

.\.venv\Scripts\Activate.ps1
```

Navigate to the frontend folder.

```powershell
cd src\frontend
```

Start the local web server.

```powershell
py -m http.server 5500
```

Leave this terminal running.

---

# 🌍 Open the Application

Open your browser and visit:

```text
http://127.0.0.1:5500/html/recognition.html
```

Allow camera access when prompted.

The application will begin recognizing sign language gestures in real time.

---

# 🔄 Running the Project Again

Once everything has been installed, you only need to run these commands.

### Backend

```powershell
cd Project

.\.venv\Scripts\Activate.ps1

cd src\backend

uvicorn main:app --host 127.0.0.1 --port 8000 --reload
```

---

### Frontend

```powershell
cd Project

.\.venv\Scripts\Activate.ps1

cd src\frontend

py -m http.server 5500
```

Open:

```text
http://127.0.0.1:5500/html/recognition.html
```

---

# ⚠ Common Issues

## PowerShell Execution Policy Error

Run:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Then activate the virtual environment again.

```powershell
.\.venv\Scripts\Activate.ps1
```

---

## Missing Python Packages

Reinstall all dependencies.

```powershell
pip install -r requirements.txt
```

---

## WebSocket Warning

If you see:

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

Make sure you are inside:

```text
src/backend
```

before running:

```powershell
uvicorn main:app --reload
```

---

## Frontend Not Loading

Ensure the HTTP server is running on port **5500**.

Open:

```text
http://127.0.0.1:5500/html/recognition.html
```

---

# 📝 Notes

* Keep both terminal windows open while using the application.
* Ensure your webcam is connected and accessible.
* Allow browser permission for camera access.
* Retraining the model is only necessary if `model.pth` is missing or you want to generate a new model.

---

# 👨‍💻 Developed By

**Rhushabh Gaikwad**

Bachelor of Engineering (Computer Engineering)

Savitribai Phule Pune University

---

## ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub.

```
```
