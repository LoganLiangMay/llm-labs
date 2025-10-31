# Voice Dictation Evaluation - Open Source Options
_Last updated: 2025-10-30_

## Context
Evaluating alternatives to Wispr (paid service) for voice dictation. Looking for open-source options that allow using your own API keys for cost control and privacy.

## 🏆 Top Open-Source Options

### 1. WhisperWriter ⭐ Most Popular

**GitHub**: https://github.com/savbell/whisper-writer
**Stars**: 3k+
**Type**: Python app

**Description**:
> Small speech-to-text app that uses OpenAI's Whisper model to auto-transcribe recordings from your microphone to the active window. Can use either local models OR OpenAI API.

**Key Features**:
- Press keyboard shortcut (ctrl+shift+space) to start recording
- Works with both local Whisper models OR OpenAI API
- Four recording modes: continuous, voice activity detection, press-to-toggle, hold-to-record
- Cross-platform (Windows, Mac, Linux)
- Customizable language, temperature, and prompts

**Setup**:
```bash
pip install whisper-writer
# Add your OpenAI API key to config file
```

**Cost with OpenAI API**:
- ~$0.006 per minute of audio
- 1 hour/week = ~$1.50/month
- 20 hours/month = ~$7.20/month

**Pros**:
✅ Very popular and maintained
✅ Simple to set up
✅ Works great with OpenAI API (pay-per-use)
✅ Can also run locally (free)
✅ Cross-platform

**Cons**:
❌ Python dependency
❌ Command-line first (no fancy GUI)

**Verdict**: **Best option for cost-conscious users who want quality**

---

### 2. OpenWhispr 🆕 Modern & Feature-Rich

**GitHub**: https://github.com/HeroTools/open-whispr
**Type**: Electron app (GUI)

**Description**:
> Voice-to-text dictation app with local Whisper models and multiple API options. Privacy-first, cross-platform, global hotkey activated.

**Key Features**:
- Supports OpenAI API, Anthropic API, and Gemini API
- Built with Electron (nice GUI)
- Globe/Fn key toggle on Mac
- Can use local models OR cloud APIs
- Cross-platform

**Setup**:
```bash
cp env.example .env
# Edit .env and add your API keys:
# OPENAI_API_KEY=your_openai_key
# ANTHROPIC_API_KEY=your_anthropic_key
npm run pack
```

**Pros**:
✅ Modern GUI
✅ Multiple AI provider options
✅ Easy to use
✅ Active development

**Cons**:
❌ Requires Node.js setup
❌ Electron app (heavier)
❌ Newer project (less battle-tested)

**Verdict**: **Best option if you want a nice GUI and multiple AI providers**

---

### 3. Whisper Dictation - Full-Featured Linux Solution

**GitHub**: https://github.com/themanyone/whisper_dictation

**Description**:
> Private voice keyboard with local Whisper processing. Supports AI chat, images, webcam, recordings, and voice control.

**Key Features**:
- Uses whisper.cpp (runs locally)
- Voice commands support
- Integrated with ChatGPT API if you want
- Works with stable-diffusion for images
- Linux-focused but very powerful

**Pros**:
✅ Runs completely locally (free)
✅ Very feature-rich
✅ No API costs

**Cons**:
❌ Linux-focused (harder on Mac)
❌ More complex setup
❌ Steeper learning curve

**Verdict**: **Best for Linux power users who want everything local**

---

### 4. WhisperLive - Real-Time Streaming

**GitHub**: https://github.com/collabora/WhisperLive

**Description**:
> Real-time transcription application that uses OpenAI Whisper model to convert speech input into text output. Works with live audio and pre-recorded files.

**Key Features**:
- Supports 3 backends: faster_whisper, tensorrt, and openvino
- Server-client architecture
- Chrome/Firefox extensions available
- iOS client available

**Pros**:
✅ Real-time streaming
✅ Multiple backend options
✅ Browser extensions

**Cons**:
❌ More complex (server-client)
❌ Overkill for simple dictation

**Verdict**: **Best for real-time streaming use cases or mobile integration**

---

## 💰 Free Built-In Options

### Apple Dictation (macOS)

**Type**: Built into macOS
**Cost**: FREE

**How to Enable**:
1. System Settings → Keyboard → Dictation
2. Turn on Dictation
3. Choose shortcut (default: press Fn key twice)
4. Enable "Enhanced Dictation" for offline use

**Features**:
- Works offline (Enhanced Dictation)
- Supports many languages
- No API keys needed
- Native macOS integration

**Pros**:
✅ Completely free
✅ Built-in, no installation
✅ Works offline
✅ Private (on-device processing)
✅ Zero setup

**Cons**:
❌ Less accurate than Whisper-based options
❌ Limited to macOS apps that support dictation
❌ No customization
❌ Requires pause before dictation starts
❌ Character limits on dictation length

**Verdict**: **Best for occasional use, privacy-sensitive, or "just try it" option**

---

### Windows Speech Recognition (Windows)

**Type**: Built into Windows 10/11
**Cost**: FREE

