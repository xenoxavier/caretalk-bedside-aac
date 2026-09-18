<div align="center">

# 🗣️ CareTalk — Bedside AAC & Caregiver Speech Assistant

**A bilingual (EN / DE), zero-friction Bedside Augmentative & Alternative Communication (AAC) platform engineered for non-verbal patients, post-operative recovery, palliative care, and caregivers.**

_Instant one-tap speech, real-time synthesized audio chimes, 4-step pain assessment, smart toggle buttons, and persistent shift logging — 100% free, private, and offline-capable._

![status](https://img.shields.io/badge/status-live-brightgreen?style=for-the-badge)
![port](https://img.shields.io/badge/port-8420-blue?style=for-the-badge)
![languages](https://img.shields.io/badge/bilingual-EN%20%7C%20DE-orange?style=for-the-badge)
![audio](https://img.shields.io/badge/audio-Web%20Audio%20API-success?style=for-the-badge)
![api-keys](https://img.shields.io/badge/external%20apis-none%20needed-lightgrey?style=for-the-badge)
![license](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black)](https://www.buymeacoffee.com/richardcuyk)

[Overview](#-overview) ·
[Quick Start](#-quick-start) ·
[Key Capabilities](#-key-capabilities) ·
[Voice & Speaker Studio](#-voice--speaker-studio-100-free) ·
[Smart Opposites & Toggles](#-smart-opposites--toggle-states) ·
[Multi-Step Pain Assessment](#-multi-step-pain-assessment) ·
[Caregiver Shift Log](#-caregiver-shift-log) ·
[Architecture](#-architecture--zero-dependency-stack) ·
[License](#-license)

</div>

* * *

> **Why CareTalk exists:** Traditional AAC hardware is bulky, expensive, and difficult for fatigued or intubated patients to navigate. CareTalk delivers hospital-grade, accessible bedside communication directly through any modern web browser or tablet display — with zero install steps, zero external audio assets, and zero recurring cloud costs.

* * *

## ✨ Overview

CareTalk provides patients with a fast, dignifying voice at their bedside while giving nursing staff and family caregivers an effortless, reliable log of needs and vital requests.

```
+------------------------------------------------------------------------------------+
|  CareTalk Bedside AAC                                                              |
|  +------------------------------------------------------------------------------+  |
|  | [🇬🇧 EN / 🇩🇪 DE]  [🎙️ Voice]  [🌙 Night]  [📋 Log (4)]  [🚨 NOTRUF]  [🩹 PAIN]  |  |
|  +------------------------------------------------------------------------------+  |
|  | FAST BAR:   [ ✓ YES / JA ]   [ ✕ NO / NEIN ]   [ ⏳ WAIT ]   [ 💙 THANKS ]   |  |
|  +------------------------------------------------------------------------------+  |
|  | SOUNDBOARD CATEGORIES & SMART TOGGLES:                                       |  |
|  |  • 💧 Water / Trinken     • 🛏️ Up/Down / Aufsetzen  • 📺 TV (Watch ↔ Done)     |  |
|  |  • 💡 Lights (On ↔ Off)   • 🦼 Wheelchair (In ↔ Out) • 🚪 Go Out (Out ↔ Back)   |  |
|  +------------------------------------------------------------------------------+  |
|  | DYNAMIC COMPOSER: Starters ✨ + Continuations 💬 + Talking Onscreen Keyboard  |  |
|  +------------------------------------------------------------------------------+  |
|  | BEDSIDE DISPLAY: Live Speech Feedback • Web Audio Chimes • Persistent Audio   |  |
+------------------------------------------------------------------------------------+
```

The system features **three distinct layout variants** switchable at the top:
1. **Variant A (Soundboard Grid)**: Big visual touch targets organized into categorical panels (Things, Position & Rest, Comfort, Urgent).
2. **Variant B (Split Screen)**: Equal emphasis on quick action buttons and rapid on-screen sentence creation.
3. **Variant C (Message-First)**: Direct sentence canvas up front, ideal for patients who prefer spelling and multi-word requests.

---

## 🚀 Quick Start

### 1. Prerequisites
No build tools or database required. Any modern browser (Chrome, Safari, Edge, Firefox) is supported.

### 2. Run Locally

#### Option A: Using Python (Recommended)
```bash
python3 -m http.server 8420
```

#### Option B: Using Node / npx
```bash
npx serve -l 8420 .
```

#### Option C: Direct Browser Launch
Simply double-click `index.html` to open it in your web browser.

### 3. Open the Bedside Interface
Navigate to: **[http://localhost:8420](http://localhost:8420)**

---

## 🎯 Key Capabilities

| Feature | Description | Bedside Benefit |
|---|---|---|
| **Full Talking Keyboard** | Language-adaptive layout (**QWERTZ** with `Ä, Ö, Ü, ß` for German, **QWERTY** for English) | Natural, effortless typing with numbers and control keys |
| **Clickable Autocomplete** | Dynamic predictive word suggestions bar above the keyboard with medical and comfort vocabulary | 1-tap word completion saves energy and reduces typing fatigue |
| **Instant Talk Mode** | Speaks immediately upon tapping any button or key | Zero cognitive load for fatigued patients |
| **Fast Response Bar** | Persistent top-level buttons: *YES / JA*, *NO / NEIN*, *WAIT / WARTEN*, *THANKS / DANKE* | Instant answers during doctor/nurse rounds |
| **Smart Toggle Opposites** | Single button toggles state (*Watch TV ↔ Finished TV*, *Lights On ↔ Lights Off*) | Prevents clutter; remembers previous action |
| **Emergency Nurse Call (Notruf)** | High-priority siren with flashing bedside screen and dismissal safety check | Audible room alert for urgent assistance |
| **Bilingual Support (EN/DE)** | Instant switch between English and German vocabulary and speech synthesis | Ideal for international hospitals and care facilities |
| **Caregiver Shift Log** | Timestamped drawer logging every request, pain report, and bell ring | Seamless handover communication between nurse shifts |
| **Night & Dark Mode** | Low-glare dark palette and night theme with bedside digital clock | Prevents sleep disruption during overnight monitoring |

---

## 🎙️ Voice & Speaker Studio (100% Free)

CareTalk integrates directly with native browser and OS speech synthesizers to deliver natural, human-quality pronunciation without robotic cadence.

### In-App Studio Features:
- **Language Voice Selector**: Select independent natural voices for German (Deutsch) and English.
- **Audition Test Buttons (`▶ Test`)**: Instantly preview sentence rhythm and warmth.
- **Cadence & Pitch Calibration**:
  - **Speech Speed**: Calibrated at `0.92x` for gentle, articulate bedside enunciation.
  - **Voice Pitch**: Calibrated at `1.00x` for warm acoustic resonance.
- **Persistent Preferences**: Selections are saved automatically in `localStorage`.

### How to Unlock Ultra-Natural Free Voices on macOS & Browsers:

#### 1. Apple Enhanced & Siri Voices (macOS / iPad — 100% Free)
1. Open **System Settings** $\rightarrow$ **Accessibility** $\rightarrow$ **Spoken Content**.
2. Click the dropdown next to **System Voice** $\rightarrow$ **Manage Voices...**.
3. Under **German (Germany)**, download:
   - **Anna (Enhanced)** *(Warm, compassionate human tone)*
   - **Markus (Enhanced)**
   - **Siri Voice 1 / Voice 2**
4. Refresh CareTalk, open `🎙️ Voice`, and select the enhanced voice!

#### 2. Google Chrome Natural Neural Voices (Free Built-in)
* Open CareTalk in Chrome to automatically use **Google Deutsch** and **Google US English**.

#### 3. Microsoft Edge Natural Voices (Free Built-in)
* Open CareTalk in Edge to automatically use **Microsoft Stefan Natural** or **Microsoft Jenny Natural**.

---

## 🔄 Smart Opposites & Toggle States

CareTalk simplifies the interface by combining opposing actions into a single reactive smart button:

```
[ 📺 Watch TV ]  -- (Tapped) -->  Speaks "I would like to watch TV"
                                   Transforms button to [ 📺 Done with TV ]
[ 📺 Done with TV ] -- (Tapped) --> Speaks "I am finished watching TV"
                                   Transforms button back to [ 📺 Watch TV ]
```

| Action | State A (Initial) | State B (Toggled) |
|---|---|---|
| **Television** | 📺 *Watch TV / Fernsehen* | 📺 *Done with TV / Fertig mit Fernsehen* |
| **Room Lighting** | 💡 *Lights On / Licht an* | 💡 *Lights Off / Licht aus* |
| **Mobility** | 🦼 *Wheelchair / In Rollstuhl* | 🦼 *Back to Bed / Zurück ins Bett* |
| **Fresh Air** | 🚪 *Go Outside / Nach draußen* | 🚪 *Go Back Inside / Wieder rein* |

---

## 🩹 Multi-Step Pain Assessment

Tapping the **`🩹 PAIN`** button opens a guided, accessible 4-step assessment wizard:

```
Step 1: WHERE DOES IT HURT?
  Filter by: [ All Parts ] [ Head & Face ] [ Chest & Back ] [ Arms & Legs ]
  Select part: 🧠 Head, 👁️ Eyes, 🫀 Chest, 🫁 Stomach, 🦴 Back, 🦵 Legs, etc.

Step 2: HOW BAD IS IT? (1 - 10 Scale)
  🟢 1-3: Mild  |  🟡 4-6: Moderate  |  🟠 7-8: Severe  |  🔴 9-10: Extreme

Step 3: WHAT KIND OF PAIN?
  Sharp • Dull / Aching • Burning • Throbbing • Cramping • Stabbing

Step 4: GENERATE & SPEAK
  Auto-synthesizes clear clinical phrase:
  "I have severe throbbing pain in my lower back (Severity 8/10)."
  "Ich habe starke pochende Schmerzen im unteren Rücken (Stärke 8/10)."
```

Every pain report is automatically timestamped and recorded in the Caregiver Shift Log.

---

## 📋 Caregiver Shift Log

Accessible anytime via the **`📋 Log`** button on the app bar:
- **Chronological History**: Shows time of day, request type badge, and bilingual text.
- **Active Badge Counter**: Displays current request tally.
- **1-Click Clipboard Export**: Formats the shift log for pasting into medical notes or handover messages:

```text
=== CAREGIVER SHIFT LOG (CareTalk) ===
Total Events: 3
Timestamp: 18.09.2026, 10:15

[10:12:05] [PAIN] I have moderate aching pain in my chest (Severity 5/10).
[10:14:18] [QUICK] I would like a drink of water, please.
[10:15:02] [FAST] Thank you!
======================================
```

---

## 🏗️ Architecture & Zero-Dependency Stack

CareTalk is intentionally constructed with zero external npm dependencies or heavy build chains to maximize uptime, reliability, and security in healthcare environments.

```
┌─────────────────────────────────────────────────────────────┐
│                       index.html                            │
│  ┌────────────────────────┐    ┌─────────────────────────┐  │
│  │     CSS Design System  │    │  Bilingual Content Data │  │
│  │  • Responsive Grid/Flex│    │  • STRINGS (EN / DE)    │  │
│  │  • Accessible Touch Fitt│    │  • Pain Body Dictionary │  │
│  │  • Light / Dark / Night│    │  • Smart Toggle States  │  │
│  └────────────────────────┘    └─────────────────────────┘  │
│  ┌────────────────────────┐    ┌─────────────────────────┐  │
│  │    Web Audio Engine    │    │  Web Speech Synthesis   │  │
│  │  • Sine/Triangle Synth │    │  • Natural Voice Studio │  │
│  │  • Emergency Siren Sweep│   │  • Rate & Pitch Engine  │  │
│  │  • Non-blocking clicks │    │  • Autoplay Unlocker    │  │
│  └────────────────────────┘    └─────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
```

- **Web Audio API Synth Engine**: Real-time synthesized tones for UI feedback, tactile confirmation, and alarms without loading audio files.
- **Web Speech Synthesis API**: High-fidelity local speech synthesis with custom cadence and pitch controls.
- **Hardware Acceleration**: GPU-accelerated CSS animations and tactile feedback.
- **Local Storage**: Zero-cloud client-side persistence for voice choices and shift logs.

---

## 📁 Repository Structure

```
.
├── index.html                 # Complete standalone CareTalk Bedside AAC application
├── package.json               # Node script helpers (npm start, npm run serve)
├── .gitignore                 # Standard system and cache exclusions
├── LICENSE                    # MIT Open-Source License
├── README.md                  # Detailed platform documentation & user guide
└── .planning/
    └── sketches/
        └── 001-main-screen/   # Design iterations & research prototype files
            ├── index.html
            ├── theme.css
            └── README.md
```

---

## ☕ Support & Donations

If CareTalk helps your loved ones, patients, or care facility, consider supporting ongoing development:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black)](https://www.buymeacoffee.com/richardcuyk)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — free for personal, clinical, and commercial use.
