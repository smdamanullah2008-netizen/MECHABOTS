# MECHABOTS — Website

A premium, futuristic website for **MECHABOTS**, a student startup project developing a low-cost modular collaborative robot (cobot) for MSMEs.

## Quick Start

### Prerequisites
- **Node.js** (any version — already on your system)

### Run the Website Locally

```bash
cd C:\Users\smdam\.gemini\antigravity\scratch\mechabots
"C:\Users\smdam\AppData\Local\AppLab\resources\node\node.exe" server.js
```

Then open **http://localhost:3000** in your browser.

Press `Ctrl+C` in the terminal to stop the server.

---

## Project Structure

```
mechabots/
├── index.html          ← Main webpage (all sections)
├── server.js           ← Local development server (Node.js)
├── css/
│   └── styles.css      ← Complete stylesheet
├── js/
│   ├── config.js       ← ✏️ Editable brand/contact/product config
│   ├── app.js          ← Main entry point
│   ├── navigation.js   ← Header, mobile menu, smooth scroll
│   ├── animations.js   ← Scroll-triggered fade-in animations
│   ├── faq.js          ← FAQ accordion
│   └── contact-form.js ← Form validation & mailto fallback
├── assets/
│   ├── logo.svg        ← MECHABOTS wordmark
│   ├── favicon.svg     ← Browser tab icon
│   ├── robot-arm.svg   ← Hero robot illustration
│   ├── robot-diagram.svg ← Component diagram
│   ├── gripper-concepts.svg ← End-effector concepts
│   ├── hero-bg-pattern.svg  ← Subtle grid pattern
│   └── workflow.svg    ← Process workflow diagram
└── README.md           ← This file
```

## How to Update Content

### Contact Details, Brand Info, Product Status
Edit **`js/config.js`** — all business details are in one place:
- `CONFIG.contact.email` — email address
- `CONFIG.contact.phone` — phone number
- `CONFIG.contact.linkedin` — LinkedIn URL
- `CONFIG.brand.name` — brand name
- `CONFIG.product.targetCost` — cost target
- `CONFIG.features` — feature list with status labels
- `CONFIG.faq` — FAQ questions and answers

### Feature Status Labels
In `js/config.js`, each feature has a `status` field:
- `"Planned"` — not yet started
- `"Under Development"` — in progress
- `"Demonstrated"` — tested and working

### Making the Contact Form Send Real Emails
The form currently uses a **mailto:** fallback (opens the user's email client).
To enable server-side email delivery:
1. Set up a backend (e.g., Node.js with Nodemailer, or a service like Formspree/EmailJS)
2. Modify `js/contact-form.js` to POST form data to your endpoint
3. No API keys are required for the current mailto approach

## Building for Production / Deployment
This is a static website — no build step needed!

### To deploy:
1. Upload all files to any web hosting (Netlify, Vercel, GitHub Pages, shared hosting)
2. The `server.js` file is only for local development — you don't need it in production
3. Make sure your web server serves `index.html` as the default document

### Netlify (free, recommended):
1. Push files to a GitHub repository
2. Connect the repo to Netlify
3. Set publish directory to the root folder
4. Done — auto-deploys on every push

### GitHub Pages (free):
1. Push files to a GitHub repository
2. Go to Settings → Pages → select branch → Save
3. Your site will be at `https://username.github.io/repo-name/`

## Tech Stack
- **HTML5** — semantic markup
- **CSS3** — custom properties, CSS Grid, flexbox, animations
- **JavaScript** — ES modules, no dependencies
- **SVG** — self-contained vector illustrations
- **Node.js** — local dev server only (no npm packages needed)

## License
© MECHABOTS. Student startup project.
