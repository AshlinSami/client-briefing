# Algorithm Agency — Client Briefing Portal v3

A personalised task intake system hosted on GitHub Pages. Clients get a direct link that pre-fills their details — they just describe the task and pick urgency. You get a structured email with P1/P2/P3 classification done automatically.

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The client-facing form |
| `thankyou.html` | Confirmation page shown after submission |
| `clients.html` | **Your internal tool** — generate personalised links per client |
| `README.md` | This guide |

---

## Setup (15 minutes)

### 1. Create GitHub repo & upload files
- Go to github.com → New repository → name it `client-briefing` → Public
- Upload all 4 files → Commit

### 2. Enable GitHub Pages
- Repo → Settings → Pages → Branch: main / (root) → Save
- Your URL: `https://YOUR-USERNAME.github.io/client-briefing/`

### 3. Set up Formspree
- Go to formspree.io → Sign in with GitHub → New Form
- Copy your Form ID (the code after `/f/`)

### 4. Add your Formspree ID
- Edit `index.html` on GitHub (pencil icon)
- Find: `const FORMSPREE_ID = 'YOUR_FORM_ID';`
- Replace `YOUR_FORM_ID` with your actual ID
- Commit

### 5. Test
- Open your live URL, submit a test → confirm Formspree's verification email → done

---

## Sending links to clients

Open `clients.html` on your live site:
`https://YOUR-USERNAME.github.io/client-briefing/clients.html`

This is your internal tool. Enter a client's name, company, and email → Generate link → Draft email (opens in your mail client pre-written) → Send.

The client clicks their personalised link and the form already knows who they are.

---

## How the priority mapping works

Clients never see P1/P2/P3. They pick plain English:

| Client sees | You get in email |
|-------------|-----------------|
| It's urgent | P1 — Critical · Same day / 24 hrs |
| This week   | P2 — Important · 2–5 business days |
| No rush     | P3 — Planned · 1–3 weeks |

---

## Optional upgrades

- **Slack alerts** — Formspree Dashboard → Integrations → Slack (free)
- **Google Sheets log** — Formspree Dashboard → Integrations → Google Sheets (free)
- **Custom domain** — GitHub Pages Settings → Custom Domain → add DNS CNAME
- **ClickUp auto-tasks** — Zapier: Formspree → ClickUp (~R350/month)

---

*Algorithm Agency — Internal. Questions: ashlin@algorithmAgency.co.za*
