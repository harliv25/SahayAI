<div align="center">

# SahayAI India

**Every 112 call answered. The most critical, first.**

An AI copilot for India's emergency response. It listens to callers in Hindi, Marathi and English, ranks every incident by urgency, and puts a clear brief on a human dispatcher's screen while the caller is still talking.

<img width="1366" height="768" alt="Capture" src="https://github.com/user-attachments/assets/f6b9cc22-d8c9-48fc-9ad7-9759908dee33" />

<img width="1366" height="768" alt="Capture 2" src="https://github.com/user-attachments/assets/800e67a9-cae5-4334-b662-90b374be0069" />

<img width="1366" height="768" alt="Capture 3" src="https://github.com/user-attachments/assets/1b3cdcbc-fe0b-4ac6-9f59-2f87ab26bef9" />

<img width="431" height="709" alt="Capture 4" src="https://github.com/user-attachments/assets/822d0a68-e910-4635-a49d-8f7196f8dd58" />

<img width="1366" height="768" alt="Capture 5" src="https://github.com/user-attachments/assets/1098bfff-b393-4ca4-931f-fdbb4d9f0e4c" />

<img width="1366" height="768" alt="Capture 6" src="https://github.com/user-attachments/assets/d228e422-79cd-46a3-8399-3e6ee36444e0" />

</div>

# SahayAI 🚨

**An AI-assisted emergency operator console for India's 112 system.**

SahayAI auto-answers incoming emergency calls in the caller's own language, triages them in seconds, filters out prank and low-priority calls, guides the caller with safety steps, and dispatches the nearest ambulance, fire brigade or police unit, either automatically for critical cases or with one click from a human dispatcher.

> *"Sahay" (सहाय) means "help" in Hindi and Marathi.*

---

## The Problem

India's emergency helplines handle huge call volumes across many languages. Operators lose critical seconds because:

- Callers panic and speak in Hindi, Marathi, Tamil, Hinglish or other languages, and an operator may not speak the caller's language.
- A large share of calls are pranks, test calls or non-emergencies, and they sit in the same queue as real emergencies.
- Locating the caller and choosing the right nearby unit is done manually.
- Callers get no guidance while they wait for help to arrive.

## The Solution

SahayAI sits between the caller and the dispatcher:

1. **Auto-answers** the call and detects the language.
2. **Locks location** from the mobile tower feed (cell-site triangulation).
3. **Triages** the call: category, severity (1 to 5), AI confidence, fake-call risk and caller distress level.
4. **Talks the caller through it** with a calming line in their language, the next question to ask, and first-aid or safety precautions.
5. **Prioritises the queue** with critical calls on top and fake or low-priority calls pushed to the bottom.
6. **Dispatches** the right unit, automatically for critical cases (with a cancel window) or via an Accept & dispatch button.
7. **Logs everything** (transcript, decision, who handled it) in a searchable data-management view.

---

## Features

| Area | What it does |
|---|---|
| 📡 **Tower feed** | Shows BTS ID, operator, masked caller number and location accuracy (± metres) for each call |
| 🌐 **Multilingual** | Hindi, Marathi, Tamil, Hinglish and English calls, with live English translation under each line |
| 🧠 **AI triage** | Category, severity (S1 to S5), confidence %, fake-call risk % and a one-paragraph incident brief |
| 😰 **Distress meter** | Calm / Anxious / Panic indicator that updates as the call progresses |
| 🤖 **Caller assistant** | A "say now" calming line, an "ask next" question and numbered precautions for the caller |
| 🔊 **Voice** | Spoken replies using browser text-to-speech, with voice input for test reports |
| 🚑 **Smart dispatch** | Recommends the nearest hospital, police station and fire station, and animates the unit moving on the map with a live ETA |
| ⚡ **Autonomous mode** | Calls with severity 4 or above and fake risk under 20% are auto-dispatched after an 8 second countdown, which the operator can cancel or override |
| 🗑 **Prank filtering** | Suspected pranks and civic complaints are auto-closed or routed to the right helpline without any dispatch |
| 🗺 **Live map** | Vector map of the Mumbai Metropolitan Region with pulsing incident markers, facility icons and zoom-to-incident |
| 📊 **Data management** | Every call in a searchable table, with summary cards for total calls, average triage time, auto-dispatched, filtered and resolved |
| 🌗 **Theme** | Light and dark mode (follows system setting, toggle available) |
| 📱 **Responsive** | Works on desktop and collapses to a single column on mobile |

### Emergency categories

| Category | Units suggested | Example precautions given |
|---|---|---|
| 🚗 Road accident | 108 Ambulance, 100 Police | Keep victim still, press cloth on bleeding |
| 🔥 Fire | 101 Fire Brigade, 108 Ambulance | Exit via stairs, stay low under smoke |
| 🫀 Medical | 108 Advanced Life Support | Lay patient flat, CPR guidance if not breathing |
| 🛡 Crime / personal safety | 100 Police, 181 Women helpline | Move to a crowded lit place, share live location |
| 🌊 Flood / collapse | 112 NDRF, SDRF, 108 | Move to higher ground, switch off power |
| 📋 Non-emergency | No dispatch, log and advise | Redirect to civic helpline, flag repeat callers |

---

## Quick Start

SahayAI is a **single self-contained HTML file** with no build step, no dependencies and no backend.

