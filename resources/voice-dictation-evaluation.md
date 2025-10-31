# Voice Dictation Evaluation - Complete Comparison
_Last updated: 2025-10-30_

## Context
Evaluating alternatives to Wispr (paid service) for voice dictation. Comparing paid commercial options, open-source solutions with own API keys, and free built-in options.

## 💰 Paid/Commercial Options (with Free Trials)

### Wispr
**Website**: https://wispr.ai
**Cost**: $8/month or $60/year
**Free Trial**: 7 days
**Platform**: macOS

**What It Is**:
> Clean, polished voice dictation app for Mac. Press a hotkey, speak, and it types in any app. Built on OpenAI's Whisper.

**Key Features**:
- Global hotkey activation
- Works in all macOS apps
- High accuracy (Whisper-based)
- Minimal, unobtrusive UI
- Regular updates

**Verdict**: **Best for users who want "just works" experience and don't mind paying**

---

### Wispr Flow
**Website**: https://wispr.ai/flow
**Cost**: $12/month or $96/year
**Free Trial**: 7 days
**Platform**: macOS

**What It Is**:
> Wispr + AI editing. After dictation, it can improve your text based on context.

**Key Features**:
- All Wispr features
- AI-powered text editing after dictation
- Context-aware corrections ("make this more professional")
- Grammar and formatting fixes
- Command execution

**Verdict**: **Best for users who want AI to polish their dictation automatically**

---

### Aqua Voice
**Website**: https://aquavoice.app
**Cost**: $8/month or $60/year
**Free Trial**: 14 days (longest trial!)
**Platform**: macOS

**What It Is**:
> Alternative to Wispr with longer free trial and on-device processing option.

**Key Features**:
- 14-day free trial (vs. 7 for Wispr)
- Global hotkey (Fn key or custom)
- Works in all macOS apps
- Multiple transcription services
- On-device processing option (privacy)
- Custom commands

**Verdict**: **Best for trying before buying (longest trial) or wanting on-device privacy**

---

### Superwhisper ⭐ Best Value
**Website**: https://superwhisper.com
**Cost**: $30 one-time purchase (lifetime)
**Free Trial**: Limited free version
**Platform**: macOS

**What It Is**:
> Pay once, own forever. No subscription.

**Key Features**:
- ONE-TIME $30 payment (no monthly fees!)
- Works in all apps
- Multiple recording modes
- Customizable hotkeys
- Privacy-focused
- Regular updates included

**Verdict**: **BEST VALUE if you'll use it long-term. $30 one-time = $2.50/month after 1 year, $1.25/month after 2 years**

---

### Otter.ai
**Website**: https://otter.ai
**Cost**: Free (600 min/month), Pro $16.99/month, Business $30/user/month
**Free Trial**: Generous free tier (600 minutes/month = 10 hours!)
**Platform**: Web, iOS, Android, Chrome extension

**What It Is**:
> Meeting transcription and collaboration tool with live transcription.

**Key Features**:
- 600 minutes/month FREE (10 hours!)
- Meeting transcription (Zoom, Google Meet integrations)
- Live transcription
- Speaker identification
- Searchable transcripts
- Team collaboration
- Cross-platform

**Verdict**: **Best if under 10 hours/month (free tier) or need meeting transcription**

---

### Dragon Professional
**Website**: https://www.nuance.com/dragon
**Cost**: $500 one-time OR $15/month subscription
**Free Trial**: 7 days
**Platform**: Windows, macOS

**What It Is**:
> Industry leader with decades of development. Professional-grade dictation with voice commands.

**Key Features**:
- Best-in-class accuracy
- Medical/legal specialized vocabulary
- Voice commands for computer control
- Custom vocabulary training
- Extremely high accuracy
- Professional workflows

**Verdict**: **Best for professionals (medical, legal) who need absolute accuracy and can justify the cost. Overkill for casual use.**

---

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

#### Paid/Commercial Options

| Option | Monthly Cost | Upfront | Long-Term Value | Notes |
|--------|-------------|---------|-----------------|-------|
| **Wispr** | $8/month | - | $96/year | Fixed subscription |
| **Wispr Flow** | $12/month | - | $144/year | AI editing features |
| **Aqua Voice** | $8/month | - | $96/year | 14-day trial, on-device option |
| **Superwhisper** | $2.50* | $30 one-time | $30 total | *Averages to $2.50/month year 1, $1.25/month year 2 |
| **Otter.ai (Free)** | $0 | - | $0 | If under 600 min (10h)/month |
| **Otter.ai (Pro)** | $17/month | - | $204/year | For >10 hours/month |
| **Dragon Pro (subscription)** | $15/month | - | $180/year | Professional features |
| **Dragon Pro (one-time)** | - | $500 | $500 | Own forever |

#### Open-Source & Free Options

| Option | Monthly Cost | Notes |
|--------|-------------|-------|
| **WhisperWriter + OpenAI API** | ~$7.20 | Pay per use (20h × $0.006/min × 60min) |
| **WhisperWriter + Local Whisper** | $0 | Free, runs on your machine |
| **OpenWhispr + OpenAI API** | ~$7.20 | Same API cost, nicer GUI |
| **Apple Dictation** | $0 | Free, less accurate |
| **Voice In (Free)** | $0 | Only 5 min/day |
| **Voice In (Paid)** | $4/month | Unlimited browser use |
| **Talon Voice** | $0 | Free beta |

### 💰 Best Value Analysis

