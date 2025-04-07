# AI Career Coach

A full-stack application that provides personalized career guidance, interview preparation, and AI-powered tools for professional success.

![AI Career Coach](https://github.com/user-attachments/assets/eee79242-4056-4d19-b655-2873788979e1)

## Features

- **Personalized Career Guidance**: Get tailored advice based on your industry and experience
- **Interview Preparation**: Practice with AI-generated interview questions and receive feedback
- **Resume Builder**: Create and optimize your resume with AI assistance
- **Cover Letter Generator**: Generate customized cover letters for job applications
- **Industry Insights**: Access up-to-date information about your industry's trends and salary data
- **Skills Assessment**: Evaluate your skills and get recommendations for improvement

## Tech Stack

- **Frontend**: Next.js, React, Tailwind CSS, Shadcn UI
- **Backend**: Next.js API Routes
- **Database**: PostgreSQL (Neon DB)
- **ORM**: Prisma
- **Authentication**: Clerk
- **AI Integration**: Google Gemini API
- **Background Jobs**: Inngest

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- A Neon DB account for PostgreSQL database
- A Clerk account for authentication
- A Google AI Studio account for Gemini API access

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ai-career-coach.git
   cd ai-career-coach
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory with the following variables:
   ```
   # Database URL (Get this from Neon DB - https://neon.tech)
   DATABASE_URL="your-neon-db-connection-string"

   # Clerk Authentication Keys (Get these from https://dashboard.clerk.com/last-active?path=api-keys)
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your-clerk-publishable-key
   CLERK_SECRET_KEY=your-clerk-secret-key

   # Clerk Authentication URLs
   NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
   NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
   NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/onboarding
   NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding

   # Gemini API Key (Get this from Google AI Studio)
   GEMINI_API_KEY=your-gemini-api-key
   ```

4. Set up the database:
   ```bash
   npx prisma generate
   npx prisma db push
   ```

5. Start the development server:
   ```bash
   npm run dev
   ```

6. Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## Project Structure

- `/app`: Next.js app router pages and API routes
- `/components`: Reusable UI components
- `/lib`: Utility functions and database client
- `/prisma`: Database schema and migrations
- `/public`: Static assets

## Usage

1. **Sign Up/Login**: Create an account or log in using Clerk authentication
2. **Complete Onboarding**: Provide your industry and experience details
3. **Dashboard**: Access all features from the main dashboard
4. **Resume Builder**: Create and optimize your resume
5. **Interview Prep**: Practice with AI-generated questions
6. **Cover Letter Generator**: Create customized cover letters
7. **Industry Insights**: View trends and salary data for your industry

## Troubleshooting

### Common Issues

- **Database Connection Issues**: Ensure your Neon DB connection string is correct and the database is accessible
- **Authentication Errors**: Verify your Clerk API keys are correctly set in the `.env` file
- **AI Integration Problems**: Check that your Gemini API key is valid and has sufficient quota

### Prisma Permission Errors

If you encounter permission errors with Prisma on Windows, try running your terminal as administrator and then:

```bash
Remove-Item -Recurse -Force node_modules\.prisma
npm install
npx prisma generate
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Made with 💗 by Mardhav
