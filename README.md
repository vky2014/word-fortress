# 🏰 Word Fortress

**Medieval Vocabulary Tower Defense** — Build towers, learn words, defend the realm!

An educational tower defense game targeting **6th–10th grade** vocabulary. Answer word definition questions to earn gold, place medieval towers on a grid, and survive 15 waves of enemies. Harder and rarer words earn exponentially more rewards.

## 🎮 Play Now

**[Play Word Fortress →](https://YOUR-USERNAME.github.io/word-fortress/)** *(auto-populated after enabling GitHub Pages)*

## ✨ Features

- **5 grade levels** — 6th Grade through SAT Prep, each calibrated with different word difficulty and starting gold
- **50 vocabulary words** across 5 difficulty tiers with adaptive difficulty
- **Word rarity system** — Common (×1), Uncommon (×2), Rare (×3), Epic (×5), Legendary (×8) score multipliers
- **4 tower types** — Archer 🏹, Catapult 🪨, Frost Mage 🧙, Lightning ⚡ — each upgradeable to level 5
- **15 waves** with boss dragons every 5th wave
- **📖 Study List** — flag words during gameplay to review later with definitions and example sentences
- **🏆 Persistent leaderboard** — arcade-style initials, top 10 scores saved locally
- **Fully responsive** — auto-scaling grid plays on phones, tablets, and desktop
- **Single HTML file** — zero build step, zero dependencies

## 🚀 Deploy

### GitHub Pages (Free — Recommended)

This repo includes a GitHub Actions workflow that auto-deploys on every push to `main`:

1. Fork or clone this repo
2. Go to **Settings → Pages → Source → GitHub Actions**
3. Push to `main` — live within minutes at `https://YOUR-USERNAME.github.io/word-fortress/`

### Custom Domain

1. Deploy via GitHub Pages (above)
2. Go to **Settings → Pages → Custom domain** → enter your domain
3. Add a `CNAME` DNS record pointing to `YOUR-USERNAME.github.io`
4. Enable **Enforce HTTPS**

### Other Hosts

The game is a single `public/index.html` file. Upload it anywhere:

| Host | Command |
|------|---------|
| **Vercel** | `npx vercel public/ --prod` |
| **Netlify** | `npx netlify deploy --prod --dir=public` |
| **DigitalOcean** | App Platform → static site → output dir: `public` |
| **Any server** | `cp public/index.html /var/www/html/` |

## 🏗 Project Structure

```
word-fortress/
├── public/
│   └── index.html              # Entire game (~45KB single file)
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Pages auto-deploy
├── .gitignore
├── LICENSE
└── README.md
```

## 🎯 How It Works

**Game Loop:** Answer 3 vocab questions → earn gold → place/upgrade towers → launch wave → towers auto-attack enemies → survive 15 waves.

**Adaptive Difficulty:** 3 correct in a row → harder words. 2 wrong in a row → easier words. Capped by grade level.

**Tower Targeting:** "First" priority — towers attack the enemy closest to the exit.

### Rarity Rewards

| Rarity | Badge | Gold | Score |
|--------|-------|------|-------|
| Common | ⬜ | ×1.0 | ×1 |
| Uncommon | 🟩 | ×1.3 | ×2 |
| Rare | 🟦 | ×1.7 | ×3 |
| Epic | 🟪 | ×2.2 | ×5 |
| Legendary | 🟨 | ×3.0 | ×8 |

## 🛠 Tech

React 18 + Babel from CDN. No npm, no bundler, no build. localStorage for persistence. CSS animations for effects. Google Fonts (Cinzel + Crimson Text).

## 📄 License

MIT — see [LICENSE](LICENSE).
