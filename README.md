# Dcode-LMS

A comprehensive Learning Management System (LMS) platform built with React, TypeScript, and Supabase. Features include course management, student/mentor/admin dashboards, assessments, code playground, video learning, real-time collaboration, and AI-powered features.

## 🚀 Features

### Core Features
- **Multi-Role System**: Student, Mentor, and Admin dashboards with role-based access control
- **Course Management**: Create, manage, and deliver courses with rich content
- **Assessment System**: Comprehensive assessment creation and management with multiple question types
- **Code Playground**: Integrated IDE with support for multiple programming languages
- **Video Learning**: HLS video streaming with quality selection and progress tracking
- **Real-time Collaboration**: Live discussions, notifications, and updates
- **AI-Powered Features**: AI-generated assessments and automated grading
- **Learning Paths**: Structured learning journeys with progress tracking
- **Discussion Forums**: Interactive discussions between students and mentors
- **Achievement System**: Badges, certificates, and progress tracking
- **Resume Builder**: Integrated resume creation tool
- **Job Placements**: Career opportunities and placement tracking
- **Schedule Management**: Session scheduling and calendar integration
- **Analytics Dashboard**: Comprehensive analytics for students, mentors, and admins

### Assessment Features
- **Multiple Question Types**: Multiple choice, true/false, short answer, essay, coding, file upload
- **AI-Generated Assessments**: Automated question generation based on topics
- **Auto-Grading**: Automatic grading for objective questions
- **Manual Grading**: Support for subjective questions and coding challenges
- **Time Limits**: Configurable time limits for assessments
- **Attempt Tracking**: Multiple attempts with attempt history
- **Results Analytics**: Detailed performance analytics and reports
- **Accessibility**: WCAG 2.1 AA compliant with screen reader support

### Code Playground Features
- **Multi-Language Support**: C, C++, Java, Python, JavaScript, Go, and more
- **Monaco Editor**: Advanced code editor with syntax highlighting
- **Code Execution**: Real-time code execution with output display
- **Terminal Integration**: Interactive terminal for program execution
- **Judge0 Integration**: Code compilation and execution service
- **Piston API**: Alternative code execution engine
- **Save & Load**: Save code snippets and load previous work

### Video Learning Features
- **HLS Streaming**: Adaptive bitrate streaming for optimal quality
- **Quality Selection**: Multiple quality options (1080p, 720p, 480p, etc.)
- **Progress Tracking**: Automatic progress saving and resume
- **Playback Controls**: Standard video controls with speed adjustment
- **Subtitles Support**: Closed captions and subtitle support
- **Video Analytics**: Watch time and engagement tracking

## 📁 Project Structure

```
dcodesystems/
├── src/                          # Source code
│   ├── components/              # Reusable React components
│   │   ├── assessment/          # Assessment-related components
│   │   ├── base/                # Base UI components (Button, Card, Modal, etc.)
│   │   ├── celebration/         # Achievement celebration components
│   │   ├── editor/              # Rich text editor components
│   │   ├── feature/             # Feature-specific components
│   │   ├── Terminal/            # Terminal components
│   │   └── ui/                  # UI components
│   ├── contexts/                # React contexts
│   │   ├── SidebarSettingsContext.tsx
│   │   ├── ThemeContext.tsx
│   │   └── UserThemeContext.tsx
│   ├── hooks/                   # Custom React hooks
│   ├── i18n/                    # Internationalization
│   ├── lib/                     # Utility libraries
│   │   ├── auth.ts             # Authentication service
│   │   ├── supabaseAuth.ts     # Supabase auth implementation
│   │   ├── roleBasedAccess.ts  # Role-based access control
│   │   ├── notificationService.ts
│   │   ├── accessibilityService.ts
│   │   └── securityService.ts
│   ├── pages/                   # Page components
│   │   ├── admin/              # Admin dashboard pages
│   │   ├── auth/               # Authentication pages
│   │   ├── home/                # Home page
│   │   ├── mentor/             # Mentor dashboard pages
│   │   ├── product/             # Product showcase pages
│   │   └── student/            # Student dashboard pages
│   ├── router/                  # Routing configuration
│   ├── services/               # API services
│   │   ├── assessmentService.ts
│   │   ├── courseService.ts
│   │   ├── dataService.ts
│   │   └── analyticsService.ts
│   └── utils/                   # Utility functions
├── public/                       # Static assets
│   ├── judge0-ide/              # Judge0 IDE integration
│   └── [assets]                 # Images, logos, etc.
├── backend/                     # Backend server
│   ├── server.js               # Express server
│   └── [config files]          # Backend configuration
├── supabase/                    # Supabase functions
│   └── functions/               # Edge functions
│       ├── extract-video/
│       ├── send-email/
│       └── send-email-resend/
├── sql/                         # Database scripts (119 files)
│   ├── assessment-*.sql         # Assessment-related schemas
│   ├── course-*.sql            # Course-related schemas
│   ├── fix-*.sql               # Database fixes
│   └── setup-*.sql             # Setup scripts
├── docs/                        # Documentation (160 markdown files)
│   ├── ASSESSMENT_*.md         # Assessment documentation
│   ├── DEPLOYMENT.md           # Deployment guides
│   ├── JUDGE0_*.md             # Judge0 integration docs
│   └── [other guides]          # Various setup and troubleshooting guides
├── figma/                       # Design files
├── hls-output/                  # HLS video output
├── judge0 ide/                  # Judge0 IDE source
└── [config files]              # Configuration files
```

