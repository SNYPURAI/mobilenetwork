# replit.md

## Overview

Ghost Network is a decentralized mobile network platform that enables community-owned wireless infrastructure through blockchain technology. The application provides a comprehensive dashboard for managing mobile plans, eSIM profiles, hotspot deployment, and $GHOST token wallet operations. Built as a full-stack web application, it combines React frontend with Express.js backend, utilizing PostgreSQL for data persistence and Solana blockchain integration for token operations.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite for build tooling
- **UI Library**: Radix UI components with shadcn/ui design system
- **Styling**: Tailwind CSS with custom theming and dark mode support
- **State Management**: TanStack React Query for server state management
- **Routing**: Wouter for client-side routing
- **Component Structure**: Modular component architecture with separate sections for wallet, plans, hotspots, eSIM, and network statistics

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **API Design**: RESTful API endpoints for network stats, mobile plans, wallet management, user subscriptions, hotspots, and eSIM profiles
- **Development Setup**: Hot reload development server with Vite integration
- **Error Handling**: Centralized error middleware with status code management
- **Logging**: Request/response logging with duration tracking for API endpoints

### Data Storage Solutions
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Schema Design**: Relational tables for users, wallets, mobile plans, subscriptions, hotspots, and eSIM profiles
- **Database Abstraction**: Storage interface pattern allowing for multiple storage implementations
- **Migrations**: Drizzle Kit for database schema management and migrations

### Authentication and Authorization
- **User Management**: User accounts with username/password authentication
- **Wallet Integration**: Solana wallet address linking for blockchain operations
- **Session Management**: Cookie-based sessions with PostgreSQL session storage

### Business Logic Components
- **Mobile Network Management**: Plan selection, subscription management, and usage tracking
- **Hotspot Operations**: Indoor/outdoor hotspot deployment with earnings calculation
- **eSIM Profile Generation**: LPA:1 format activation codes with QR code generation
- **Token Economy**: $GHOST token balance tracking, staking rewards, and transaction handling

## External Dependencies

### Blockchain Integration
- **Solana Web3.js**: Primary blockchain interaction library for wallet operations and token transactions
- **Neon Database**: Serverless PostgreSQL database with @neondatabase/serverless driver

### UI and Development Tools
- **Radix UI**: Comprehensive component library for accessible UI primitives
- **QR Code Generation**: qrcode library for eSIM activation code visualization
- **TanStack React Query**: Server state synchronization and caching
- **Tailwind CSS**: Utility-first CSS framework with custom design tokens

### Development and Build Tools
- **Vite**: Frontend build tool with hot module replacement
- **TypeScript**: Type safety across frontend and backend
- **ESBuild**: Backend bundling for production deployment
- **Drizzle Kit**: Database schema management and migration tools

### Utility Libraries
- **Date-fns**: Date manipulation and formatting
- **Class Variance Authority**: Type-safe CSS class composition
- **Zod**: Runtime type validation and schema definition
- **UUID**: Unique identifier generation for database records