# 🚀 Dynamic Pricing Optimization using Thompson Sampling

[![Python](https://img.shields.io/badge/Python-3.9+-blue)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-3.0-green)](https://flask.palletsprojects.com)
[![AI](https://img.shields.io/badge/AI-Thompson%20Sampling-orange)](https://en.wikipedia.org/wiki/Thompson_sampling)
[![Live](https://img.shields.io/badge/Local-127.0.0.1:5000-brightgreen)](http://127.0.0.1:5000)

---

## 🧠 Overview

**Intelligent pricing system** that **learns optimal price automatically** using **Bayesian Multi-Armed Bandit**.

**Problem solved:**  
> *How to find best price without knowing customer behavior upfront?*

**Solution:** **Thompson Sampling** - balances **exploration** (try new prices) + **exploitation** (use best known price).

---

## 🎯 What It Does
Input: Product (T-Shirt/Jeans/Shoes) + Day
AI Tests: 4 prices → Predicts demand → Picks revenue winner
Output: Optimal price + Live revenue tracking


**Real Example:**

T-Shirt → Tests ₹25,30,35,40
AI Learns: ₹35 gives ₹980 revenue (best!)
Dashboard: Live charts + ₹2,450 total revenue


---

## ⚙️ Key Features

| Feature | Status | Tech |
|---------|--------|------|
| **🎯 Dynamic Pricing** | ✅ Live | Thompson Sampling |
| **📈 Revenue Dashboard** | ✅ Real-time | Flask + Plotly |
| **💾 Sales Database** | ✅ Auto-save | SQLite |
| **⚡ Ultra Fast** | ✅ 6-50ms | LRU Cache |
| **🧮 Revenue Max** | ✅ Optimal | SciPy linprog |

---

## 🧪 Real-World Use Cases

### **1. E-commerce** 🛒
Test prices: ₹100, ₹120, ₹150
Learn: ₹120 → max revenue
Auto-adjust daily
### **2. Airlines** ✈️
Dynamic seat pricing by demand
Balance load factor + revenue
### **3. Uber** 🚗
Surge pricing simulation
Real-time demand adaptation

## 🛠️ Tech Stack
Backend: Flask 3.0.3 + Python
AI: Thompson Sampling + SciPy linprog
Demand: Poisson Distribution (λ=25)
Database: SQLite (pricing_data.db)
Frontend: HTML + Plotly Charts
Cache: LRU (256 entries)
Deploy: Render.com 


---

## ▶️ Run Locally (Your Folder)

```bash
# Your exact folder (no changes!)
cd "C:\Users\HP\OneDrive\Desktop\dynamic-pricing-project"

# Start
python app.py
```

**🌐 Dashboard:** `http://127.0.0.1:5000`
## 📁 **Complete Project Structure**
Dynamic-pricing-project/ ← Your main folder
│
├── app.py # 🚀 MAIN Flask API + AI Engine
│ - Complete web server
│ - Thompson Sampling AI
│ - All 5 API endpoints
│ - Database integration
│
├── dashboard.html # 🎨 Live Analytics Dashboard
│ - Beautiful purple UI
│ - Real-time charts (Plotly)
│ - Price optimizer form
│ - Live sales table
│ - Revenue stats
│
├── database.py # 💾 Database Helper Functions
│ - init_database()
│ - save_sale()
│ - SQLite table creation
│
├── dynamic-thompos.ipynb # 🧮 Jupyter Notebook (AI Research)
│ - Thompson Sampling math
│ - Algorithm experiments
│ - Learning curves
│ - Data visualizations
│
├── pricing_data.db # 💾 SQLite Database (LIVE DATA!)
│ - Auto-created
│ - Grows with every price click
│ - Contains all sales history
│ - Revenue tracking
│
├── README.md # 📖 This documentation
│ - Setup instructions
│ - Features overview
│ - Deploy guide
│
└── requirement.txt # 📦 Python Dependencies (7 packages)
- flask==3.0.3
- flask-cors==5.0.0
- numpy==1.26.4
- scipy==1.13.1
- tabulate==0.9.0
- plotly==5.17.0
- gunicorn==21.2.0

text

---
## 📊 Live Results
Trial 1: Shirt ₹35 → 28 demand → ₹980
Trial 2: Jeans ₹55 → 18 demand → ₹990
Trial 3: Shoes ₹85 → 12 demand → ₹1,020

Dashboard:
💰 Total Revenue: ₹2,990
📈 Daily: ₹2,990
🔢 Sales: 3

text

---

## 🌐 Deploy Production (FREE - 5 min)

**Render.com:**
github.com → New repo → Upload folder

render.com → New Web Service

Build: pip install -r requirements.txt

Start: gunicorn app:app
→ https://yourpricing.onrender.com

text

---

## 🧮 AI Deep Dive

### **Thompson Sampling Algorithm**
Each price = "Arm" with Beta prior

Sample from posterior → Select arm

Observe reward → Update belief

Repeat → Converge to optimal!

text

### **Linear Programming Constraint**
Max: Σ(Price_i × Demand_i × Probability_i)
s.t. Σ(Demand_i × Probability_i) ≤ Inventory


**AI Pricing → Real Revenue →  Success!** 
