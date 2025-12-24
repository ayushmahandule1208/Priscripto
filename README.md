<div align="center">

# 💊 Priscripto

### AI-Powered Healthcare with Real-Time Clinical Intelligence

[![Live Demo](https://img.shields.io/badge/🌐_Live_Demo-priscripto--two.vercel.app-00C853?style=for-the-badge)](https://priscripto-two.vercel.app)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)](https://reactjs.org/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)](https://mongodb.com/)

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Hand%20gestures/Waving%20Hand.png" alt="Wave" width="50" />

**Book appointments. Get AI-powered recommendations. Evidence-based care.**

</div>

---

## 🎯 What Makes This Special?

> Doctors don't just see patients — they get **real-time AI recommendations** powered by the latest PubMed research.

```
Patient Books Appointment → Enters Symptoms → Doctor Gets AI Insights → Better Diagnosis
```

---

## 🧠 The ML Magic (RAG-CDSS)

<table>
<tr>
<td width="50%">

### How It Works

1. **Doctor asks**: *"Best treatment for diabetic hypertension?"*
2. **System scrapes** latest PubMed/PMC articles
3. **BioBERT** converts text → medical embeddings
4. **FAISS** finds most relevant research chunks
5. **Gemini 2.0** generates evidence-based recommendation

</td>
<td width="50%">

### Tech Behind It

| Component | Technology |
|-----------|------------|
| Embeddings | `BioBERT` (medical-tuned) |
| Vector DB | `FAISS` (Facebook AI) |
| LLM | `Google Gemini 2.0 Flash` |
| Scraping | `Selenium` + `BeautifulSoup` |
| Chunking | `LangChain` (300 chars) |

</td>
</tr>
</table>

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Query     │ ──► │   Retrieve  │ ──► │  Generate   │ ──► │   Answer    │
│  "symptoms" │     │  from FAISS │     │ via Gemini  │     │  to Doctor  │
└─────────────┘     └─────────────┘     └─────────────┘     └─────────────┘
```

---

## 🏃 Quick Start

```bash
# Clone & Install
git clone https://github.com/ayushmahandule1208/Priscripto.git
cd Priscripto

# Backend (Port 4000)
cd Backend && npm install && npm start

# Frontend (Port 5173)
cd frontend && npm install && npm run dev

# Admin Panel (Port 5174)
cd admin && npm install && npm run dev

# ML Backend (Port 8000)
cd ml-backend/RAG
pip install fastapi uvicorn langchain sentence-transformers faiss-cpu selenium beautifulsoup4 google-generativeai
uvicorn main:app --port 8000
```

---

## 📁 Project Structure

```
Priscripto/
├── frontend/          # Patient portal (React + Vite)
├── admin/             # Doctor & Admin dashboard
├── Backend/           # REST API (Express + MongoDB)
└── ml-backend/RAG/    # 🧠 AI Engine
    ├── faiss_index.bin      # Vector embeddings
    ├── text_chunks.pkl      # Cached article chunks
    └── symptom_records.json # Processed conditions
```

---

## 🔑 Key Features

| For Patients | For Doctors |
|--------------|-------------|
| 📅 Book appointments | 🤖 AI-powered recommendations |
| 🏥 Browse specialists | 📋 View patient symptoms |
| 💳 Online payments | 📄 Generate prescriptions (PDF) |
| 📱 Medical history | 📊 Dashboard analytics |

---

## 🌐 API Endpoints

```http
POST /api/user/book-appointment    # Book with symptoms
POST /api/doctor/login             # Doctor auth
POST /rag_cdss/                    # 🧠 Get AI recommendation
     Body: { "query": "...", "symptoms": "..." }
```

---

## 🛡️ Environment Variables

```env
# Backend/.env
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_secret
CLOUDINARY_NAME=your_cloudinary

# ML Backend
GOOGLE_API_KEY=your_gemini_key
```

---


