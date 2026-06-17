# FinanceOS 2.0

AI-powered financial management system built with Next.js 15, TypeScript, Tailwind CSS, and Supabase.

## Features

- **Initial Configuration Screen** - Setup Supabase and Gemini API credentials on first launch
- **Responsive Design** - Works on desktop (responsive sidebar) and mobile (collapsible navigation)
- **Modern UI** - Built with Tailwind CSS and Lucide icons
- **Type-Safe** - Full TypeScript support with Zod schema validation
- **Navigation** - Sidebar with 9 main sections (Dashboard, AI Inbox, Accounts, Transactions, Budgets, Projects, Investments, Reports, Settings)
- **Global Search** - Search bar in navbar
- **Floating Action Button** - Quick access button for new items

## Tech Stack

- **Framework**: Next.js 15
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: Lucide React
- **Form Handling**: React Hook Form
- **Validation**: Zod
- **Backend**: Supabase
- **AI**: Google Gemini API

## Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the app.

On first launch, you'll be prompted to enter:
1. **Supabase Project URL** (must start with `https://`)
2. **Supabase Anon Key** (must start with `eyJ`, min 100 chars)
3. **Gemini API Key** (must start with `AIza`, min 30 chars)

The app will test each connection before saving to localStorage.

### Configuration

Configuration is stored in `localStorage` under the key `financeos_config` and persists across sessions.

## Project Structure

```
.
├── app/                  # Next.js app directory
│   ├── layout.tsx       # Root layout
│   ├── page.tsx         # Home/auth page
│   ├── globals.css      # Global styles
│   └── [sections]/      # Stub pages for each section
├── components/          # React components
│   ├── ConfigScreen.tsx # Initial setup form
│   ├── Navbar.tsx       # Top navigation
│   ├── Sidebar.tsx      # Left sidebar (desktop) / drawer (mobile)
│   ├── Shell.tsx        # Main layout wrapper
│   └── FloatingActionButton.tsx
├── lib/                 # Utilities
│   └── config.ts        # Config schema, store, and API tests
└── public/              # Static assets
```

## Mobile Responsiveness

- **Desktop (≥768px)**: Permanent sidebar + full navbar
- **Mobile (<768px)**: Collapsible drawer + responsive navbar with menu toggle

## Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run lint` - Run ESLint

## Future Development

- Dashboard analytics and charts
- Account management and linking
- Transaction tracking and categorization
- Budget creation and monitoring
- Investment portfolio tracking
- AI-powered insights and recommendations
- Report generation
- User settings and preferences
