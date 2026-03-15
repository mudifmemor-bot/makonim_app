# Makonim - Civic-Tech School Verification

Makonim is a Next.js 14 civic-tech web application that allows citizens to verify whether improvements promised for their schools actually happened.

## Quick Start (Hackathon Mode)

The project currently uses **mock data fallback** out of the box so you can start developing and demoing immediately without setting up Supabase.

1. Ensure you have Node.js 18+ installed.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.

## Supabase Setup Instructions

If you want to use the real database:

1. Create a new project on [Supabase.com](https://supabase.com/).
2. Go to the **SQL Editor** in your Supabase dashboard.
3. Copy and paste the contents of `supabase/schema.sql` and click **Run**.
4. Copy and paste the contents of `supabase/seed.sql` and click **Run**.
5. Go to **Storage** and create a bucket named `photos`. Make it public.

## Environment Variables Needed

You need the following environment variables. In your local repository, copy `.env.example` to `.env.local` and substitute your actual values from the **Project Settings -> API** section of your Supabase dashboard.

```env
NEXT_PUBLIC_SUPABASE_URL=https://your-project-id.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
```

## Deployment Instructions for Vercel

1. Push your code to a GitHub repository.
2. Go to [Vercel](https://vercel.com/) and click **Add New Project**.
3. Import your GitHub repository.
4. In the "Environment Variables" step, add `NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_ANON_KEY`.
5. Click **Deploy**. Vercel will automatically build your Next.js project.

## Project Structure

- `app/` - Next.js App Router pages (map, schools, verify, dashboard)
- `components/` - React components, including shadcn/ui and Leaflet Map
- `lib/` - Supabase client setup and mock data APIs
- `supabase/` - SQL schema and seed data for setting up the backend

## Features

- **Interactive Map**: Built with Leaflet to visualize school statuses.
- **Reporting System**: Mobile-responsive form for uploading photos and registering promises statuses.
- **Dashboard**: Real-time charts utilizing Recharts and a top-user leaderboard.
- **Modern UI**: Styled with TailwindCSS and custom shadcn/ui components for a premium look.
