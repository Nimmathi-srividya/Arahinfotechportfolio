# replit.md

## Overview

This is a full-stack web application for Arah Infotech, a software development and AI solutions company. The application serves as a company portfolio website showcasing services, team capabilities, and client work. It features a modern React frontend with shadcn/ui components, an Express.js backend API, and PostgreSQL database integration using Drizzle ORM. The site includes contact forms, newsletter subscriptions, and comprehensive information about the company's technology services including web development, mobile apps, AI/ML, and cloud security.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **UI Library**: shadcn/ui components built on Radix UI primitives with Tailwind CSS for styling
- **State Management**: TanStack Query (React Query) for server state management and API caching
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation for type-safe form submissions
- **Styling**: Tailwind CSS with CSS custom properties for theming, including dark mode support

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **API Pattern**: RESTful API design with JSON responses
- **Request Processing**: Express middleware for JSON parsing, URL encoding, and request logging
- **Error Handling**: Centralized error handling middleware with structured error responses
- **Development Tools**: TSX for TypeScript execution in development, ESBuild for production builds

### Data Storage Solutions
- **Database**: PostgreSQL with Neon serverless hosting
- **ORM**: Drizzle ORM for type-safe database operations
- **Schema Management**: Drizzle Kit for migrations and schema management
- **Fallback Storage**: In-memory storage implementation for development/testing
- **Database Tables**: Users, contact submissions, and newsletter subscriptions with UUID primary keys

### Authentication and Authorization
- **Current State**: Basic user schema exists but authentication is not implemented
- **Prepared Infrastructure**: User table with username/password fields ready for future auth implementation
- **Session Management**: Connect-pg-simple package available for PostgreSQL session storage

## External Dependencies

### Third-party Services
- **Database Hosting**: Neon serverless PostgreSQL (configured via DATABASE_URL)
- **Email Service**: Not currently implemented but newsletter subscription endpoint exists
- **Image Assets**: Unsplash for stock photography in UI components

### Development and Deployment
- **Replit Integration**: Vite plugins for Replit development environment including error modal and cartographer
- **Build Process**: Vite for frontend bundling, ESBuild for backend compilation
- **Development Server**: Hot reload and middleware integration between Vite dev server and Express

### UI and Styling Dependencies
- **Component Library**: Comprehensive shadcn/ui component collection including forms, dialogs, navigation
- **Icons**: Lucide React for general icons, React Icons for brand/social media icons
- **Styling**: Tailwind CSS with PostCSS for processing, class-variance-authority for component variants
- **Utilities**: clsx and tailwind-merge for conditional styling, date-fns for date handling

### Form and Data Validation
- **Validation**: Zod for runtime type checking and schema validation
- **Form Integration**: React Hook Form with Zod resolver for form validation
- **Database Validation**: Drizzle-zod for consistent validation between client and database schemas