# ClauseGuard 🛡️

**ClauseGuard** is an AI-powered rental agreement analyzer and negotiation assistant built with Next.js. It helps tenants understand lease documents, flags unfair or one-sided clauses, and provides actionable counter-proposals to negotiate fairer terms with landlords.

---

## Features

- **AI-Powered Rental Scanning:** Scan upload or pasted rental agreements to detect unfair, one-sided, or illegal clauses.
- **Tenant Friendliness Score:** Get an instant evaluation of how favorable the lease is to you versus the landlord.
- **Visual Risk Breakdowns:** Highlighted original text side-by-side with risk analysis (High, Medium, and Low severity flags).
- **Negotiation Assistant Agent:** Drafts professional email templates and counter-proposals to send to landlords citing local rent rules or market standard practices.
- **Scan History:** Save your agreement analyses securely to reference or compare later.

---

## Tech Stack

- **Framework:** [Next.js 16 (App Router)](https://nextjs.org/)
- **Database ORM:** [Prisma](https://www.prisma.io/)
- **Database:** PostgreSQL (via Neon DB)
- **Styling:** [Tailwind CSS v4](https://tailwindcss.com/)
- **Language:** [TypeScript](https://www.typescriptlang.org/)

---

## Getting Started

### 1. Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed on your machine.

### 2. Environment Setup

Create a `.env` file in the root directory (or use the existing one) and add the following variables:

```env
DATABASE_URL="your-postgresql-connection-string"
GEMINI_API_KEY="your-gemini-api-key"
```

### 3. Installation

Install the project dependencies:

```bash
npm install
```

### 4. Database Sync

Apply database schemas to your PostgreSQL database:

```bash
npx prisma db push
```

### 5. Running the Application

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

---

## Project Structure

```txt
├── app/                  # Next.js App Router (pages, layout, actions)
│   ├── scan/[id]/        # Interactive analysis dashboard
│   ├── layout.tsx        # Global layout & fonts
│   ├── page.tsx          # Landing page & file uploader
│   └── globals.css       # Tailwind CSS styles
├── lib/                  # Shared services (DB client, LLM analyzer agent)
├── prisma/               # Database schemas & configurations
```
