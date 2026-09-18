# 🎬 16fps

**AI Video Generation Agent — Landing Page & Interactive Demo**

> *"Creativity moves at 16 frames per second."*

16fps is the marketing site and interactive demo for an AI-powered video generation agent. It showcases a product that turns text prompts into short, consistent, ready-to-post videos — and automates the entire pipeline from generation to multi-platform publishing.

Built with **React + TypeScript + Vite + Tailwind CSS**.

---

## ✨ What is 16fps?

16fps positions itself as a **24/7 video generation agent** rather than a one-off video editor. The pitch: describe what you want once, and the agent generates, schedules, and publishes consistent, on-brand videos across social platforms — with no manual editing required.

This repository contains the **marketing website and demo experience**, including:

- A cinematic landing page explaining the product
- An interactive demo page that simulates the generation pipeline with real sample videos
- Market-intelligence stats and a feature comparison against tools like Runway, Synthesia, and Pictory
- Contact/pricing flows that route through pre-filled email requests

---

## 🚀 Features

| Section | What it does |
|---|---|
| **Hero** | Animated grid + lightning-effect background with the core value prop and a primary CTA |
| **Demo Video Section** | Embedded showcase clips demonstrating output quality |
| **What Can It Do** | Six core capabilities: 1-minute videos, style switching, auto-scheduling, multi-platform export, consistency, speed |
| **How It Works** | 4-step pipeline: Upload → AI Generates → Auto-Schedule → Multi-Platform Publish |
| **Features** | 24/7 agent, auto-generate & post, character consistency engine |
| **Market Intelligence** | Industry stats on AI video growth, creator adoption, and ROI |
| **Comparison Table** | Side-by-side feature/pricing comparison vs. Runway, Synthesia, and Pictory |
| **Interactive Demo Page** | Pick or randomize a prompt, watch a simulated multi-step generation process, then preview a matching sample video |
| **Global Audio Control** | Site-wide mute/unmute toggle that persists across all embedded videos |
| **Dynamic SEO** | Per-page `<title>`, meta description, Open Graph, Twitter cards, and JSON-LD structured data via a custom `useSEO` hook |

---

## 🧠 How the Demo Works

The `/demo` page simulates the product experience end-to-end:

1. User clicks **Randomize** (or would type a prompt — inputs are currently disabled pending subscription)
2. A staged loading sequence plays through realistic pipeline steps — *"Analyzing prompt," "Generating character design," "Rendering video frames,"* etc. — with a live progress bar and countdown
3. Once "complete," a matching pre-recorded `.webm` sample plays, paired with the selected prompt

This gives visitors a realistic feel for the product's workflow without requiring a live backend — the interactions are simulated using the sample media in `public/`.

---

## 🛠️ Tech Stack

- **React 18** + **TypeScript**
- **Vite** — build tooling & dev server
- **Tailwind CSS** — styling
- **Lucide React** — icon set
- **Supabase JS client** — installed and ready for future backend/auth integration
- **ESLint** — linting

---

## 📁 Project Structure

```
16fps/
├── public/                    # Static assets & demo video clips (.webm)
├── src/
│   ├── components/
│   │   ├── HomePage.tsx           # Composes all landing page sections
│   │   ├── HeroSection.tsx        # Animated hero + primary CTA
│   │   ├── DemoVideoSection.tsx   # Showcase reel
│   │   ├── WhatCanItDoSection.tsx # Capability grid
│   │   ├── HowItWorksSection.tsx  # 4-step process
│   │   ├── FeaturesSection.tsx    # Core feature highlights
│   │   ├── MarketIntelligenceSection.tsx # Industry stats
│   │   ├── ComparisonSection.tsx  # vs. competitors table
│   │   ├── UseCasesSection.tsx    # Who it's for
│   │   ├── ProcessSection.tsx     # Alternate process breakdown
│   │   ├── ClosingSection.tsx     # Quote + pricing CTA
│   │   ├── DemoPage.tsx           # Interactive simulated demo
│   │   ├── Navigation.tsx         # Responsive nav bar
│   │   ├── GlobalAudioControl.tsx # Site-wide mute toggle
│   │   └── RollingFooter.tsx      # Footer
│   ├── contexts/
│   │   └── AudioContext.tsx       # Global mute state provider
│   ├── hooks/
│   │   └── useSEO.ts              # Dynamic per-page SEO/meta management
│   ├── App.tsx                    # Page routing (home ⇄ demo) + SEO config
│   └── main.tsx
├── package.json
├── tailwind.config.js
├── vite.config.ts
└── tsconfig*.json
```

---

## ⚙️ Getting Started

### Prerequisites
- Node.js (LTS recommended)
- npm

### Installation

```bash
git clone https://github.com/Abhinav-1890/16fps.git
cd 16fps
npm install
```

### Development

```bash
npm run dev
```

Runs the app locally with hot reload via Vite.

### Build

```bash
npm run build
```

Produces an optimized production build.

### Other Scripts

```bash
npm run preview     # Preview the production build locally
npm run lint         # Run ESLint
npm run typecheck    # Run TypeScript type checking with no emit
```

---

## 📬 Contact & Pricing Flow

Instead of a checkout page, CTA buttons ("Use 16fps Agent," "Get Pricing Information," "Contact & Unlock") generate a pre-filled `mailto:` link with context-specific subject lines and bodies, routing interested users directly to an email inquiry.

---

## 🗺️ Roadmap Ideas

- Wire up the Supabase client for real authentication and user accounts
- Replace simulated demo generation with a live API-backed pipeline
- Enable the currently-disabled prompt input and image upload on the demo page
- Add a real checkout/subscription flow

---

## 📄 License

No license file is currently included in this repository. Add one (e.g. MIT) if you intend for others to reuse this code.
