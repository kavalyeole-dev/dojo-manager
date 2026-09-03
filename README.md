# Dojo Manager — MKSF Foundation

A lightweight, single-page web app for running the day-to-day admin of a karate class: taking attendance, tracking monthly fees, and generating payment receipts — built for a single instructor managing 30–100 students.

No login, no backend, no monthly subscription. It runs entirely in the browser and saves data locally on the device it's used on.

## Features

- **Student roster** — add, edit, and remove students with belt rank, parent name/contact, join date, and monthly fee
- **Attendance tracking** — mark students present or absent per session date; attendance history and per-student attendance percentage are calculated automatically
- **Fee management** — see who's paid and who owes money for any given month, and record new payments (amount, method, date)
- **Payment receipts** — every recorded payment generates a receipt with a unique receipt number, ready to show the parent as proof of payment, and printable
- **Records log** — a searchable, filterable history of every attendance mark and every payment ever recorded
- **Dashboard** — an at-a-glance view of today's turnout, this month's collections, pending fees, and overall attendance

## Tech stack

- [React](https://react.dev/) (functional components + hooks)
- [Vite](https://vitejs.dev/) for local development and bundling
- [lucide-react](https://lucide.dev/) for icons
- Plain CSS (custom properties / design tokens, no framework) for styling
- Data persistence via the browser's `localStorage` — no server or database required

## Getting started

### Prerequisites
- [Node.js](https://nodejs.org/) (LTS version)

### Installation
```bash
git clone <this-repo-url>
cd dojo-manager
npm install
```

### Run locally
```bash
npm run dev
```
Open the printed local address (usually `http://localhost:5173`) in your browser.

### Build for production
```bash
npm run build
```
This outputs a static, deployable site to the `dist/` folder — ready to host on any static hosting provider (Netlify, Vercel, GitHub Pages, etc.).

## Data & privacy

All data (students, attendance, payments) is stored **locally in the browser** using `localStorage`. Nothing is sent to a server. This means:
- Data does not sync across different devices or browsers
- Clearing the browser's site data will erase the records
- There is currently no built-in backup/export — back up important data manually if needed

## Roadmap ideas

- Monthly (not just all-time) attendance percentages
- CSV/Excel export of attendance and payment records
- Multi-device sync via a lightweight backend
- Automated SMS/email payment confirmations to parents

