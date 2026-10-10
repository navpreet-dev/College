# Shivaji College Website

**A modern, responsive website for a college: programs, admissions, campus life, events and portals, plus an AI chat assistant and a working contact form.**

🔗 **Live demo:** [college-alpha-amber.vercel.app](https://college-alpha-amber.vercel.app)

![Next.js](https://img.shields.io/badge/Next.js-16-000000?logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-6-2D3748?logo=prisma&logoColor=white)
![Gemini](https://img.shields.io/badge/AI-Gemini-8E75B2?logo=googlegemini&logoColor=white)
![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-000000?logo=vercel&logoColor=white)

![Shivaji College home page](screenshots/home.png)

## Features

**17 pages in one fast app**
- Home, About, Academics, Admissions, Research, Campus Life, Library
- News, Events, Careers, Alumni, Downloads, Grievance and Contact
- Student Portal and Faculty Portal (demo screens, login disabled in the preview)
- Hash-based routing (`/#/academics`) so every page has its own shareable link

**AI chat assistant**
- Floating chatbot that answers questions about the college
- Powered by Google Gemini (`gemini-2.0-flash`), with a built-in fallback reply when the AI is unavailable

**Contact form**
- Messages are saved to the database first (`ContactSubmission` table)
- Email notification sent via SMTP with Nodemailer

**Design**
- Clean navy-and-gold design with animated stats and bento-style sections
- Fully responsive with a mobile menu

## Screenshots

<table>
  <tr>
    <td align="center"><img src="screenshots/programs.png" width="400" alt="About and programs"><br><sub>About & programs</sub></td>
    <td align="center"><img src="screenshots/academics.png" width="400" alt="Academics"><br><sub>Academics</sub></td>
  </tr>
  <tr>
    <td align="center" colspan="2"><img src="screenshots/admissions.png" width="400" alt="Admissions"><br><sub>Admissions</sub></td>
  </tr>
</table>

## Tech stack

| Layer | Tools |
|---|---|
| Framework | Next.js 16 (App Router, API routes), React 19, TypeScript |
| Styling / UI | Tailwind CSS 4, shadcn/ui (Radix UI), Framer Motion, Lucide icons |
| AI | Google Gemini API |
| Email | Nodemailer (SMTP) |
| Database | Prisma 6 ORM with PostgreSQL |
| Hosting | Vercel |

## Getting started

```bash
git clone https://github.com/navpreet-dev/College.git
cd College
npm install
```

Create a `.env` file (placeholders only — use your own values):

```env
DATABASE_URL="postgresql://user:password@host:5432/dbname"
GEMINI_API_KEY="your-gemini-api-key-here"
SMTP_HOST="smtp.example.com"
SMTP_PORT="587"
SMTP_USER="your-smtp-username"
SMTP_PASS="your-smtp-password"
SMTP_FROM="no-reply@example.com"
CONTACT_EMAIL="inbox@example.com"
```

```bash
npm run db:generate
npm run db:push
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Scripts

| Command | What it does |
|---|---|
| `npm run dev` | Start the dev server on port 3000 |
| `npm run build` | Production (standalone) build |
| `npm run start` | Run the standalone production server |
| `npm run lint` | Lint with ESLint |
| `npm run db:push` | Push the Prisma schema to the database |
| `npm run db:generate` | Generate the Prisma client |
| `npm run db:migrate` | Create and apply a migration |
| `npm run db:reset` | Reset the database |

## How to use the site

1. **Explore** — use the top menu to visit Academics, Admissions, Campus Life and more.
2. **Ask the assistant** — click the chat button in the corner and ask anything about the college.
3. **Apply** — the Admissions page walks through the steps to apply.
4. **Stay updated** — check News and Events for what's happening on campus.
5. **Get in touch** — send a message from the Contact page.

## Disclaimer

This is a portfolio project. College details on the site are for demonstration.

## Author

**Navpreet Singh**

- GitHub: [@navpreet-dev](https://github.com/navpreet-dev)
- LinkedIn: [navpreetsingh-dev](https://www.linkedin.com/in/navpreetsingh-dev)

If you like this project, a ⭐ on the repo is appreciated.
