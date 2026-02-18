# 🔓 Uncensored AI

A freemium AI chat service with 2 free questions, then paid subscription.

## Quick Start

### Option 1: Static HTML (Demo)
1. Open `index.html` in a browser
2. Demo mode works immediately
3. Configure API for real AI responses

### Option 2: Full Server
```bash
cd uncensored-ai
npm install
npm start
```

Then open `http://localhost:3000`

## Environment Variables

Create `.env` file (never commit this!):

```env
# Groq API (sign up at groq.com) - Fast free LLM
GROQ_API=your_groq_api_key_here

# HuggingFace API (huggingface.co) - Free image gen
HUGGINGFACE_API=your_hf_key_here

# Stripe (for payments - optional)
STRIPE_SECRET_KEY=sk_live_xxx
STRIPE_WEBHOOK_SECRET=whsec_xxx
```

## API Keys (Free)

| Service | Get Key | Cost |
|---------|---------|------|
| Groq | groq.com | Free tier available |
| HuggingFace | huggingface.co | Free tier available |
| Stripe | stripe.com | 2.9% + 30¢ per transaction |

## Security Best Practices

✅ API keys stored in `.env` (gitignored)
✅ Keys NEVER exposed in client-side code
✅ Server-side API calls only
✅ Environment variables on deployment

## Revenue Model

```
FREE TIER: 2 questions
     ↓
$10/month UNLIMITED
     ↓
$15/month + Image Gen (10/day)
```

## File Structure

```
uncensored-ai/
├── index.html      # Frontend (can deploy anywhere)
├── server.js      # Backend API
├── package.json    # Dependencies
├── .env           # API keys (local only, gitignored!)
├── .gitignore     # Protects .env from commit
└── README.md      # This file
```

## Deployment

### Vercel (Free)
```bash
vercel --prod
```
Set environment variables in Vercel dashboard.

### Railway
```bash
railway deploy
```

### Render
Connect GitHub repo, set environment variables

## Features

✅ 2 Free Questions
✅ Groq LLM Integration (fast, free)
✅ Unlimited Questions ($10/mo)
✅ Image Generation ($15/mo)
✅ Clean Dark Theme
✅ Mobile Responsive
✅ Stripe Integration Ready
✅ Local Storage (no login required)

## Customization

Change prices in `index.html`:
```javascript
const PRICE_UNLIMITED = 10;  // $10/month
const PRICE_IMAGE = 15;     // $15/month
```

Change colors:
```css
:root {
    --primary: #f39c12;  // Orange
    --secondary: #e74c3c; // Red
}
```

## License

MIT - Build, modify, profit.
