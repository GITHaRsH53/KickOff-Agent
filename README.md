# ⚽ KickOff Agent – AI Football Travel Planner 🏟️  

## ✈️ Overview  
**KickOff Agent** is an AI-powered **football travel planner** built using **n8n**, **Gemini**, and **ElevenLabs Voice AI**.  
It helps football fans plan trips for **UCL and La Liga matches**, automating flight and hotel searches, local activity suggestions, and visa assistance — all delivered as a professional HTML itinerary email. 💌  

---

## 🎥 Demo  
📹 `n8n.Kickoff.Agent.mp4`

---

## 🛠️ Features  
- 🗣️ Natural voice conversations via **ElevenLabs Voice Agent**  
- ✈️ Fetches best **flights**, layovers, and price insights  
- 🏨 Curates **hotel recommendations** with price, rating, and links  
- 🎟️ Suggests **activities & local fan experiences** near stadiums  
- 🪪 Provides **visa and safety advice** for the travel country  
- 📧 Sends **automated HTML itinerary** to user via Gmail  
- 🤖 Combines **multiple AI agents** for seamless automation  

---

## 🏗️ Tech Stack  

| Component | Description |
|------------|-------------|
| **n8n** | Core workflow automation engine |
| **ElevenLabs** | Handles user’s voice input via webhook |
| **Gemini API** | Generates structured summaries & formatted emails |
| **SerpAPI / Tavily** | Real-time flight, hotel, and activity search |
| **Gmail Integration** | Sends personalized itinerary emails |

---

## 🚀 Getting Started  

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/yourusername/KickOff-Agent.git
cd KickOff-Agent

2️⃣ Import Workflow into n8n

Open your n8n instance

Go to Workflows → Import

Upload the file KickOff_Agent_Workflow.json

3️⃣ Configure API Keys 🔑

Set the following credentials in n8n → Credentials:

Gmail → Enables automated email sending

ElevenLabs → For voice agent integration

Gemini API → For text generation and summarization

SerpAPI / Tavily → For fetching flights, hotels, and activities

4️⃣ Run the Workflow 🎯

Start your n8n instance

Trigger using the Webhook URL linked to the ElevenLabs voice agent

Speak or input trip details (e.g., “Plan my Madrid trip for El Clásico 2025”)

Receive your personalized football travel itinerary in your Gmail inbox 🚀

💡 How It Works

🎤 User Interaction — You talk to the ElevenLabs voice companion

🧠 Gemini Model — Extracts travel fields (destination, dates, budget, reason)

🔎 APIs — Retrieve flight, hotel, and local attraction data in real time

🪪 Advice Agent — Adds visa, currency, and safety recommendations

📧 Email Agent — Generates and sends a formatted HTML travel plan

flowchart TD
A[🎤 ElevenLabs Voice Input] --> B[🌐 Webhook Trigger in n8n]
B --> C[🧠 Gemini Model → Extracts & Summarizes]
C --> D[🔎 API Calls → Flights, Hotels, Activities]
D --> E[🪪 Travel Advice Agent]
E --> F[💌 Email Agent → HTML Itinerary]
F --> G[📧 Gmail → Sends to User]
