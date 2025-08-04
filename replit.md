# Overview

This is a full-stack web application featuring a personal portfolio website for Raghav Duggal, a Strategic HR Business Partner. The application is built with React on the frontend and Express.js on the backend, using modern web technologies including TypeScript, Tailwind CSS, and shadcn/ui components. The project follows a monorepo structure with shared schemas and types between client and server.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript and Vite as the build tool
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **UI Components**: shadcn/ui component library built on Radix UI primitives
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management
- **Form Handling**: React Hook Form with Zod validation through @hookform/resolvers

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM configured for PostgreSQL
- **Session Storage**: PostgreSQL-backed sessions using connect-pg-simple
- **Development**: Hot reload with tsx and Vite integration for development mode

## Data Layer
- **Database**: PostgreSQL with Neon serverless database
- **Schema Management**: Drizzle ORM with migrations in `./migrations` directory
- **Validation**: Zod schemas for runtime type checking and validation
- **Shared Types**: Common schema definitions in `./shared/schema.ts` for type safety across client and server

## Build and Development
- **Monorepo Structure**: Client, server, and shared code in separate directories
- **Build Process**: Vite for frontend bundling, esbuild for server bundling
- **Development Server**: Concurrent client and server development with Vite middleware
- **TypeScript Configuration**: Unified tsconfig with path mapping for clean imports

## Authentication and Security
- **Session Management**: Express sessions with PostgreSQL storage
- **Type Safety**: Full TypeScript coverage with strict configuration
- **CORS**: Configured for cross-origin requests in development

## Deployment Strategy
- **Production Build**: Static frontend assets served from Express server
- **Environment Configuration**: Environment variables for database connections
- **Asset Handling**: Static file serving with proper caching headers

# External Dependencies

## Core Framework Dependencies
- **@neondatabase/serverless**: Neon PostgreSQL serverless database connection
- **drizzle-orm & drizzle-kit**: Modern TypeScript ORM for PostgreSQL
- **@tanstack/react-query**: Server state management and caching
- **wouter**: Lightweight React router alternative

## UI and Styling
- **@radix-ui/react-***: Comprehensive set of unstyled, accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Type-safe variant API for component styling
- **lucide-react**: Icon library for React applications

## Development Tools
- **vite**: Fast build tool and development server
- **typescript**: Static type checking
- **tsx**: TypeScript execution engine for development
- **@replit/vite-plugin-***: Replit-specific development enhancements

## Form and Validation
- **react-hook-form**: Performant forms with minimal re-renders
- **zod**: TypeScript-first schema validation
- **@hookform/resolvers**: React Hook Form resolvers for Zod integration

## Additional Utilities
- **date-fns**: Modern JavaScript date utility library
- **clsx & tailwind-merge**: Conditional CSS class name utilities
- **nanoid**: URL-safe unique string ID generator