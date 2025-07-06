# GreLea - English Learning Application

## Overview

GreLea (Green Learning) is a comprehensive English vocabulary, grammar, and pronunciation learning application designed to work both online and offline. The app features a modern React frontend with Node.js/Express backend, PostgreSQL database with Drizzle ORM, and is built with TypeScript for type safety.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management
- **UI Components**: Radix UI primitives with shadcn/ui design system
- **Styling**: Tailwind CSS with custom green theme (#4CAF50 primary color)
- **Animations**: Framer Motion for smooth transitions and intro animations
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful API endpoints under `/api` prefix
- **Request Handling**: JSON and URL-encoded body parsing
- **Development**: Hot module replacement with Vite integration

### Database Architecture
- **Database**: PostgreSQL (configured for Neon serverless)
- **ORM**: Drizzle ORM with type-safe schema definitions
- **Schema Management**: Drizzle Kit for migrations and schema synchronization
- **Connection**: Environment-based DATABASE_URL configuration

## Key Components

### Data Models
1. **Words Table**: Stores vocabulary with pronunciation, definitions, examples, related words, and favorite status
2. **Grammar Topics Table**: Contains grammar rules, structures, examples, and usage tips
3. **Offline Packages Table**: Manages downloadable content packages for offline use
4. **User Progress Table**: Tracks learning statistics and progress

### Frontend Modules
1. **Vocabulary Tab**: Word lookup with comprehensive definitions and examples
2. **Grammar Tab**: Grammar topic browsing and search functionality
3. **Pronunciation Tab**: IPA pronunciation display with text-to-speech integration
4. **Offline Tab**: Package management for offline content access
5. **Intro Animation**: Brand animation sequence showing "GreLea" expanding to "Green Learning"

### Backend Services
1. **Dictionary API**: Word search and definition retrieval
2. **Grammar API**: Grammar topic management and search
3. **Offline Package API**: Content package management
4. **Storage Layer**: Abstracted data access with in-memory fallback

## Data Flow

1. **Client Requests**: Frontend makes API calls using TanStack Query
2. **API Routing**: Express routes handle requests under `/api` prefix
3. **Data Processing**: Storage layer abstracts database operations
4. **Response Formatting**: JSON responses with consistent error handling
5. **Client Updates**: React Query manages caching and UI updates
6. **Offline Support**: Service worker capabilities for offline functionality

## External Dependencies

### Core Framework Dependencies
- React ecosystem (React, React DOM, React Query)
- Express.js with TypeScript support
- Drizzle ORM with PostgreSQL adapter
- Neon Database serverless PostgreSQL

### UI and Styling
- Radix UI component primitives
- Tailwind CSS for styling
- Framer Motion for animations
- Lucide React for consistent iconography

### Development Tools
- Vite for build tooling and development server
- TypeScript for type safety
- ESBuild for production bundling
- Replit-specific development enhancements

## Deployment Strategy

### Development Environment
- Vite development server with HMR
- Express server with middleware integration
- TypeScript compilation on-the-fly
- Replit-specific tooling integration

### Production Build
- Vite builds optimized frontend bundle to `dist/public`
- ESBuild bundles backend to `dist/index.js`
- Static file serving from Express
- Environment-based configuration

### Database Management
- Drizzle migrations stored in `./migrations`
- Schema definitions in shared TypeScript files
- Environment variable configuration for database connections

## User Preferences

Preferred communication style: Simple, everyday language.

## Recent Changes

- July 06, 2025: Major vocabulary expansion to 762+ words using automated generation system
- July 06, 2025: Integrated Free Dictionary API for real pronunciation data and audio playback
- July 06, 2025: Fixed Settings tab with working localStorage persistence for all settings
- July 06, 2025: Enhanced pronunciation with real API data, multiple accents, and audio controls
- July 06, 2025: Expanded grammar topics from 5 to 14 comprehensive topics covering all major English grammar areas
- July 06, 2025: Added categorized vocabulary (animals, colors, food, technology, etc.) with proper relationships

## Changelog

Changelog:
- July 06, 2025. Initial setup