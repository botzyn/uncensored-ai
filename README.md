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

Create `.env` file:

```env
# Free MiniMax API (sign up at minimax.chat)
MINIMAX_API=your_api_key_here

# Free HuggingFace API (huggingface.co)
HUGGINGFACE_API=your_hf_key_here

# Stripe (for payments - optional)
STRIPE_SECRET_KEY=sk_live_xxx
STRIPE_WEBHOOK_SECRET=whsec_xxx
```

## API Keys (Free)

| Service | Get Key | Cost |
|---------|---------|------|
| MiniMax | minimax.chat | Free tier available |
| HuggingFace | huggingface.co | Free tier available |
| Stripe | stripe.com | 2.9% + 30¢ per transaction |

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
├── .env           # API keys (create this)
└── README.md      # This file
```

## Deployment

### Vercel (Free)
```bash
vercel --prod
```

### Railway
```bash
railway deploy
```

### Render
Connect GitHub repo, set environment variables

## Features

✅ 2 Free Questions
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
