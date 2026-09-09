# safva-portfolio

**A portfolio built to prove one thing: I build usable AI products, not just models in a notebook.**

![Status](https://img.shields.io/badge/status-in--progress-35415C)
![Stack](https://img.shields.io/badge/stack-HTML%20%2F%20CSS-15181D)
![License](https://img.shields.io/badge/license-MIT-6B7280)

## Overview

Most portfolio sites either bury real work behind vague "I'm passionate about tech" copy, or list projects with no evidence they actually run. This one is built around a single claim — *I build usable AI products, not just models in a notebook* — and every page is designed to back it with real proof: real screenshots, real numbers, real repos, not stock imagery or filler. It's aimed at one reader (a hiring manager screening for backend AI/ML roles) and one action (get in touch about a role).

The site currently has a live Home page with the full visual identity applied, and a working Contact page wired to a real form backend — ahead of Work and About going in over the following build weeks.

## Features

- Responsive layout, tested at both desktop and mobile widths
- Full identity system applied from day one: type, palette, logo, and a judged (not just generated) background texture
- Working links to LinkedIn, GitHub, a downloadable CV, and a booking link ("let's talk")
- Working Contact form (Web3Forms-backed) with inline success/error feedback and spam honeypot, no page reload required
- Zero build step — pure HTML/CSS, deploys straight from the repo
- Structured to expand cleanly into a full site (Work, About) without a rebuild

## Tech Stack

- **HTML5 / CSS3** — no framework, no bundler
- **Google Fonts** — Space Grotesk (headings), Inter (body)
- **GitHub Pages** — static hosting, deployed from `main`

## Screenshots

![Home page — desktop](screenshots/home-desktop.png)
*Home, desktop viewport*

![Home page — mobile](screenshots/home-mobile.png)
*Home, mobile viewport — verified live on a phone, not just locally*

## Installation

```bash
git clone https://github.com/fsafva13-coder/safva-portfolio.git
cd safva-portfolio
```

No dependencies, no build step — it's static HTML.

## Usage

Open `index.html` directly in a browser, or serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Project Structure

```
safva-portfolio/
├── index.html              # Home — name, claim, positioning, and links
├── contact.html             # Contact — form wired to Web3Forms, matches Home's identity system
├── assets/
│   ├── favicon.svg         # Logo mark, also used as favicon
│   ├── logo.svg             # Mark + wordmark, for the site header
│   ├── home-background.png  # Connective background texture (judged against a rejected candidate — see Learnings)
│   └── safva-cv.pdf         # CV, linked directly from the Home page
├── screenshots/            # Live screenshots used in this README
└── README.md
```

## Results

- Live and reachable at the URL below, confirmed on a second device (phone), not just a local build
- Identity system (2 fonts, 3 colors, 1 logo mark) applied consistently from the first commit, so later pages inherit it instead of reinventing it
- Contact form submits via fetch to Web3Forms and confirms success inline, so there's no dead-end mailto link or page reload between a visitor and a sent message

## Challenges & Learnings

- The background texture wasn't picked by eye — two AI-generated candidates were rendered *behind actual hero copy* at low opacity before choosing, because a texture that looks fine in isolation can still visually compete with text once it's actually behind a headline. The denser candidate failed that test; the sparser one, with an empty center, passed.
- Deliberately kept the identity system small (2 fonts, 3 colors) specifically so future project screenshots — which already carry their own colors — don't have to compete with the site's own styling.

## Future Improvements

- Work page with three real case studies (SOLACE, mirae-luxe, BE-04 Tasks API), each backed by a real screenshot rather than a generated one
- About page with a real photo and short bio
- Possible custom domain once the full site is live

## Demo

**Live:** https://fsafva13-coder.github.io/safva-portfolio/

## License

MIT — code is free to reuse; the case studies and personal content are not.