## 🛠️ Tech Stack

### Frontend
- **React 18** - UI library
- **TypeScript** - Type-safe development
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **React Router DOM** - Client-side routing
- **Framer Motion** - Animation library
- **Monaco Editor** - Code editor
- **React Quill** - Rich text editor
- **i18next** - Internationalization

### Backend
- **Supabase** - Backend as a Service (BaaS)
  - PostgreSQL database
  - Authentication
  - Row Level Security (RLS)
  - Storage
  - Edge Functions
- **Express.js** - Backend server (for additional services)
- **Node.js** - Runtime environment

### Code Execution
- **Judge0 API** - Code compilation and execution
- **Piston API** - Alternative code execution engine

### Video Processing
- **HLS.js** - HTTP Live Streaming
- **FFmpeg** - Video processing (via backend)

### Other Tools
- **Axios** - HTTP client
- **DOMPurify** - HTML sanitization
- **React Player** - Video player
- **Lottie React** - Animations
- **jsPDF** - PDF generation
- **html2canvas** - Screenshot generation

## 📦 Installation

### Prerequisites
- Node.js (version 18 or higher)
- npm or yarn
- Git
- Supabase account (for backend services)

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Chinnu891/Dcode-LMS.git
   cd Dcode-LMS
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp env.local.template .env.local
   ```
   
   Edit `.env.local` with your Supabase credentials:
   ```env
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Set up the database**
   - Go to your Supabase project dashboard
   - Navigate to SQL Editor
   - Run the SQL scripts from the `sql/` folder in order:
     - Start with `complete-database-setup.sql`
     - Then run other setup scripts as needed

5. **Start the development server**
   ```bash
   npm run dev
   ```

   The application will be available at `http://localhost:3000`

## 🚀 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run build:prod` - Build for production (optimized)
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint to check code quality
- `npm run serve` - Serve production build on port 3000

## 📚 Documentation

Comprehensive documentation is available in the `docs/` folder:

- **Setup Guides**: Database setup, deployment, local development
- **Feature Documentation**: Assessment system, code playground, video learning
- **Integration Guides**: Judge0, Piston API, Supabase setup
- **Troubleshooting**: Common issues and solutions
- **API Documentation**: Service layer documentation

## 🎯 Key Features in Detail

### Student Dashboard
- View enrolled courses
- Take assessments
- Track learning progress
- Participate in discussions
- View achievements
- Build resume
- Schedule sessions with mentors
- Access code playground

### Mentor Dashboard
- Create and manage courses
- Create assessments (manual or AI-generated)
- Upload course materials (videos, PDFs, etc.)
- Manage students
- View analytics
- Conduct live sessions
- Provide feedback
- Manage learning paths

### Admin Dashboard
- System-wide analytics
- User management
- Course oversight
- Assessment monitoring
- Payment management
- Integration management
- System settings
- Security monitoring

## 🔐 Security Features

- **Row Level Security (RLS)**: Database-level access control
- **Role-Based Access Control**: User role permissions
- **Authentication**: Supabase Auth with email/password
- **Audit Logging**: Comprehensive activity logging
- **Input Sanitization**: XSS protection
- **CORS Configuration**: Secure API access
- **Rate Limiting**: API rate limiting

## 🌐 Internationalization

The platform supports multiple languages through i18next:
- English (default)
- Additional languages can be added via the `src/i18n/` directory

## 📊 Database Schema

The database includes:
- **Users & Profiles**: User management and profiles
- **Courses**: Course content and metadata
- **Assessments**: Assessment system with questions and responses
- **Learning Paths**: Structured learning journeys
- **Discussions**: Forum and discussion threads
- **Notifications**: Real-time notifications
- **Analytics**: Performance and engagement data
- **Storage**: File and media storage

See `sql/` folder for complete database schemas.

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is private and proprietary.

## 🆘 Support

For support, please:
- Check the documentation in the `docs/` folder
- Open an issue in the repository
- Contact the development team

## 🔗 Links

- **Repository**: https://github.com/Chinnu891/Dcode-LMS
- **Supabase**: https://supabase.com
- **Judge0**: https://judge0.com
- **Vite**: https://vitejs.dev

## 📈 Project Statistics

- **Total Files**: 1000+ files
- **SQL Scripts**: 119 database scripts
- **Documentation**: 160 markdown files
- **React Components**: 100+ components
- **Pages**: 50+ page components
- **Services**: 22 API services
- **Lines of Code**: 50,000+ lines

## 🎉 Acknowledgments

- Supabase for the amazing backend platform
- Judge0 for code execution services
- Monaco Editor for the code editing experience
- All contributors and users of this platform

---

**Built with ❤️ by the Dcode Systems team**
