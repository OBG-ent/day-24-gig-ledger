# GigLedger 💰

**Every shift, every kilometre, every dollar — the earnings tracker built for couriers and gig drivers.**

Gig workers juggle three jobs at once: the work itself, the kilometres, and the paperwork. GigLedger keeps the money side in one place — log a shift in ten seconds and instantly see your **net pay, effective $/hour, and effective $/km**, the two numbers that tell you whether a gig is actually worth it.

## ✨ Features

- ➕ **Fast shift logging** — date, client/platform, hours, kilometres, gross pay, and expenses with categories
- 📊 **Live stat cards** — net earnings, gross, expenses, effective $/hour and $/km, updated on every entry
- 📈 **Canvas bar chart** — net earnings by day for your last 14 logged days (hand-rolled, no chart library)
- 🧾 **Mileage deduction estimator** — set your own per-km rate and see what your logged kilometres are worth at tax time
- 💾 **Auto-save** — everything persists in `localStorage`; refresh-safe, account-free, works offline
- ⬇ **CSV export** — one click downloads your full ledger for spreadsheets or your accountant
- 🎞️ **Sample week built in** — load a realistic courier week and explore before logging your own
- 🔒 **Private by design** — zero backend, zero tracking; your data never leaves your browser

## 🚀 Run it in 30 seconds

No build tools, no server needed:

1. Download or clone this repo
2. Double-click **`index.html`** — that's it

Or serve it locally:

```bash
npx serve .
# then open the URL it prints
```

**Try this:** click **Load sample week**, then check the stat cards — notice how the delivery-app shifts earn more gross but less per kilometre than the courier shifts once expenses land. That gap is exactly what GigLedger exists to expose.

## 🧠 What I practiced

- State-driven rendering — one `entries` array, one `render()` that repaints stats, table, and chart
- `localStorage` persistence with corruption guards on load
- Hand-drawn Canvas charts (bar scaling, value labels, negative-value handling)
- CSV generation with proper quoting/escaping + `Blob` download
- Defensive input handling — form parsing that never lets a bad number poison the totals
- Event delegation for row deletion

## 🗂️ Project structure

```
day-24-gig-ledger/
├── index.html   # the whole app — markup, styles, and logic in one file
└── README.md
```

## 🔮 Ideas for v2

- Weekly/monthly summaries with per-client breakdowns
- Import a CSV back into the ledger
- Goal tracking ("rent is $X — you're 62% there")

---

Day 24 of my daily coding streak — one simple build and one bigger build, every day. Follow along: [@Reynoldobago](https://x.com/Reynoldobago) · [github.com/OBG-ent](https://github.com/OBG-ent)
