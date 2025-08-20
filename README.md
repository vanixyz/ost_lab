#This is the readme file and bob will work on it

//CALORIE ESTIMATION & RECOGNITION HEALTH TRACKING WEBAPP

#Eatly – AI Calorie Estimator (Web)

Snap a photo of your meal and get an approximate calorie & macro breakdown. NutriSnap uses computer vision to detect foods, asks smart clarifying questions when it’s unsure (e.g., **atta roti vs maida roti**), estimates portion size, and pulls nutrition data from free sources.

---

## ✨ Features

- 📸 **Web camera/upload** (mobile & desktop supported)
- 🔎 **Food detection** with YOLOv8 (free & open-source)
- 💬 **Chatbox-style clarification** when confidence is low
- ⚖️ **Portion estimation** via simple image heuristics (OpenCV)
- 🧮 **Calories & macros** (Protein/Carbs/Fat) via USDA FoodData Central (free API)
- 💾 **Meal history** (local storage / Firebase free tier)
- 📱 Mobile-friendly UI; can be made installable as a **PWA**

---

## 🧠 How it works
[User (camera/upload)]
|
v
[YOLOv8 Detection] ----> If low confidence or ambiguous
| |
| v
| [Chatbox Clarification]
v
[Portion Estimation (OpenCV)]
|
v
[USDA Nutrition Lookup]
|
v
[Calorie & Macro Calculation]
|
v
[Results Display]


---

## 🧰 Tech Stack

- **Frontend/Web App:** Streamlit (Python)  
- **CV / ML:** Ultralytics YOLOv8 (PyTorch), OpenCV  
- **Nutrition Data:** USDA FoodData Central API (free)  
- **Training (optional):** Google Colab (free GPU)  
- **Deployment (free):** Streamlit Community Cloud or Hugging Face Spaces

---

## 📂 Project Structure



## 📂 Project Structure

eatly/
├─ app.py # Streamlit app (UI + flow)
├─ yolov8/ # Model files, training utils
│ ├─ model.yaml
│ ├─ best.pt # Trained weights (place here)
├─ utils/
│ ├─ detection.py # YOLO inference helpers
│ ├─ portion.py # OpenCV-based portion estimation
│ ├─ nutrition.py # USDA API wrapper
│ ├─ clarifier.py # Low-confidence Q&A logic
│ └─ mapping.py # Label ↔ USDA FDC mapping
├─ data/
│ ├─ samples/ # Sample test images
│ └─ datasets.md # Notes on Food-101, Indian food datasets
├─ requirements.txt
├─ .env.example # USDA_API_KEY=...
├─ README.md
└─ LICENSE



