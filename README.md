💰 FinTrack — AI-Powered Personal Finance Tracker
> Built by **Manish** · Powered by Claude AI (Finny)
---
✨ Features
Feature	Description
Dashboard	Balance, income, expenses, savings rate at a glance
Transactions	Add, edit, delete, filter, sort, and export (CSV/JSON)
Insights	Category breakdowns, monthly comparisons, financial health score
UPI Automation	Link your phone number to auto-import bank SMS alerts
Finny AI	Chat with your personal AI finance advisor powered by Claude
Dark mode	Full light/dark theme support
Responsive	Works on mobile, tablet, and desktop
---
 Deploy to Vercel (Zero Config)
Option 1 — Vercel CLI
```bash
npm i -g vercel
vercel
```
Follow the prompts. Done!
Option 2 — GitHub Import
Push this repo to GitHub
Go to vercel.com/new
Import your repository
Click Deploy — no configuration needed
Option 3 — Drag & Drop
Go to vercel.com/new
Drag the project folder onto the page
Deploy instantly
---
🤖 Setting up Finny (AI Advisor)
Finny uses the Anthropic Claude API. The API key is injected at the proxy layer — no key needed in the frontend code.
If you're self-hosting and want Finny to work:
Get an API key from console.anthropic.com
Set up a simple proxy (e.g., a Vercel Edge Function or Cloudflare Worker) that injects the `x-api-key` header
Update the fetch URL in `index.html` to point to your proxy
> **Note:** The app works fully without Finny — all finance features are standalone.
---
📱 UPI Automation
The UPI Automation feature (⚡ in sidebar) lets users:
Enter their bank-registered mobile number
Verify via OTP
Grant SMS read permission
Auto-import UPI & bank SMS alerts into FinTrack
> **Demo mode:** The current build uses mock SMS data to demonstrate the flow. Production integration requires a backend SMS parsing service.
---
🏗️ Tech Stack
React 18 (via CDN, no build step)
Chart.js 4 — line chart & donut chart
DM Sans + DM Mono + Syne — Google Fonts
Anthropic Claude API — Finny AI advisor
localStorage — client-side data persistence
Web Speech API — voice input for Finny
---
📁 Project Structure
```
fintrack/
├── index.html          # Entire app (single file)
├── vercel.json         # Vercel deployment config
└── README.md           # You are here
```
---
🔧 Local Development
No build tools needed! Just open `index.html` in a browser:
```bash
# Using Python
python3 -m http.server 3000

# Using Node
npx serve .

# Or just open index.html directly in Chrome/Firefox
```
---
🎨 Design
Fonts: Syne (headings) + DM Sans (body) + DM Mono (numbers)
Theme: Warm neutral tones with blue accent — light & dark modes
Splash: 3-second branded loading screen
Finny: Custom SVG robot avatar with gradient design
---
📄 License
MIT — free to use, modify, and deploy.
---
Made with ❤️ by Manish · FinTrack v2.0