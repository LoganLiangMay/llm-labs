# Voice Dictation Tools
_Last updated: 2025-10-30_

## What It Does
Voice-to-text dictation software that converts speech to text in real-time, useful for documentation, coding comments, and quick note-taking during development workflow.

## Current Setup
**Using**: Wispr
**Status**: Evaluating alternatives (paid vs. free options)

## Options Being Evaluated

## Paid/Commercial Options (with Free Trials)

### Wispr (Current)
**Website**: [https://wispr.ai](https://wispr.ai)
**Cost**: $8/month or $60/year
**Free Trial**: 7 days
**Platform**: macOS

**Features**:
- Global hotkey activation
- Works in all apps
- High accuracy (OpenAI Whisper-based)
- Clean, minimal UI

**Pros**:
- Polished user experience
- Works well out of the box
- Regular updates and support
- No setup required

**Cons**:
- Paid subscription
- Closed source
- Data sent to their servers

**Current Experience**:
- [Add notes about your experience]

---

### Wispr Flow
**Website**: [https://wispr.ai/flow](https://wispr.ai/flow)
**Cost**: $12/month or $96/year
**Free Trial**: 7 days
**Platform**: macOS

**Features**:
- All Wispr features
- AI-powered text editing after dictation
- Context-aware corrections
- Format and style adjustments
- Command execution (e.g., "make this more professional")

**Pros**:
- Enhanced AI editing capabilities
- Fixes grammar and formatting automatically
- Context-aware improvements
- Premium Wispr experience

**Cons**:
- More expensive than basic Wispr
- Still closed source
- Requires internet connection

---

### Aqua Voice
**Website**: [https://aquavoice.app](https://aquavoice.app)
**Cost**: $8/month or $60/year
**Free Trial**: 14 days (longer than Wispr!)
**Platform**: macOS

**Features**:
- Global hotkey (Fn key or custom)
- Works in all macOS apps
- Multiple transcription services (Whisper, others)
- Custom commands and shortcuts
- On-device processing option

**Pros**:
- 14-day free trial (vs. 7 days for Wispr)
- On-device option for privacy
- Customizable commands
- Similar price to Wispr

**Cons**:
- Less established than Wispr
- UI not as polished

---

### Superwhisper
**Website**: [https://superwhisper.com](https://superwhisper.com)
**Cost**: One-time $30 (lifetime)
**Free Trial**: Limited free version available
**Platform**: macOS

**Features**:
- One-time purchase (no subscription!)
- Works in all apps
- Multiple recording modes
- Customizable hotkeys
- Privacy-focused

**Pros**:
- ONE-TIME PAYMENT (best value long-term)
- No monthly subscription
- Privacy-focused
- Regular updates

**Cons**:
- Higher upfront cost
- Free version is very limited
- Smaller company/support

---

### Otter.ai
**Website**: [https://otter.ai](https://otter.ai)
**Cost**: Free tier, Pro $16.99/month, Business $30/user/month
**Free Trial**: Free tier (600 minutes/month)
**Platform**: Web, iOS, Android, Chrome extension

**Features**:
- Meeting transcription
- Live transcription
- Speaker identification
- Searchable transcripts
- Team collaboration
- Integrations (Zoom, Google Meet, etc.)

**Pros**:
- Generous free tier (600 min/month)
- Great for meetings
- Cross-platform
- Team features

**Cons**:
- More focused on meetings than general dictation
- Web-based (not native app)
- Not ideal for quick dictation

---

### Dragon Professional
**Website**: [https://www.nuance.com/dragon](https://www.nuance.com/dragon)
**Cost**: $500 one-time OR $15/month subscription
**Free Trial**: 7 days
**Platform**: Windows, macOS

**Features**:
- Industry leader (decades of development)
- Medical/legal vocabulary
- Voice commands for computer control
- Custom vocabulary
- Extremely high accuracy

**Pros**:
- Best-in-class accuracy
- Professional features
- Medical/legal specialized versions
- Voice computer control

**Cons**:
- VERY expensive ($500 or $180/year)
- Overkill for casual use
- Steep learning curve
- Resource-intensive

---

## Open-Source with Own API Keys

#### WhisperWriter ⭐ Recommended
**GitHub**: [https://github.com/savbell/whisper-writer](https://github.com/savbell/whisper-writer)
**Type**: Open source, use your own OpenAI API key
**Platform**: Cross-platform (Windows, Mac, Linux)

**How It Works**:
- Press keyboard shortcut (ctrl+shift+space) to start recording
- Uses OpenAI Whisper API OR local Whisper models
- Auto-transcribes to active window

**Cost with OpenAI API**:
- ~$0.006 per minute of audio
- 1 hour/week = ~$1.50/month
- Way cheaper than paid services

**Setup**:
```bash
git clone https://github.com/savbell/whisper-writer
cd whisper-writer
pip install -r requirements.txt
# Add your OpenAI API key to config.yaml
python run.py
```

**Pros**:
- Very cheap (pay only for what you use)
- Open source, full control
- Can run locally (free) or via API
- Simple setup
- Four recording modes

**Cons**:
- Requires Python setup
- Not as polished as commercial apps
- Need to manage API keys

---

#### OpenWhispr
**GitHub**: [https://github.com/HeroTools/open-whispr](https://github.com/HeroTools/open-whispr)
**Type**: Open source, multiple API options
**Platform**: Cross-platform (Electron app)

**Features**:
- Supports OpenAI, Anthropic, Gemini APIs
- Nice GUI (Electron-based)
- Globe/Fn key toggle on Mac
- Local OR cloud processing

**Setup**:
```bash
cp env.example .env
# Edit .env with your API keys
npm run pack
```

**Pros**:
- Modern UI
- Multiple AI provider options
- Cross-platform

**Cons**:
- More complex setup (Node.js)
- Electron app (heavier than native)

---

### Option 3: Apple Built-In Dictation (Free)

**Type**: Built into macOS
**Cost**: FREE

**How to Enable**:
1. System Settings → Keyboard → Dictation
2. Turn on Dictation
3. Choose shortcut (default: press Fn key twice)

**Features**:
- Works offline (Enhanced Dictation)
- Supports many languages
- No API keys needed
- Native macOS integration

**Pros**:
- Completely free
- Built-in, no installation
- Works offline
- Private (on-device processing)

**Cons**:
- Less accurate than Whisper/paid options
- Limited to macOS apps that support dictation
- No customization
- Requires pause before dictation starts

**Good For**:
- Quick notes and emails
- When you don't want to pay anything
- Privacy-sensitive use cases

---

### Other Free Options

#### Talon Voice (Advanced)
**Website**: [https://talonvoice.com](https://talonvoice.com)
**Type**: Free (beta), highly customizable
**Platform**: Cross-platform

**Features**:
- Code by voice
- Custom voice commands
- Eye tracking support
- Extremely powerful for developers

**Pros**:
- Free during beta
- Built for coders
- Highly customizable
- Active community

**Cons**:
- Steep learning curve
- Requires training and setup
- Overkill for simple dictation

---

#### Voice In (Browser Extension)
**Website**: [https://voicein.io](https://voicein.io)
**Type**: Free tier + paid
**Platform**: Chrome/Edge extension

**Features**:
- Works in browser text fields
- Free tier: 5 minutes/day
- Paid: unlimited

**Pros**:
- Simple browser extension
- Works everywhere in browser
- Free tier for light use

**Cons**:
- Limited to browser
- Free tier very limited
- Not for coding workflows

---

## Comparison Table

### Paid/Commercial Options

| Tool | Cost | Free Trial | Platform | Accuracy | Best For |
|------|------|-----------|----------|----------|----------|
| **Wispr** | $8/mo or $60/yr | 7 days | macOS | High | Polished, ready-to-use |
| **Wispr Flow** | $12/mo or $96/yr | 7 days | macOS | High | AI editing, premium features |
| **Aqua Voice** | $8/mo or $60/yr | 14 days | macOS | High | Longer trial, on-device option |
| **Superwhisper** | $30 one-time | Limited free | macOS | High | One-time payment, best value |
| **Otter.ai** | Free/$17/mo | 600 min/mo free | Cross-platform | High | Meetings, transcription |
| **Dragon Pro** | $500 or $15/mo | 7 days | Win/Mac | Highest | Professional, medical/legal |

### Open-Source & Free Options

| Tool | Cost | Platform | Accuracy | Setup | Best For |
|------|------|----------|----------|-------|----------|
| **WhisperWriter** | ~$1.50/mo (API) | Cross-platform | High | Medium | Cost-conscious, own API keys |
| **OpenWhispr** | ~$1.50/mo (API) | Cross-platform | High | Medium | GUI + own API keys |
| **Apple Dictation** | FREE | macOS | Medium | None | Quick notes, privacy, trying it out |
| **Talon Voice** | FREE (beta) | Cross-platform | High | Hard | Code by voice, power users |
| **Voice In** | Free/Paid | Browser | Medium | Easy | Browser-only use |

---

## My Decision Process

### Questions to Answer:
- [ ] How many hours/week will I use dictation?
- [ ] Do I need it for coding or just notes?
- [ ] Am I comfortable managing API keys?
- [ ] Is cost or convenience more important?
- [ ] Do I need offline capability?

### Cost Calculation:
**If using 5 hours/week (20 hours/month)**:
- **Wispr**: $8/month (fixed subscription)
- **Wispr Flow**: $12/month (AI editing features)
- **Aqua Voice**: $8/month (fixed subscription)
- **Superwhisper**: $30 one-time (after 1 year = $2.50/month, 2 years = $1.25/month)
- **Otter.ai**: Free tier (if under 600 min/month = 10 hours/month)
- **WhisperWriter (OpenAI API)**: ~$7.20/month (20h × $0.006/min × 60min)
- **Apple Dictation**: $0 (free)

**Best Value Long-Term**: Superwhisper ($30 one-time, no subscription)

### Privacy Consideration:
- **Most Private**: Apple Dictation (on-device) or local Whisper models
- **Least Private**: Wispr, cloud APIs (data sent to servers)

---

## Current Evaluation Notes

### Wispr Experience:
- [Add your notes about current Wispr usage]
- What works well:
- What's frustrating:
- Worth the cost?

### Testing Plan:

**Week 1: Free Baseline**
- [ ] Try Apple Dictation (free, built-in)
- [ ] Note accuracy and frustrations
- [ ] Track daily usage hours

**Week 2-3: Test Paid Options (Free Trials)**
- [ ] Aqua Voice (14-day free trial) - longest trial
- [ ] Wispr (7-day free trial if needed) - current option
- [ ] Wispr Flow (7-day free trial) - if you want AI editing
- [ ] Note which feels best for workflow

**Week 3: Test Open-Source**
- [ ] Set up WhisperWriter with OpenAI API
- [ ] Track actual API costs
- [ ] Compare accuracy to paid options

**Week 4: Decision**
- [ ] Compare all experiences and costs
- [ ] Consider Superwhisper ($30 one-time) if worth it
- [ ] Make final decision

---

## Integration with Workflow

**Use Cases**:
1. **Documentation**: Dictate README sections, workflow notes
2. **Code Comments**: Explain complex logic verbally
3. **Quick Notes**: Capture ideas during development
4. **Obsidian Notes**: Faster note-taking in this vault
5. **PR Descriptions**: Quickly explain changes

**Keyboard Shortcuts**:
- Wispr: [your shortcut]
- WhisperWriter: Ctrl+Shift+Space (default)
- Apple: Fn twice (default)

---

## Related
- [[resources/voice-dictation-evaluation]] - Detailed comparison and evaluation notes
- [[workflows/current]] - Current workflow setup

---

**Tags**: #tool #voice-dictation #productivity #evaluation
**Status**: Evaluating alternatives
**Decision Deadline**: [Set a date to make final decision]
