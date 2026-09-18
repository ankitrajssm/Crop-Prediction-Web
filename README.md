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
**How to Run the Project:**

1. **Generate the Models:** Open and run all the cells in `Crop_Recommendation_System.ipynb`. This will train the machine learning model and automatically generate the required `model.pkl`, `standscaler.pkl`, and `minmaxscaler.pkl` files in your directory.
2. **Start the Server:** Once the `.pkl` files are created, run the Flask backend by typing `python app.py` in your terminal.
3. **View the App:** Open your web browser and go to `http://127.0.0.1:5000/` to use the platform.
