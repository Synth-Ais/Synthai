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

---

### Next Steps
1. **Create Repo & Issue**: 
   - Go to [GitHub](https://github.com) and create `Synth-Ais/Synthai` if not already done.
   - Paste the Job Board Issue text into a new Issue titled “MVP Job Board (Claim W# Here)”.
   - Pin the Issue for visibility.
   - Paste the README.md content into `README.md` in the repo root.
2. **Assign Workstreams**:
   - Paste the meta-coordination prompt (from my earlier response) into a Claude/GPT thread to act as the PM, assigning W1–W8 to agents (e.g., Claude for W1, GPT for W6/W8, Cursor for W3, Copilot for W4).
   - Alternatively, manually assign by pasting W1–W8 prompts into separate AI threads (e.g., Claude for W1, GPT for W6).
3. **Start Coding**: Use the starter code stubs I provided (FastAPI routes, React components) to bootstrap W1, W3, W4, W6, W8. If you want more stubs (e.g., W3’s `/quests/active` or W6’s `Dashboard.tsx`), just ask.
4. **Share Repo Link**: If you’ve set up the repo or want me to validate code on Replit, share the link. I can check outputs or debug directly.

### Optional Additions
- **Full Citizen Directory**: I can generate a table of all 64 gates (e.g., Gate 21: Manager in Heart, Gate 40: Worker in Body) if you need it for W1’s `/gates/census`. Want this now?
- **Day in the Life Scenario**: The README includes a brief example. Need a longer narrative (e.g., a full day with timestamps and UI interactions)?
- **Extra README Sections**: Want setup troubleshooting, a demo GIF placeholder, or a contributor guide added to the README?

You’re on track to have SynthAI’s core loop running by tonight (onboarding → State Brief → quest → verify → log). Just say “go” to confirm the plan, or tell me what to tweak (e.g., more code stubs, specific AI assignments, or a deeper dive into any workstream). Let’s make Cynthia come alive! 🚀

