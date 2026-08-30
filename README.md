# 🌾 Crop Recommendation Web Platform

> **Hey there! 👋** I am currently cleaning up the Flask server code and frontend files. The full repository will be live soon!

## 📌 What is this?
This is a full-stack web application that predicts the best crop for a farmer to plant based on real-time soil and weather data. It serves the same Machine Learning model I used in my Android app, but wrapped in a clean, browser-friendly web interface.

## 🛠️ Tech Stack
* **Backend:** Python, Flask
* **Machine Learning:** Scikit-learn, NumPy
* **Frontend:** HTML, CSS, JavaScript

## ⚙️ How It Works
1. **The Web Interface:** A user visits the site and fills out a simple HTML form with 7 values (Nitrogen, Phosphorus, Potassium, Temperature, Humidity, pH, and Rainfall).
2. **The Flask Server:** When the user hits submit, a POST request is sent to the Flask backend (`app.py`).
3. **Data Processing:** The server converts the form data into a NumPy array and passes it through my pre-trained data scalers (`standscaler.pkl` and `minmaxscaler.pkl`).
4. **The Prediction:** The processed data is fed into the `model.pkl` classifier. 
5. **The Output:** The Python script injects the predicted crop name back into the HTML template (`index.html`) so the user sees their result instantly.

## 📂 What's coming to this repo soon:
```text
📦 Crop-Prediction-Web
 ┣ 📂 templates                  # HTML/JS files for the frontend
 ┣ 📂 static                     # CSS styling and images
 ┣ 📜 app.py                     # The main Flask server script
 ┣ 📜 model.pkl                  # Trained Scikit-learn classifier
 ┣ 📜 standscaler.pkl            # Standardization weights
 ┗ 📜 minmaxscaler.pkl           # MinMax scaling weights