**How to Enable**:
- Settings → Time & Language → Speech
- Turn on "Online speech recognition"

**Pros**:
✅ Free
✅ Built-in

**Cons**:
❌ Less accurate
❌ Limited functionality
❌ Windows only

---

## 🎯 Additional Free Apps

### Voice In (Browser Extension)

**Website**: https://voicein.io
**Type**: Chrome/Edge extension
**Cost**: Free tier (5 min/day) + paid ($48/year)

**Features**:
- Works in all browser text fields
- 100+ languages
- Custom voice commands
- Works on all websites

**Pros**:
✅ Simple browser extension
✅ Works everywhere in browser
✅ Free tier for light use

**Cons**:
❌ Limited to browser
❌ Free tier very limited (5 min/day)
❌ Not suitable for coding workflows

---

### Talon Voice (Advanced)

**Website**: https://talonvoice.com
**Type**: Free (beta), highly customizable
**Cost**: FREE during beta

**Features**:
- Code by voice
- Custom voice commands
- Eye tracking support
- Extremely powerful for developers
- Active community

**Pros**:
✅ Free during beta
✅ Built specifically for coders
✅ Highly customizable
✅ Very active community

**Cons**:
❌ Steep learning curve
❌ Requires significant training and setup
❌ Overkill for simple dictation

**Verdict**: **Best for developers who want to code entirely by voice (accessibility or power users)**

---

## 💡 OpenRouter Note

**Important**: OpenRouter doesn't have native speech-to-text support (it's primarily for text generation models).

**Workaround**:
1. Use any of the above tools for speech → text
2. Send that text to OpenRouter for AI processing

**Example Workflow**:
```
Your Voice → WhisperWriter (free local) → Text
Text → OpenRouter (Claude/GPT) → AI Response
```

This gives you:
- Free dictation (local Whisper)
- Cheap AI processing (OpenRouter)
- Full control of costs

---

## 📊 Cost Comparison

### Scenario: 20 hours of dictation per month

| Option | Monthly Cost | Notes |
|--------|-------------|-------|
| **Wispr** | $X/month | Fixed cost |
| **WhisperWriter + OpenAI API** | ~$7.20 | Pay per use |
| **WhisperWriter + Local Whisper** | $0 | Free, runs on your machine |
| **OpenWhispr + OpenAI API** | ~$7.20 | Same API cost, nicer GUI |
| **Apple Dictation** | $0 | Free, less accurate |
| **Voice In (Free)** | $0 | Only 5 min/day |
| **Voice In (Paid)** | $4/month | Unlimited browser use |
| **Talon Voice** | $0 | Free beta |

---

## 🎯 Recommendation Based on Use Case

### If you want the cheapest option:
**→ Apple Dictation (free) or WhisperWriter with local models (free)**

### If you want best accuracy for $1-2/month:
**→ WhisperWriter + OpenAI API**

### If you want a nice GUI:
**→ OpenWhispr + OpenAI API**

### If you code a lot and want voice commands:
**→ Talon Voice (free beta)**

### If you mainly use browser:
**→ Voice In extension**

### For your 2015 MacBook Pro:
**→ Start with Apple Dictation (free, test if it meets your needs)**
**→ If you need better accuracy: WhisperWriter + OpenAI API (~$1.50/month)**

---

## 🧪 Testing Plan

### Week 1: Free Options
- [ ] Test Apple Dictation for daily workflow
- [ ] Note accuracy issues
- [ ] Track how often I use it

### Week 2: WhisperWriter
- [ ] Install WhisperWriter
- [ ] Set up with OpenAI API
- [ ] Compare accuracy to Apple Dictation
- [ ] Track actual API costs

### Week 3: Decision
- [ ] Calculate actual costs from Week 2
- [ ] Compare to Wispr subscription
- [ ] Make final decision

---

## 📝 Evaluation Notes

### Current Wispr Experience:
- Cost: $X/month
- Works well: [fill in]
- Frustrations: [fill in]
- Worth the cost? [TBD]

### Apple Dictation Test (Week 1):
- Accuracy: [fill in after testing]
- Speed: [fill in]
- Workflow integration: [fill in]
- Good enough? [fill in]

### WhisperWriter Test (Week 2):
- Setup difficulty: [fill in]
- Accuracy vs Apple: [fill in]
- Actual API cost: [fill in]
- Would I pay this monthly? [fill in]

---

## 🔗 Links

- WhisperWriter: https://github.com/savbell/whisper-writer
- OpenWhispr: https://github.com/HeroTools/open-whispr
- Whisper Dictation: https://github.com/themanyone/whisper_dictation
- WhisperLive: https://github.com/collabora/WhisperLive
- Talon Voice: https://talonvoice.com
- Voice In: https://voicein.io

---

## Related
- [[tools/voice-dictation]] - Tool reference and comparison
- [[workflows/current]] - Current workflow setup

---

**Tags**: #resources #voice-dictation #evaluation #open-source #cost-comparison
**Status**: Evaluating
**Date Started**: 2025-10-30
