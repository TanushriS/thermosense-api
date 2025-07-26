# 🔌 ThermoSense API

This is the **ML + GPT-2 powered FastAPI backend** for the ThermoSense platform.

### 📡 Live Link 
👉 [https://thermosense.com](https://thermosense-ui-psi.vercel.app/)

### 🖥️ Live dashboard
![Live Dashboard](https://github.com/TanushriS/assets/blob/main/dashboard.png)

---

## 🧠 What It Does

- ✅ Predicts battery health impact using a trained `RandomForestRegressor`
- 🧠 Generates natural language safety tips using **GPT-2**
- ⚠️ Classifies alert levels: `safe`, `warning`, `danger`

---

## 🔍 Sample Request (POST)

```json
{
  "battery_temp": 38.5,
  "ambient_temp": 32.0,
  "device_state": "charging"
}
```

## ✅ Sample Response

```json
{
  "predicted_health_impact": 0.08672,
  "alert_level": "warning",
  "natural_language_tip": "Warning: Battery is getting warm. Move device to cooler location and avoid heavy usage.",
  "optional_action": "Monitor temperature and reduce intensive tasks"
}
```

---

## 🧰 Tech Stack

- FastAPI
- Scikit-learn (ML model)
- Hugging Face Transformers (GPT-2)
- Python 3.10+
- Deployed on **Render.com** / **Hugging Face Spaces**

---

## 📸 API Demo Screenshots

### 🔄 Rendor API Call (via /api/advice)
![API Response](https://github.com/TanushriS/assets/blob/main/Rendor%20API%20Live.png)

### 🖥️ Hugging Face Spaces Live
![Live Space](https://github.com/TanushriS/assets/blob/main/Hugging%20Face%20API%20Live.png)
### 🖥️ Hugging Face API Interface
![Live Space](https://github.com/TanushriS/assets/blob/main/HF%20API%20Interface.png)


## 🚀 How to Run Locally

```bash
git clone https://github.com/TanushriS/thermosense-api.git
cd thermosense-api
pip install -r requirements.txt
uvicorn api:app --reload
```

---

## 📁 Files

```
📦thermosense-api
 ┣ 📜 api.py
 ┣ 📜 main.py
 ┣ 📜 transformer_t5_test.py
 ┣ 📜 thermosense_test_data.csv
 ┗ 📜 requirements.txt
```

---

## 📌 Endpoints

| Method | Route        | Description                  |
|--------|--------------|------------------------------|
| POST   | /api/advice  | Predicts health & advice     |

---

## 👩‍💻 Author

**Tanushri Sukhwal**  
[GitHub Profile](https://github.com/TanushriS) | [LinkedIn](https://www.linkedin.com/in/tanushri-sukhwal-67131728a)
