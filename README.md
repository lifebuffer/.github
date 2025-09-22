# LifeBuffer

> **Flexible life tracking for professionals**
> Capture, organize, and recall your daily activities with minimal friction.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.0.0-orange.svg)](#)
[![Status](https://img.shields.io/badge/status-active-success.svg)](#)

## 🚀 What is LifeBuffer?

LifeBuffer is a comprehensive life tracking platform designed for busy professionals who need to capture, organize, and recall their daily activities without the overhead of complex productivity systems. Whether you're preparing for 1-on-1s, tracking project contributions, or simply wanting to remember what you accomplished, LifeBuffer adapts to your workflow.

### ✨ Key Features

- **🎤 Voice-First Capture** - Log activities instantly with AI-powered voice recognition
- **⏱️ Smart Time Tracking** - Built-in timer with automatic status updates and additive logging
- **🏷️ Flexible Contexts** - Organize activities your way with custom contexts and emoji icons
- **📱 Cross-Platform Sync** - Real-time synchronization across web, desktop, and mobile
- **📊 Professional Reporting** - Export data in multiple formats for meetings and reviews
- **🌙 Beautiful Dark Mode** - Custom-designed interface that's easy on the eyes

## 🏗️ Platform Architecture

LifeBuffer is built as a modern, scalable platform with multiple client applications:

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Web App       │    │   Desktop CLI   │    │   iOS App       │
│   React 19      │    │   Native Go     │    │   SwiftUI       │
│   TanStack      │    │   Cross-platform│    │   Offline-first │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 │
                    ┌─────────────────────┐
                    │    Backend API      │
                    │    Laravel 12       │
                    │    PostgreSQL       │
                    │    OAuth 2.0 + PKCE │
                    └─────────────────────┘
```

## 📦 Repository Structure

### Core Applications

- **[`/api`](./api/)** - Laravel 12 backend API with OAuth 2.0, PostgreSQL, and comprehensive testing
- **[`/webapp`](./webapp/)** - React 19 web application with TanStack Start and real-time sync
- **[`/landing`](./landing/)** - Marketing website built with React 19 and Tailwind CSS v4
- **[`/cli`](./cli/)** - Cross-platform CLI application built with Go (planned)
- **[`/ios`](./ios/)** - Native iOS app with SwiftUI and offline-first architecture (planned)

### Documentation

- **[`CLAUDE.md`](./CLAUDE.md)** - Development guidelines and architecture overview
- **[`iOS.md`](./iOS.md)** - Complete iOS app specification with UI mockups
- **[`VOICE_RECORDING.md`](./VOICE_RECORDING.md)** - Voice input implementation details
- **[`API_DOCUMENTATION.md`](./API_DOCUMENTATION.md)** - Complete API reference

## 🚀 Quick Start

### Backend Setup

```bash
cd api
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan db:seed
php artisan passport:install
composer dev  # Starts server + queue + logs + vite
```

### Web App Setup

```bash
cd webapp
pnpm install
cp .env.example .env
# Add your OAuth client ID to .env
pnpm dev
```

### Landing Page Setup

```bash
cd landing
pnpm install
pnpm dev
```

## 🎯 Target Users

### Individual Contributors
> "Never walk into a 1-on-1 empty-handed again"

Track your daily contributions, blockers, and achievements effortlessly.

### Knowledge Workers
> "Professional tracking without productivity overhead"

Capture work without interrupting your flow - voice input, smart categorization, instant sync.

### Consultants & Freelancers
> "Professional reporting for the self-directed"

Generate detailed reports for clients with flexible export options and time tracking.

### Project Managers
> "Track leadership impact beyond the tools"

Document strategic contributions, team interactions, and decision-making that don't fit in project management tools.

## 💡 Core Philosophy

**Friction-Free Capture** → **AI-Powered Organization** → **Professional Output**

Unlike complex productivity systems that become burdensome to maintain, LifeBuffer focuses on:

- **Minimal Input Friction** - Voice recording, quick forms, smart defaults
- **Intelligent Processing** - AI categorization, context detection, time estimation
- **Flexible Structure** - Adapt to your workflow, not vice versa
- **Professional Output** - Multiple export formats, meeting-ready reports

## 🛠️ Technology Stack

### Backend
- **Laravel 12** with PHP 8.2+
- **PostgreSQL** for production, SQLite for development
- **OAuth 2.0 + PKCE** for secure authentication
- **Laravel Passport** for API authentication
- **Pest** for testing with 100% coverage goals
- **Laravel Pail** for real-time development logs

### Web Applications
- **React 19** with TypeScript
- **TanStack Start** (webapp) and **Vite** (landing)
- **TanStack Store** for state management
- **Tailwind CSS v3/v4** with custom orange accent (`#FF893F`)
- **Shadcn/ui** component library
- **Web Audio API** for voice recording

### Mobile & Desktop
- **SwiftUI** for iOS with offline-first Core Data
- **Go** for cross-platform CLI with Cobra framework
- **OAuth 2.0 + PKCE** authentication across all platforms

### AI Integration
- **OpenAI Whisper** for speech-to-text
- **GPT-4o-mini** for content structuring and categorization
- Smart title extraction and notes generation

## 🌟 Key Features Deep Dive

### Voice Recording & AI Processing
- **60-second recordings** with real-time waveform visualization
- **Multiple audio formats** (WebM Opus, WAV, MP3, M4A, OGG)
- **Intelligent transcription** using OpenAI Whisper
- **Smart content extraction** with GPT-4o-mini for titles and notes
- **Comprehensive error handling** with manual fallback options

### Time Tracking & Activity Management
- **Built-in timer** with play/pause/complete functionality
- **Additive time logging** - adds to existing time instead of replacing
- **Automatic status updates** - sets activities to "in_progress" when timer starts
- **Keyboard shortcuts** - `T` for timer, `V` for voice, `C` for create

### Real-Time Sync & Offline Support
- **TanStack Store** for intelligent caching and real-time updates
- **Day-based cache system** for optimal performance
- **Background data fetching** for recent days
- **Optimistic updates** with server sync
- **Offline-first mobile** with conflict resolution

### Professional Reporting
- **Multiple export formats** - Markdown, CSV, formatted text
- **Flexible date ranges** and context filtering
- **Meeting-ready summaries** with time breakdowns
- **Context-based grouping** for project reports

## 🔐 Security & Privacy

- **OAuth 2.0 + PKCE** for secure authentication without client secrets
- **Laravel Policies** for user-scoped data access
- **Rate limiting** and input validation on all endpoints
- **Temporary audio storage** - recordings deleted after processing
- **Configurable server URLs** for self-hosted deployments

## 📱 Platform Roadmap

### ✅ Available Now
- **Web Application** - Full-featured React app with voice input and time tracking
- **Backend API** - Complete Laravel implementation with OAuth and testing
- **Marketing Site** - Beautiful landing page with Tailwind CSS v4

### 🚧 In Development
- **Desktop CLI** - Cross-platform Go application for terminal users
- **iOS Application** - Native SwiftUI app with offline-first architecture

### 🔮 Future Enhancements
- **Watch App** - Quick activity logging and timer controls
- **Advanced AI** - Context suggestions, pattern recognition, automated insights
- **Team Features** - Shared contexts, team reporting, collaborative workflows
- **Integrations** - Calendar sync, project management tools, communication platforms

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines in individual application directories.

### Development Setup
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Follow the setup instructions for the specific application you're working on
4. Run tests and ensure they pass
5. Submit a pull request with a clear description

### Code Standards
- **TypeScript/React** - Follow rules in `/rules/react.md`
- **Laravel/PHP** - Follow rules in `/rules/laravel.md`
- **Testing** - Maintain high test coverage with comprehensive test suites
- **Documentation** - Update relevant documentation with your changes

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Links

- **🌐 Production App**: [https://app.lifebuffer.com](https://app.lifebuffer.com)
- **🏠 Landing Page**: [https://lifebuffer.com](https://lifebuffer.com)
- **📚 API Documentation**: [API_DOCUMENTATION.md](./API_DOCUMENTATION.md)
- **📱 iOS Specification**: [iOS.md](./iOS.md)
- **🎤 Voice Recording Guide**: [VOICE_RECORDING.md](./VOICE_RECORDING.md)

---

**Built with ❤️ for professionals who value both productivity and simplicity.**

*LifeBuffer: Remember what you've accomplished.*
