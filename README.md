# 🔭 Exoplanet AI Explorer

A 3D interactive web application that predicts and visualizes exoplanets based on input features.  
Built with **FastAPI (backend)** + **Three.js (frontend)** + **Machine Learning model**.

---

## 🚀 Features
- 🌍 Start in the **Solar System** (Sun + Earth orbiting).  
- ✨ Warp to a new **dimension** when exploring exoplanets.  
- 🪐 Visualize host star & orbiting planet with:
  - Realistic star textures (Sun-like)  
  - Temperature-based star colors (red → orange → yellow → white → blue)  
  - Glow effects for hot stars (A/B/O class)  
- 📡 Input astrophysical parameters:
  - Orbital period  
  - Transit duration  
  - Planet radius  
  - Transit depth  
  - Impact parameter  
  - SNR  
  - Stellar effective temperature (Teff)  
  - log g  
  - Stellar radius  
- 🤖 ML backend predicts if the candidate is:
  - **Confirmed** ✅  
  - **Candidate** ⚠️  
  - **False Positive** ❌  

---

## 📂 Project Structure
exoplanet-ai/
│
├── src/
│ ├── app/
│ │ └── api.py # FastAPI backend (prediction endpoint)
│ └── model.pkl # Trained ML model
│
├── public/
│ └── textures/ # Textures (Sun, Earth, etc.)
│
├── index.html # Frontend UI
├── src/main.js # Three.js visualization + API calls
├── requirements.txt # Python dependencies
└── README.md # This file

---

## ⚙️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/exoplanet-ai.git
cd exoplanet-ai
python -m venv .venv
source .venv/bin/activate   # (Linux/Mac)
.venv\Scripts\activate      # (Windows)

pip install -r requirements.txt

# Run the API server
uvicorn src.app.api:app --host 127.0.0.1 --port 8000 --reload
The API will now run at:
👉 http://127.0.0.1:8000/docs

Setup frontend (Three.js)

Open a second terminal in the project folder:

# If using live-server (recommended)
npx live-server


Then go to 👉 http://127.0.0.1:8080
 (or the port live-server gives).