**Cheapest**: Apple Dictation (free) or Otter.ai free tier (10h/month)
**Best Paid Value**: Superwhisper ($30 one-time) - becomes $1.25/month after 2 years
**Best for Heavy Use**: WhisperWriter + Local Whisper (free unlimited)
**Best Commercial UX**: Wispr ($8/month) or Aqua Voice ($8/month with 14-day trial)

---

## 🎯 Recommendation Based on Use Case

### If you want completely FREE:
**→ Apple Dictation** (built-in macOS) or **Otter.ai free tier** (10 hours/month)

### If you want FREE unlimited (technical):
**→ WhisperWriter with local Whisper models** (runs on your machine)

### If you want best value long-term:
**→ Superwhisper** ($30 one-time) - No subscription ever

### If you want polished, "just works" experience:
**→ Wispr** ($8/month) or **Aqua Voice** ($8/month with 14-day trial)

### If you want AI editing after dictation:
**→ Wispr Flow** ($12/month) - AI improves your dictation automatically

### If you want best accuracy for $1-2/month (DIY):
**→ WhisperWriter + OpenAI API** (~$1.50/month for light use)

### If you want a nice GUI with own API keys:
**→ OpenWhispr + OpenAI API** (~$7/month)

### If you need meeting transcription:
**→ Otter.ai** (Free tier: 10h/month, Pro: $17/month)

### If you code a lot and want voice commands:
**→ Talon Voice** (free beta, built for coders)

### If you mainly use browser:
**→ Voice In** extension (free: 5 min/day, paid: $4/month)

### If you're a professional (medical/legal):
**→ Dragon Professional** ($500 one-time or $15/month)

---

## 🧪 Testing Plan

### Week 1: Free Baseline
- [ ] Test Apple Dictation (built-in, free)
- [ ] Try Otter.ai free tier (600 min/month)
- [ ] Note accuracy and workflow fit
- [ ] Track daily usage hours

### Week 2-3: Test Paid Options (Free Trials)
- [ ] **Aqua Voice** (14-day free trial) - Start here, longest trial
- [ ] **Wispr** (7-day free trial) - If Aqua doesn't feel right
- [ ] **Wispr Flow** (7-day free trial) - If you want AI editing
- [ ] Note which feels best for workflow
- [ ] Track which features matter most

### Week 3: Test Open-Source
- [ ] Install WhisperWriter
- [ ] Set up with OpenAI API
- [ ] Track actual API costs
- [ ] Compare accuracy to paid options
- [ ] Test local Whisper (free unlimited)

### Week 4: Final Decision
- [ ] Compare all experiences and actual costs
- [ ] Consider **Superwhisper** ($30 one-time) if long-term value matters
- [ ] Calculate: Is Wispr/Aqua subscription worth it vs. Superwhisper one-time?
- [ ] Make final decision and cancel unused trials

---

## 📝 Evaluation Notes

### Current Wispr Experience:
- Cost: $8/month
- Works well: [fill in]
- Frustrations: [fill in]
- Worth the cost? [TBD]

### Week 1: Free Options

**Apple Dictation**:
- Accuracy: [fill in after testing]
- Speed: [fill in]
- Workflow integration: [fill in]
- Good enough? [fill in]

**Otter.ai Free Tier**:
- Accuracy: [fill in]
- Use case fit: [fill in]
- 10 hours/month enough? [fill in]

### Week 2-3: Paid Free Trials

**Aqua Voice (14-day trial)**:
- Setup ease: [fill in]
- Accuracy: [fill in]
- Features used: [fill in]
- Worth $8/month? [fill in]

**Wispr (7-day trial)**:
- Comparison to Aqua: [fill in]
- Polish level: [fill in]
- Worth $8/month? [fill in]

**Wispr Flow (7-day trial)**:
- AI editing quality: [fill in]
- Worth extra $4/month? [fill in]

### Week 3: Open-Source

**WhisperWriter + OpenAI API**:
- Setup difficulty: [fill in]
- Accuracy vs paid options: [fill in]
- Actual API cost for my usage: $[fill in]
- Would I pay this monthly? [fill in]

**WhisperWriter + Local Whisper**:
- Performance on 2015 MacBook: [fill in]
- Accuracy vs cloud: [fill in]
- Worth the free unlimited? [fill in]

### Week 4: Final Analysis

**Best accuracy**: [winner]
**Best value**: [winner]
**Best UX**: [winner]
**My choice**: [decision]
**Why**: [reasoning]

---

## 🔗 Links

### Paid/Commercial Options
- Wispr: https://wispr.ai
- Wispr Flow: https://wispr.ai/flow
- Aqua Voice: https://aquavoice.app
- Superwhisper: https://superwhisper.com
- Otter.ai: https://otter.ai
- Dragon Professional: https://www.nuance.com/dragon

### Open-Source Options
- WhisperWriter: https://github.com/savbell/whisper-writer
- OpenWhispr: https://github.com/HeroTools/open-whispr
- Whisper Dictation: https://github.com/themanyone/whisper_dictation
- WhisperLive: https://github.com/collabora/WhisperLive

### Free Options
- Talon Voice: https://talonvoice.com
- Voice In: https://voicein.io
- Apple Dictation: Built into macOS (System Settings → Keyboard → Dictation)

---

## Related
- [[tools/voice-dictation]] - Tool reference and comparison
- [[workflows/current]] - Current workflow setup

---

**Tags**: #resources #voice-dictation #evaluation #open-source #paid-options #free-trials #cost-comparison
**Status**: Evaluating
**Date Started**: 2025-10-30
