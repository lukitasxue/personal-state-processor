# personal-state-processor
Personal state processor Project

## Project Description

The **Personal State Processor** is a **self-tracking and analysis system** designed to monitor and predict personal well-being using **real-time data collection and machine learning**. This project aims to gather insights from various aspects of daily life, including **facial expressions, sleep patterns, nutrition, exercise, and schedules**, to analyze trends and provide useful predictions.

### **Project Goal**

The goal of this project is to create a **personalized analytical tool** that helps users understand how different factors (such as sleep, food intake, and physical activity) influence their **mood, energy levels, and overall well-being**. By leveraging **data visualization and machine learning**, the system will provide **predictions and insights** on a short-term basis (e.g., **1-day, 3-day, and 7-day forecasts**), helping users optimize their lifestyle and improve their **productivity, health, and mental state**.

Visit notion for a better view

Core Components & Implementation Ideas

🔹 Face Real-Time Analysis (Emotion Detection)

**Tools & Methods**:
- Use **OpenCV** (for real-time camera processing).
- Use **DeepFace** or **MediaPipe Face Mesh** to analyze facial expressions.
- Store expressions with timestamps to track mood patterns.

**Approach:**
- Start with a basic **Webcam Face Emotion Detector**.
- Save timestamps & detected emotions in a database.

---

🔹 Sleep Tracking

**Options:**
1. **Manual Input** (Easiest) – Just input sleep hours each day.
2. **Use an External App** – Fitbit, Apple Health, or Google Fit APIs to fetch sleep data.
3. **Build a Sleep App (Advanced)** – Use a microphone to detect breathing patterns.

---

**🔹 Food Tracking**

**Methods:**
- Use **Nutrition API** (e.g., Edamam, USDA API) to fetch nutritional details of meals.
- Manually input food details and let the system fetch calories & nutrients.

**Example:**
1. User enters a meal name (`"Grilled Chicken with Rice"`).
2. API fetches nutritional details.
3. Data is stored in the database.

---

**🔹 Exercise Tracking**

**Approach:**
- Simple manual input (e.g., `"Run 6km at 9m/km"`).
- Store workout types and durations in the database.
- Later: Use **ML to analyze patterns & suggest workouts**.

---

**🔹 Schedule Tracking (Exams, Classes, Work)**
**Approach:**

- Manually input events (date, time, type).
- Allow visualization of daily/weekly schedules.
- Future: Use ML to analyze stress levels based on workload.

---

**🔹 Predictive & Machine Learning Features**

1. **Personal Humor Prediction** 🧑‍🎤
    - Uses **Facial Expressions + Sleep + Exercise + Food Intake**.
    - ML Model: Sentiment Analysis + Regression.
2. **Personal Battery (Energy Level)** 🔋
    - Uses **Sleep + Exercise + Food + Schedule Stress**.
    - ML Model: Regression Model predicting energy for the day.
3. **Extra ML Insights**
    - Sleep quality based on personal patterns.
    - Suggested exercise based on past routines.
    - Stress analysis based on **workload vs. sleep vs. emotions**.

---

**4. Visualization & User Interface**
- **Dashboard UI:**
    - Show raw data (e.g., sleep, food, exercise).
    - Show ML predictions (e.g., mood trends, energy levels).
- **Graphing Libraries:**
    - Use **Chart.js**, **D3.js**, or **Recharts** for data visualization.

---

## **5. Tech Stack**

Tools idea given by chatGPT (see which one is better)
| Feature | Tools & Libraries |
| --- | --- |
| **Face Analysis** | OpenCV, DeepFace, MediaPipe |
| **Sleep Tracking** | Manual Input, Google Fit API |
| **Food Tracking** | Edamam API, USDA API |
| **Exercise Tracking** | Manual Input, Firebase or SQLite |
| **Schedule Tracking** | Local DB (IndexedDB, Firebase, PostgreSQL) |
| **ML Predictions** | Scikit-Learn, TensorFlow, Pandas |
| **Visualization** | Chart.js, D3.js, Recharts |
