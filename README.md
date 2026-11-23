# Sany3y (صنايعي) — Frontend

Frontend web application for **Sany3y**, an Arabic (RTL) home services and maintenance marketplace connecting customers with skilled technicians, craftspeople, and local shops across Egypt.

## Tech Stack

- **Framework:** Next.js 15 (App Router) & React 19
- **Language:** TypeScript 5
- **Styling & Icons:** Bootstrap 5 (RTL), Font Awesome 6, Cairo Google Font
- **Real-Time Communication:** Microsoft SignalR (`@microsoft/signalr`) for live chat (`/chatHub`) and online presence (`/userStatusHub`)
- **Charts & Notifications:** Chart.js (`react-chartjs-2`), Sonner
- **Contact Form:** EmailJS (`@emailjs/browser`)

## Getting Started

### Prerequisites

- Node.js (v18+ recommended) and `npm`
- Running Sany3y backend API (defaults to `https://localhost:7178`)

### Installation

```bash
npm install
```

### Environment Variables

Create a `.env.local` file in the `frontend` directory if your backend runs on a custom URL:

```env
NEXT_PUBLIC_API_URL=https://localhost:7178
```

If omitted, the app defaults to `https://localhost:7178` (configured in `src/lib/api.ts`).

### Available Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the development server on `http://localhost:3000` |
| `npm run build` | Build the production bundle |
| `npm run start` | Start the production server on port `3000` |
| `npm run lint` | Run Next.js ESLint checks |

## Key Routes

- **Public:** `/`, `/about`, `/services`, `/services/[id]`, `/shops`, `/shops/[id]`, `/contact`, `/policy`
- **Authentication & Account:** `/login`, `/register`, `/register-shop`, `/complete-profile`, `/confirm-email`, `/confirm-email-notice`, `/resend-confirmation`, `/forgot-password`, `/reset-password`, `/profile`
- **Role Dashboards:** `/dashboard/customer`, `/dashboard/worker`, `/dashboard/shop`
- **Messaging:** `/chat/[id]` (plus global floating chat widget)
- **Payments:** `/payment/success`, `/payment/cancel`
- **Admin Panel:** `/admin`, `/admin/categories`, `/admin/shops`, `/admin/users`

## Project Structure

```text
frontend/
├── public/                 # Static assets and images
└── src/
    ├── app/                # Next.js App Router pages and layouts
    ├── components/         # Shared UI components (Navbar, Footer, FloatingChatWidget, etc.)
    ├── context/            # React contexts (AuthContext, SignalRContext)
    ├── lib/                # API fetch and file download helpers
    └── types/              # Shared TypeScript interfaces and types
```
