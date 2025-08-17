# 🚀 AI Career Coach - Professional Success Platform

A comprehensive AI-powered career coaching platform built with Next.js 15, featuring personalized guidance, interview preparation, and intelligent career tools to accelerate professional growth.

![AI Career Coach Banner](./public/banner.jpeg)

## ✨ Features

### 🧠 Core AI-Powered Features
- **Personalized Career Guidance**: Get tailored career advice powered by Google's Gemini AI
- **Industry Insights**: Real-time industry trends, salary data, and market analysis
- **Smart Resume Builder**: ATS-optimized resume creation with AI assistance
- **AI Cover Letter Generator**: Create compelling cover letters tailored to specific job descriptions
- **Interview Preparation**: Role-specific question practice with instant AI feedback
- **Performance Analytics**: Track your progress with detailed performance metrics

### 🎯 Key Capabilities
- **User Onboarding**: Complete profile setup with industry specialization
- **Dashboard Analytics**: Comprehensive career insights and statistics
- **Mock Interviews**: Practice sessions with AI-powered feedback
- **Resume Enhancement**: AI-powered content improvement suggestions
- **Industry-Specific Content**: Customized content based on your professional field
- **Progress Tracking**: Monitor your career development over time

## 🏗️ Tech Stack

### Frontend
- **Framework**: Next.js 15 with App Router
- **UI Components**: Radix UI + shadcn/ui
- **Styling**: Tailwind CSS 4
- **Icons**: Lucide React
- **Charts**: Recharts
- **Forms**: React Hook Form + Zod validation
- **Theming**: next-themes with dark mode support

### Backend & Database
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: Clerk (with dark theme support)
- **AI Integration**: Google Gemini AI API
- **Background Jobs**: Inngest
- **File Processing**: html2pdf.js for resume export
- **Notifications**: Sonner toast notifications

### Development Tools
- **Language**: TypeScript
- **Code Quality**: ESLint
- **Styling**: PostCSS
- **Build Tool**: Turbopack (Next.js)

## 📁 Project Structure

```
├── app/                      # Next.js App Router
│   ├── (auth)/              # Authentication pages
│   │   ├── sign-in/
│   │   └── sign-up/
│   ├── (main)/              # Main application pages
│   │   ├── dashboard/       # Industry insights & analytics
│   │   ├── resume/          # Resume builder
│   │   ├── ai-cover-letter/ # Cover letter generator
│   │   ├── interview/       # Interview preparation
│   │   └── onboarding/      # User onboarding flow
│   ├── api/                 # API routes
│   └── globals.css          # Global styles
├── components/              # Reusable UI components
│   ├── ui/                  # shadcn/ui components
│   ├── header.jsx           # Navigation header
│   └── hero.jsx             # Landing page hero
├── actions/                 # Server actions
│   ├── dashboard.js         # Dashboard data & AI insights
│   ├── resume.js            # Resume management
│   ├── cover-letter.js      # Cover letter operations
│   ├── interview.js         # Interview assessments
│   └── user.js              # User profile management
├── lib/                     # Utility functions
│   ├── prisma.js            # Database client
│   ├── checkUser.js         # User authentication helper
│   └── inngest/             # Background job configuration
├── data/                    # Static data
│   ├── features.js          # Feature descriptions
│   ├── testimonial.js       # User testimonials
│   └── faqs.js              # Frequently asked questions
├── hooks/                   # Custom React hooks
├── prisma/                  # Database schema
└── public/                  # Static assets
```

## 🗄️ Database Schema

### Core Models
- **User**: User profiles with industry specialization and skills
- **Assessment**: Interview performance tracking
- **Resume**: AI-enhanced resume content management
- **CoverLetter**: Job-specific cover letter generation
- **IndustryInsight**: Real-time industry data and trends

### Key Relationships
- Users can have multiple assessments and cover letters
- Each user has one resume and industry insight connection
- Industry insights include salary ranges, growth rates, and skill recommendations

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm
- PostgreSQL database
- Google Gemini API key
- Clerk authentication setup

### Environment Variables
Create a `.env.local` file with the following variables:

```env
# Database
DATABASE_URL="postgresql://username:password@localhost:5432/ai-career-coach"

# Authentication (Clerk)
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

# AI Integration
GEMINI_API_KEY=your_google_gemini_api_key

# Background Jobs (Inngest)
INNGEST_EVENT_KEY=your_inngest_event_key
INNGEST_SIGNING_KEY=your_inngest_signing_key
```

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd AI-Career-Coach-master
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up the database**
   ```bash
   # Generate Prisma client
   npx prisma generate
   
   # Run database migrations
   npx prisma db push
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

### Additional Scripts

```bash
# Build for production
npm run build

# Start production server
npm start

# Run linting
npm run lint

# Type checking
npm run type-check
```

## 🎨 Key Features Walkthrough

### 1. Landing Page
- Hero section with animated gradients
- Feature highlights with icons
- User testimonials and success stories
- FAQ section for common questions
- Call-to-action for user registration

### 2. User Onboarding
- Industry selection and specialization
- Experience level assessment
- Skills inventory and bio setup
- Automatic industry insights generation

### 3. Dashboard
- Personalized industry insights
- Salary benchmarking data
- Market trends and growth projections
- Recommended skills for career advancement
- Performance statistics overview

### 4. Resume Builder
- Markdown-based resume editor
- AI-powered content enhancement
- ATS optimization suggestions
- Real-time preview and editing
- PDF export functionality

### 5. Cover Letter Generator
- Job description analysis
- Company-specific customization
- AI-generated compelling content
- Multiple cover letter management
- Template-based generation

### 6. Interview Preparation
- Industry-specific question banks
- Mock interview simulations
- Performance analytics and scoring
- Improvement recommendations
- Progress tracking over time

## 🔧 Configuration

### Prisma Configuration
The project uses a custom Prisma client generated to `lib/generated/prisma` to avoid conflicts. The schema includes comprehensive models for user management, assessments, and career content.

### Clerk Authentication
Configured with dark theme support and custom appearance settings. Handles user registration, authentication, and profile management seamlessly.

### AI Integration
Google Gemini AI powers:
- Industry insights generation
- Resume content improvement
- Cover letter creation
- Interview question generation
- Performance feedback

## 📱 Responsive Design
- Mobile-first responsive design
- Dark/light theme support
- Accessible UI components
- Touch-friendly interactions
- Optimized for all screen sizes

## 🚀 Deployment

### Environment Setup
1. Set up PostgreSQL database
2. Configure Clerk authentication
3. Obtain Google Gemini API key
4. Set up Inngest for background jobs

### Recommended Platforms
- **Vercel**: Seamless Next.js deployment
- **Railway/Supabase**: PostgreSQL hosting
- **Environment Variables**: Configure all required secrets

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Made with 💗 by Arbaz**

## 🙏 Acknowledgments

- Next.js team for the amazing framework
- shadcn/ui for beautiful UI components
- Clerk for seamless authentication
- Google for Gemini AI capabilities
- Vercel for deployment platform

---

*Accelerate your career with AI-powered guidance and tools designed for professional success!*
