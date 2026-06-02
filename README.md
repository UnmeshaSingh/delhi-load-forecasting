# Delhi Load Forecasting System ⚡
### Built for Smart India Hackathon (SIH)

A full-stack AI-powered web application that predicts electricity load requirements 
across regions in India using a SARIMAX machine learning model, built as part of 
the Smart India Hackathon.

🔗 **Live Demo:** https://unmeshasingh.github.io/delhi-load-forecasting  
🤖 **Backend API:** https://delhi-load-forecasting-1.onrender.com

---

## 👥 Team Members

- **Unmesha Singh**
- Ishita Pradhan
- Satvik Behera
- Sushree Sucharita Behera
- Shakti Siddharth Ray

---

## 📌 About the Project

This project was built for the **Smart India Hackathon (SIH)** — India's biggest 
hackathon organized by the Government of India. Our problem statement focused on 
predicting electricity load requirements across several regions in India to help 
power distribution companies plan and manage energy supply more efficiently.

The system uses real historical power load data from Delhi and a **SARIMAX 
(Seasonal AutoRegressive Integrated Moving Average with eXogenous variables)** 
model to forecast electricity demand based on date, time, temperature, rainfall, 
wind speed, and holiday information.

---

## ✨ Features

- 📊 **Live ML Predictions** — Real-time electricity load forecasting powered by SARIMAX model
- 🕐 **Past Load Data Lookup** — Query historical power consumption by date and time
- 🌡️ **Weather-aware Predictions** — Model factors in temperature, rain, and wind data
- 📅 **Holiday Detection** — Accounts for holidays in load prediction
- 🗺️ **Load Profile Analysis** — Visual breakdown of Delhi's power consumption patterns
- 💡 **AI-Based Solution Page** — Explains the ML approach and methodology
- 📱 **Responsive Design** — Works on desktop and mobile

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Python, FastAPI |
| ML Model | SARIMAX (statsmodels) |
| Data Processing | Pandas, NumPy |
| Deployment | GitHub Pages (frontend), Render (backend) |

---

## 🤖 ML Model Details

- **Algorithm:** SARIMAX — Seasonal AutoRegressive Integrated Moving Average with eXogenous variables
- **Order:** (5, 0, 2) with seasonal order (0, 0, 2, 4)
- **Features used:** Temperature, Rainfall, Wind Gust Speed, Rain %, IsHoliday, Load Shift 1, Load Shift 2
- **Dataset:** Real historical Delhi power load data with datetime index
- **Train/Test Split:** 80% training, 20% testing (chronological split)

---

## 📁 Project Structure

delhi-load-forecasting/
├── index.html              # Home page with live prediction widget
├── load-profile.html       # Load profile analysis page
├── challenges.html         # Power challenges in Delhi
├── solution.html           # AI-based solution explanation
├── about.html              # About the team
├── contact.html            # Contact page
├── css/
│   └── styles.css          # All page styles
├── js/
│   └── scripts.js          # Slider, form handling, API calls
├── ml/
│   ├── only4.py            # SARIMAX model training and prediction
│   └── SIH Data.csv        # Historical Delhi power load dataset
└── main.py                 # FastAPI backend with /predict/ and /getval/ endpoints

---

## 🚀 How to Run Locally

**Frontend:**
```bash
# Just open index.html in your browser
# No installation needed
```

**Backend:**
```bash
# Clone the repository
git clone https://github.com/UnmeshaSingh/delhi-load-forecasting.git
cd delhi-load-forecasting

# Install dependencies
pip install fastapi uvicorn pandas scikit-learn statsmodels

# Run the server
uvicorn main:app --host 0.0.0.0 --port 8000

# Visit http://localhost:8000
```

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Welcome message |
| POST | `/getval/` | Get current time power usage prediction |
| POST | `/predict/` | Get historical load data for a specific date and time |

---

## 🏆 Smart India Hackathon

Smart India Hackathon is a nationwide initiative by the **Government of India** 
to provide students a platform to solve pressing problems. Our team was selected 
to build a solution for predicting electricity requirements across several regions 
in India — helping power distribution companies reduce waste and plan supply more 
effectively.

---

## 🔮 Future Plans

- Expand predictions to cover multiple states across India
- Integrate real-time weather API for live forecasting
- Add visual charts showing predicted vs actual load
- Build a more accurate deep learning model (LSTM)
- Add admin dashboard for power distribution companies

---

## 🤝 Acknowledgements

Thank you to **Smart India Hackathon** and the **Government of India** for the 
opportunity, and to our mentors for their guidance throughout the project.
