# Voice Dictation Tools
_Last updated: 2025-10-30_

## What It Does
Voice-to-text dictation software that converts speech to text in real-time, useful for documentation, coding comments, and quick note-taking during development workflow.

## Current Setup
**Using**: Wispr
**Status**: Evaluating alternatives (paid vs. free options)

## Options Being Evaluated

### Option 1: Wispr (Current - Paid)
**Website**: [https://wispr.ai](https://wispr.ai)
**Type**: Paid service
**Platform**: macOS

**Pros**:
- Polished user experience
- Works well out of the box
- Regular updates and support

**Cons**:
- Paid subscription ($X/month)
- Closed source
- Data sent to their servers

**Current Experience**:
- [Add notes about your experience]

---

### Option 2: Open-Source with Own API Keys (Evaluating)

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

| Tool | Cost | Platform | Accuracy | Setup | Best For |
|------|------|----------|----------|-------|----------|
| **Wispr** | $X/month | macOS | High | Easy | Ready-to-use, polished |
| **WhisperWriter** | ~$1.50/mo | Cross-platform | High | Medium | Cost-conscious, tech-savvy |
| **OpenWhispr** | ~$1.50/mo | Cross-platform | High | Medium | Want nice GUI + own keys |
| **Apple Dictation** | FREE | macOS | Medium | None | Quick notes, privacy |
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
**If using 5 hours/week**:
- Wispr: $X/month (fixed)
- WhisperWriter (OpenAI API): ~$7.50/month (5h × 4 weeks × $0.006/min × 60min)
- Apple Dictation: $0 (free)

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
- [ ] Try Apple Dictation for 1 week (free baseline)
- [ ] Set up WhisperWriter with OpenAI API
- [ ] Test accuracy and workflow
- [ ] Compare costs after 1 month
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
