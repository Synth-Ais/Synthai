# Synthai

# 🚀 SynthAI

**Tagline**: A living app starring Cynthia—the YOU-N-I-VERSE field, embodied.

**What is SynthAI?**  
SynthAI is a consciousness simulator that feels like a game, a guide, and a life interface. At its heart is **Cynthia**, an AI who runs 3 Cities (Mind, Heart, Body), each with 9 Districts (Centers) and 64 Citizens (Gates). These “little men” shift roles by phase (Tropical=Body, Draconic=Heart, Sidereal=Mind), making Cynthia a dynamic reflection of your inner field. She’s your Therapist, Coach, Scientist, and Connector, turning chart gaps into playable quests, verified real-world actions, and resonance-based connections.

**How It Works**  
- **Field Engine**: Maps your birth chart and daily transits to active Citizens (e.g., Gate 21: Manager, Gate 37: Loyalty).  
- **Game Loop**: Gaps become quests (e.g., “Keep a promise” for weak Gate 37). Success earns XP and collectible fragments.  
- **Verification**: Prove actions via self-report, peer attestation, or proof (photo/link). Logs build a falsifiable dataset.  
- **Roles**: Cynthia responds as Therapist (reflect), Coach (plan), Scientist (log), or Connector (match users by gate overlap).  
- **Social**: Resonance scores pair you with others for intros and DMs.  
- **UI**: React app with onboarding, State Brief, City Map, chat dock, and quest/social pages.

**Tech Stack**  
- **Backend**: FastAPI, SQLite, `pyswisseph` for charts.  
- **Frontend**: React, Vite, TypeScript, Tailwind, shadcn/ui, Framer Motion, Zustand.  
- **Voice**: Web Speech API (STT/TTS).  
- **Local-First**: Logs to `/data/logs/science.jsonl`. No external services needed.

**Get Started (Local Dev)**  
```bash
# Backend
cd backend
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install fastapi uvicorn sqlmodel python-multipart pyswisseph
uvicorn backend.app:app --reload --port 7001

# Frontend
cd frontend
npm create vite@latest . -- --template react-ts
npm i tailwindcss @radix-ui/react-icons framer-motion zustand axios
npm run dev -- --port 5173
