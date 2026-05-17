# 🇮🇳 India Economic Indicators Dashboard

**Live GDP, CPI, WPI, IIP, Repo Rate — narrated by AI in every Indian state and UT language.**

Built by [Sunil Kumar Iyer](https://github.com/linuxsunil)

---

## What it does

Every month, India releases key economic numbers. Most Indians never understand them.

This tool:
1. Fetches **live data** — GDP, CPI, WPI, IIP, Repo Rate, Unemployment
2. Sends it to **Claude / GPT-4 / Gemini** to write a plain-language explanation
3. **Speaks it aloud** in your state's language — like a personalised AIR bulletin

> *"இந்த மாதம் பணவீக்கம் 4.9% ஆக உள்ளது. இது உங்கள் மளிகை பொருட்கள் கடந்த ஆண்டை விட சற்று அதிகமாக உள்ளன என்று அர்த்தம்..."*

---

## 🗣️ Coverage — All 28 States + 8 Union Territories

| Region | Language | TTS |
|--------|----------|-----|
| Tamil Nadu, Puducherry | Tamil | ✅ Native |
| Kerala, Lakshadweep | Malayalam | ✅ Native |
| Karnataka | Kannada | ✅ Native |
| Andhra Pradesh, Telangana | Telugu | ✅ Native |
| Maharashtra, Goa | Marathi | ✅ Native |
| Gujarat, D&NH | Gujarati | ✅ Native |
| West Bengal, Tripura | Bengali | ✅ Native |
| Punjab | Punjabi | ✅ Native |
| Odisha | Odia | ✅ Native |
| Sikkim | Nepali | ✅ Native |
| J&K | Urdu | ✅ Native |
| UP, Bihar, MP, Delhi + 12 more | Hindi | ✅ Native |
| Assam, Manipur, Goa, NE states | Native script + nearest TTS | ⚠️ Fallback |

---

## 🚀 Quick Start

```bash
git clone https://github.com/linuxsunil/india-economic-dashboard
cd india-economic-dashboard
pip install -r requirements.txt

# Set your AI key (Gemini is FREE)
$env:GEMINI_API_KEY="AIza...your_key"   # Windows
export GEMINI_API_KEY="AIza...your_key" # Mac/Linux

# Run for Tamil Nadu
python src/india_economic_dashboard.py --region tamil_nadu --ai gemini

# Run for Kerala
python src/india_economic_dashboard.py --region kerala --ai claude

# List ALL regions
python src/india_economic_dashboard.py --list

# Generate audio for EVERY state and UT (saves MP3 files)
python src/india_economic_dashboard.py --region all --ai gemini --save-only
```

---

## 📊 Sample Output

```
============================================================
🇮🇳  INDIA ECONOMIC DASHBOARD — 2025-05-17
============================================================
  📈 GDP Growth:       6.4%  (2024-25)
  🛒 CPI Inflation:    4.9%  (Mar 2025)
  🏭 WPI Inflation:    1.2%  (Mar 2025)
  ⚙️  IIP Growth:       5.0%  (Feb 2025)
  🏦 Repo Rate:        6.00%  (Apr 2025)
  👷 Unemployment:     7.8%  (2024)
============================================================

🗣️  Language: Tamil (Tamil Nadu)
🤖 AI: GEMINI

📝 Narration (Tamil):
──────────────────────────────────────────────────────────
இந்த மாதம் இந்தியாவின் பொருளாதார நிலை நல்லபடியாக உள்ளது.
நமது GDP வளர்ச்சி 6.4% ஆக உள்ளது — இது நாம் முன்னேறுகிறோம்
என்பதன் அறிகுறி. பணவீக்கம் 4.9% — கடை பொருட்கள் விலை சற்று
அதிகமாக உள்ளது. RBI வட்டி விகிதம் 6% ஆக குறைந்துள்ளது,
கடன் சற்று மலிவாகும்.
──────────────────────────────────────────────────────────
🔊 Playing audio...
```

---

## 📁 Project Structure

```
india-economic-dashboard/
├── src/
│   └── india_economic_dashboard.py   # Main script
├── languages/
│   └── all_regions.json              # All 36 states/UTs mapped to languages
├── audio_output/                     # Generated MP3 files (gitignored)
├── data/
│   └── indicators_cache.json         # Daily cache (avoids re-fetching)
├── requirements.txt
└── README.md
```

---

## 🌐 Data Sources (all free, no API key needed)

| Indicator | Source |
|-----------|--------|
| GDP Growth | World Bank Open API |
| CPI Inflation | data.gov.in / MOSPI |
| WPI Inflation | data.gov.in / MOSPI |
| IIP Growth | data.gov.in / MOSPI |
| Repo Rate | RBI |
| Unemployment | World Bank / ILO |

---

## 🔑 AI Keys

| AI | Where | Cost |
|----|-------|------|
| Gemini | aistudio.google.com | **FREE** |
| Claude | console.anthropic.com | Free credits |
| GPT-4 | platform.openai.com | Paid |

---

## ⚠️ Disclaimer

Data is fetched from public government sources. This is for educational purposes only. Not financial or investment advice.

---

## 📜 License

MIT — free to use, fork, and build on.

---

*Built by Sunil Kumar Iyer • Powered by Claude AI, Gemini, gTTS, and India's open data*
