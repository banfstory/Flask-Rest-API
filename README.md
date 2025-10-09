# 🧩 REST-API-FLASK

This repository contains the **Flask RESTful API** for the Forum Web App.  
It serves as the backend for the [React Forum Frontend](https://github.com/banfstory/React-Forum-Frontend).

The API handles all server-side operations — user authentication, forums, posts, and comments — and communicates with the React frontend via HTTP requests.

## 📦 Related Repositories

- **Frontend (React App):** [React-Forum-Frontend](https://github.com/banfstory/React-Forum-Frontend)

## 🖥️ Running the Flask API (Windows Instructions)

Follow these steps to set up and run the Flask API locally:

### 1. Create a virtual environment
Create a new virtual environment inside the project folder:
```bash
python -m venv venv
```
This creates a folder named `venv` that keeps all project dependencies isolated.

### 2. Activate the virtual environment
```bash
venv\Scripts\activate
```
When activated, your terminal prompt will show `(venv)`.

### 3. Install required libraries
Install all dependencies listed in requirements.txt:
```
pip install -r requirements.txt
```
This ensures Flask, Flask-CORS, SQLAlchemy, and other required libraries are installed.

### 4. Navigate to the Flask app directory
```
cd flask_api
```

### 5. Run the Flask server
```
python run.py
```
The local server will start at:
👉 http://127.0.0.1:5000


## ⚙️ Changing the Port Number
By default, Flask runs on port 5000.
To change it:
### 1. Open the file:
```
flask_api/run.py
```
### 2. Locate the line:
```python
app.run(debug=True, port=5000)
```

### 3. Change the port number (e.g., 8000):
```python
app.run(debug=True, port=8000)
```

## 🔗 Updating the Frontend API URL
If you change the Flask port, you must also update the frontend API URL so both apps communicate properly.

In the **frontend repository**:  
👉 [React-Forum-Frontend](https://github.com/banfstory/React-Forum-Frontend)

### 1. In your React frontend repo, open:
```
src/mixin/default_API_URL.js
```
### 2. Update the first line:
```javascript
const REST_API_URL = 'http://127.0.0.1:5000/api/';
```
→ to match your new port:
```
const REST_API_URL = 'http://127.0.0.1:8000/api/';
```

## 📜 License
This project is licensed under the [MIT License](https://github.com/banfstory/Flask-Rest-API/blob/main/LICENSE).
