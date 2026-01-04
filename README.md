# Dcode-LMS

A comprehensive Learning Management System (LMS) platform built with React, TypeScript, and Supabase.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

* **Node.js** (version 18 or higher) - [Download Node.js](https://nodejs.org/)
* **npm** (comes with Node.js) or **yarn**
* **Git** - [Download Git](https://git-scm.com/)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Dcode-LMS.git
cd Dcode-LMS
```

### 2. Install Dependencies

Install all project dependencies using npm:

```bash
npm install
```

Or if you prefer using yarn:

```bash
yarn install
```

### 3. Set Up Environment Variables

Create a `.env.local` file in the root directory:

```bash
cp env.local.template .env.local
```

Then edit `.env.local` with your Supabase credentials:

* `VITE_SUPABASE_URL` - Your Supabase project URL
* `VITE_SUPABASE_ANON_KEY` - Your Supabase anonymous key

You can get these from your Supabase project dashboard: Settings → API

### 4. Start Development Server

Run the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:3000` (or the port shown in the terminal).

## Available Scripts

* `npm run dev` - Start development server
* `npm run build` - Build for production
* `npm run build:prod` - Build for production (optimized)
* `npm run preview` - Preview production build locally
* `npm run lint` - Run ESLint to check code quality

## Project Structure

```
Dcode-LMS/
├── src/                 # Source code
│   ├── components/      # React components
│   ├── pages/           # Page components
│   ├── services/        # API services
│   └── lib/             # Utility libraries
├── public/              # Static assets
├── docs/                # Documentation files
├── sql/                 # SQL scripts and migrations
├── backend/             # Backend server
├── supabase/            # Supabase functions
├── dist/                # Production build (generated)
├── node_modules/        # Dependencies (generated)
├── package.json         # Project dependencies
└── vite.config.ts       # Vite configuration
```

## Tech Stack

* **Frontend**: React 18, TypeScript
* **Build Tool**: Vite
* **Styling**: TailwindCSS
* **Backend**: Supabase
* **State Management**: React Hooks
* **Routing**: React Router DOM
* **Code Editor**: Monaco Editor
* **Animations**: Framer Motion

## Documentation

All documentation is available in the `docs/` folder. Key documents include:

* `docs/README.md` - Main documentation index
* `docs/LOCAL_DEVELOPMENT.md` - Local development setup guide
* `docs/DEPLOYMENT.md` - Deployment instructions
* `docs/SUPABASE_SETUP.md` - Supabase configuration guide

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is private and proprietary.

## Support

For support, please contact the development team or open an issue in the repository.

