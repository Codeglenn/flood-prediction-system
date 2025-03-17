# 🌊 Flood Prediction System  

This **Flood Prediction System** is a **Flask-based web application** that predicts **flood risk** using **real-time weather data and machine learning**. It integrates **MongoDB for storage, Visual Crossing API for weather data, and APScheduler for automated cleanup**.  

---

## 🚀 Features  
✅ **Predict Flood Risk** based on real-time weather conditions  
✅ **Machine Learning Model (Random Forest Classifier)** for risk assessment  
✅ **MongoDB Integration** for storing past flood predictions  
✅ **Weather API (Visual Crossing)** for real-time data  
✅ **Automatic Data Cleanup** (Deletes old records after 7 days)  
✅ **Past Predictions History** with search & filtering  
✅ **User-Friendly Dashboard** with navigation buttons  
✅ **Search by City & Date** in prediction history  

---

## 📌 Installation Guide  

### **1️⃣ Install Python (If Not Installed)**  
- ✅ **Required Version:** `Python 3.8+`  
- 📌 **[Download Python](https://www.python.org/downloads/)**  

### **2️⃣ Clone This Repository**  
```sh
git clone https://github.com/Codeglenn/flood-prediction-system.git
cd flood-prediction-system
```

### **3️⃣ Install Dependencies**  
```sh
pip install -r requirements.txt
```
or manually install:  
```sh
pip install flask pymongo joblib pandas numpy scikit-learn requests flask-caching apscheduler python-dotenv
```

### **4️⃣ Set Up MongoDB**  

#### **Local Installation (Recommended)**
- 📌 **[Download MongoDB](https://www.mongodb.com/try/download/community)**  
- ✅ **Run MongoDB Locally:**  
  ```sh
  mongod --dbpath /path/to/database
  ```

#### **Using MongoDB Atlas (Cloud)**
- Sign up at: **[MongoDB Atlas](https://www.mongodb.com/atlas)**  
- Set up a free database  
- Update `.env` with your **MongoDB URI**:  
  ```txt
  MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/flood_db?retryWrites=true&w=majority
  ```

### **5️⃣ Configure Environment Variables**
Create a `.env` file in the project directory and add:  
```txt
MONGO_URI=mongodb://localhost:27017/flood_db
VISUAL_CROSSING_API_KEY=your_api_key_here
```
📌 **Get a free API key from:** [Visual Crossing Weather API](https://www.visualcrossing.com/)  

### **6️⃣ Run the Application**
```sh
python app.py
```
💡 Flask should now start, and the app will be available at:  
👉 **`http://127.0.0.1:5000/`**  

---

## 📊 How It Works  
1️⃣ **User enters a city** → The app fetches real-time weather.  
2️⃣ **ML model predicts flood risk** using weather & city data.  
3️⃣ **Prediction is stored in MongoDB** for future reference.  
4️⃣ **User can view past predictions** via the history page.  
5️⃣ **Old data is auto-deleted** after 7 days (background task).  

---

## 🔥 Technologies Used  
| Component              | Technology  |
|------------------------|------------|
| **Backend Framework**  | Flask (Python) |
| **Machine Learning**   | Scikit-Learn (RandomForestClassifier) |
| **Database**          | MongoDB (PyMongo) |
| **Weather API**       | Visual Crossing API |
| **Job Scheduler**     | APScheduler (for automatic cleanup) |
| **Caching**          | Flask-Caching |
| **Frontend**          | HTML, Tailwind CSS, Bootstrap, Font Awesome |

---

## 🎯 Future Enhancements  
💡 **Export Prediction History to CSV**  
💡 **Multiple City Predictions in One Request**  
💡 **Additional Features (Wind Speed, Past Flood Events)**  
💡 **Dashboard with Graphs & Charts for Flood Trends**  

---

## 🤝 Contributing  
🔹 Fork this repository.  
🔹 Create a new branch: `git checkout -b feature-branch`  
🔹 Make changes and commit: `git commit -m "Added a new feature"`  
🔹 Push to the branch: `git push origin feature-branch`  
🔹 Submit a Pull Request for review.  

---

## 📝 License  
This project is open-source and available under the **MIT License**.  

---

## 📞 Contact  
For questions or contributions, feel free to reach out:  
📧 **Email:** kiruiglen@gmail.com  
🐙 **GitHub:** [kiruiglen](https://github.com/Codeglenn)  
