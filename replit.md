# Overview

BuildPro is a comprehensive construction management application built as a full-stack web platform. The system provides project managers, site supervisors, and workers with tools to manage construction projects, track tasks, monitor materials, generate daily reports, and coordinate team activities. The application follows a modern web architecture with a React frontend, Express.js backend, and PostgreSQL database, designed to streamline construction workflows and improve project visibility.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development patterns
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management and caching
- **UI Components**: Radix UI primitives with shadcn/ui component library for consistent, accessible design
- **Styling**: Tailwind CSS with custom design tokens and CSS variables for theming
- **Build Tool**: Vite for fast development and optimized production builds

## Backend Architecture
- **Runtime**: Node.js with Express.js framework for RESTful API endpoints
- **Language**: TypeScript with ES modules for type safety and modern JavaScript features
- **Database ORM**: Drizzle ORM for type-safe database operations and schema management
- **Session Management**: Express sessions with PostgreSQL storage using connect-pg-simple
- **Development**: Hot module replacement and error overlay for development experience

## Database Design
- **Primary Database**: PostgreSQL for reliable data persistence
- **Connection**: Neon serverless PostgreSQL with connection pooling
- **Schema Management**: Drizzle Kit for migrations and schema versioning
- **Core Entities**:
  - Users with role-based access (admin, project-manager, site-supervisor, laborer)
  - Projects with status tracking and timeline management
  - Tasks with assignments and progress monitoring
  - Daily reports with weather and progress documentation
  - Materials inventory and usage tracking
  - Equipment management and allocation
  - Attendance tracking for workforce management

## Authentication & Authorization
- **Session-based Authentication**: Server-side session management with secure cookies
- **Role-based Access Control**: Four distinct user roles with appropriate permissions
- **User Management**: Profile management with avatar support and contact information

## API Architecture
- **RESTful Design**: Standard HTTP methods with consistent endpoint patterns
- **Error Handling**: Centralized error middleware with structured error responses
- **Request Validation**: Zod schema validation for type-safe API contracts
- **Response Format**: JSON API responses with consistent error messaging

## Development & Deployment
- **Type Safety**: End-to-end TypeScript with shared schema definitions
- **Code Organization**: Monorepo structure with client, server, and shared directories
- **Path Mapping**: TypeScript path aliases for clean import statements
- **Build Pipeline**: Separate client and server builds with ESBuild for production

# External Dependencies

## Database Services
- **Neon Database**: Serverless PostgreSQL hosting with connection pooling
- **connect-pg-simple**: PostgreSQL session store for Express sessions

## UI & Styling
- **Radix UI**: Headless UI primitives for accessibility and customization
- **shadcn/ui**: Pre-built component library built on Radix UI
- **Tailwind CSS**: Utility-first CSS framework with custom design system
- **Lucide React**: Icon library for consistent iconography

## Development Tools
- **Vite**: Frontend build tool with hot module replacement
- **ESBuild**: Fast JavaScript bundler for production builds
- **Drizzle Kit**: Database migration and schema management tools
- **TanStack Query**: Server state management and caching library

## Form & Validation
- **React Hook Form**: Form management with validation
- **Zod**: Runtime type validation and schema definition
- **@hookform/resolvers**: Integration between React Hook Form and Zod

## Date & Utilities
- **date-fns**: Date manipulation and formatting utilities
- **clsx & class-variance-authority**: Conditional CSS class management
- **cmdk**: Command palette and search functionality