```bash
To test the demo : https://harliv25.github.io/SahayAI/
```

> **Browser note:** Use **Google Chrome** for voice input (Web Speech API). Text-to-speech works in most modern browsers. Hindi, Marathi and Tamil speech output depends on the voices installed on your device; if none is available, SahayAI falls back to speaking the English translation.

---

## How to Demo

1. **Pick a simulated call** from the left panel, for example *Highway crash · Hindi* or *Chawl fire · Marathi*.
2. Watch the call get auto-answered, the transcript stream in with translations, and the severity, confidence and fake-risk fields fill in.
3. For critical calls, see the **auto-dispatch countdown**. Let it fire, press **Dispatch now**, or **Cancel auto**.
4. Follow the dispatched unit moving across the map with its ETA, and watch the status stepper advance from *Received* to *Resolved*.
5. Try the **Prank call · Hindi** scenario and see it filtered to the bottom of the queue and auto-closed with no dispatch.
6. Use the **Test a report** box (type or 🎙 speak) to submit your own message, such as:
   - `Dadar mein aag lag gayi, bachche andar fase hain`
   - `Andheri mein accident ho gaya, ek aadmi behosh hai, khoon beh raha hai`
7. Switch to the **Data management** tab to search and review every call.

### Built-in scenarios

| Scenario | Language | Location | Severity | Outcome |
|---|---|---|---|---|
| Highway crash | Hindi | Thane | 5 | Auto-dispatch ambulance |
| Chawl fire | Marathi | Dadar | 5 | Auto-dispatch fire brigade |
| Chest pain | Hinglish | Andheri | 4 | Auto-dispatch ambulance |
| Waterlogging | Tamil | Navi Mumbai | 3 | Operator decision |
| Prank call | Hindi | Mulund | 1 | Auto-closed as suspected prank |
| Streetlight issue | English | Borivali | 2 | Routed to municipal helpline |

---

## How It Works

```
 Mobile call ──► Tower feed (BTS, location ± m)
      │
      ▼
 Auto-answer ──► Language detection ──► Transcript + translation
      │
      ▼
 Triage engine ──► category · severity · confidence · fake-risk · distress
      │
      ├── low / fake ──► auto-close or route to civic helpline
      │
      └── real ──► Caller assistant (calming line, next question, precautions)
                     │
                     ▼
            Ranked queue ──► Auto-dispatch (S4+, low fake-risk) or operator click
                     │
                     ▼
            Nearest hospital / police / fire unit ──► Map animation + ETA ──► Resolved
```

### Triage logic (prototype)

- **Category** is matched from keyword patterns in English, Hinglish and Devanagari (for example `aag`, `accident`, `seene`, `flood`, `आग`, `बाढ़`).
- **Severity** starts from a base score per category and is boosted by cues such as bleeding, unconsciousness, being trapped, or children involved (capped at 5).
- **Fake-call risk** is high for very short messages or words like *prank*, *joke*, *pizza*.
- **Distress** is estimated from exclamation marks and urgent words like *jaldi*, *bachao*, *help*, *मदद*.

### Ranking

The queue is sorted so that critical, un-dispatched calls come first, while resolved calls and suspected fakes sink to the bottom. Filters: **All · Critical · Active · Low / fake · Resolved**.

---

## Tech Stack

- **HTML5, CSS3 and vanilla JavaScript**, with zero dependencies
- **Inline SVG** for the map, markers, animations and unit movement
- **Web Speech API** (`speechSynthesis` and `SpeechRecognition`) for voice
- **CSS variables** for theming, with `prefers-color-scheme` support and safe-area insets for mobile

---

## ⚠️ Prototype Disclaimer

This is a **hackathon demo**. To keep it runnable anywhere offline:

- Calls, tower data, caller numbers and facility names are **simulated**.
- The triage engine is a **rule-based heuristic**, not a trained model, and it must not be used for real emergencies.
- The map is a stylised vector map of Mumbai, not real geodata.
- No data leaves the browser, and nothing is stored after a refresh.

## Roadmap to Production

| Prototype | Production |
|---|---|
| Simulated tower feed | Integration with telecom / ERSS-112 location services (cell-site and AML handset location) |
| Keyword triage | LLM + speech-to-text pipeline with multilingual models for Indian languages |
| Vector map | Google Maps / MapMyIndia tiles, Street View and live-traffic ETA |
| Browser TTS | Telephony layer (SIP / WebRTC / Twilio-style voice) for real two-way AI voice |
| In-memory logs | Secure database, audit trail, role-based access and privacy controls |
| Static facility list | Live availability of ambulances, fire engines and beds |
| Fake-call heuristics | Repeat-number detection and call-pattern analysis |
| Human oversight | Mandatory human-in-the-loop policy, with the auto-dispatch threshold set by authorities |

## Project Structure

```
.
├── index.html   # the entire app: markup, styles and logic
└── README.md
```

## Contributing

Ideas and pull requests are welcome, especially for:

- Additional Indian languages (Bengali, Telugu, Kannada, Gujarati, Punjabi)
- More incident categories and city maps
- Accessibility improvements (screen readers, high contrast)

## License

Add the license of your choice (for example MIT) before publishing.

---

*Built for a hackathon to show how AI can help emergency responders save critical minutes.*
