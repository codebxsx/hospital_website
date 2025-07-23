# Arth Hospital Website

## Overview

Arth Hospital is a modern healthcare website built with React and Express.js, featuring a responsive design, contact forms, appointment booking, and comprehensive information about medical services. The application follows a full-stack architecture with a PostgreSQL database for data persistence.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Styling**: Tailwind CSS with shadcn/ui components for consistent design
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Animations**: Framer Motion for smooth animations and transitions
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript for type safety
- **Database**: PostgreSQL with Drizzle ORM
- **Validation**: Zod schemas for request/response validation
- **Session Management**: Express sessions with PostgreSQL store
- **Development**: Hot reload with Vite integration

### Key Design Decisions

**Monorepo Structure**: The application uses a monorepo with shared TypeScript types and schemas between client and server, ensuring type safety across the full stack.

**Component Architecture**: Modular component design with reusable UI components from shadcn/ui, customized with healthcare-specific theming.

**Database Schema**: Simple relational design with tables for users, contact submissions, and appointments, using Drizzle ORM for type-safe database operations.

## Key Components

### Frontend Components
- **Navigation**: Fixed navigation with smooth scrolling to sections
- **Hero Section**: Full-screen landing area with call-to-action buttons
- **Services Grid**: Interactive grid showcasing medical services
- **Doctor Profiles**: Card-based doctor information with ratings
- **Contact Section**: Form handling with validation and error states
- **Appointment Booking**: Integrated booking system with doctor selection

### Backend Components
- **API Routes**: RESTful endpoints for contact forms and appointments
- **Storage Layer**: Abstracted storage interface with in-memory fallback
- **Middleware**: Request logging and error handling
- **Database Integration**: Drizzle ORM with PostgreSQL connection

## Data Flow

1. **User Interaction**: Users interact with React components
2. **Form Submission**: Forms use React Hook Form with Zod validation
3. **API Communication**: TanStack Query handles API requests to Express backend
4. **Data Validation**: Server validates requests using shared Zod schemas
5. **Database Operations**: Drizzle ORM performs type-safe database operations
6. **Response Handling**: Success/error states managed by React Query and toast notifications

## External Dependencies

### Production Dependencies
- **UI Framework**: Radix UI primitives for accessible components
- **Database**: Neon Database (PostgreSQL) for cloud hosting
- **Styling**: Tailwind CSS for utility-first styling
- **Validation**: Zod for schema validation
- **Animations**: Framer Motion for enhanced UX
- **Date Handling**: date-fns for date operations

### Development Dependencies
- **Build Tools**: Vite, esbuild for fast builds
- **Type Checking**: TypeScript for static type analysis
- **Database Tools**: Drizzle Kit for migrations and schema management

## Deployment Strategy

### Build Process
1. **Frontend Build**: Vite builds React app to `dist/public`
2. **Backend Build**: esbuild bundles Express server to `dist/index.js`
3. **Database Migration**: Drizzle Kit manages schema migrations

### Environment Configuration
- **Development**: Uses Vite dev server with Express API proxy
- **Production**: Serves static files from Express with API routes
- **Database**: PostgreSQL connection via DATABASE_URL environment variable

### Hosting Requirements
- Node.js environment for Express server
- PostgreSQL database (configured for Neon Database)
- Static file serving capability for React build
- Environment variables for database connection

The application is designed to be easily deployable to platforms like Vercel, Netlify, or traditional hosting providers with Node.js support.