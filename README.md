# OpenClaw

**Multi-agent mobile messaging workspace for iOS**

OpenClaw is a production-ready React Native + Expo mobile application that combines real-time chat, channel management, and AI agent orchestration into a unified iOS experience.

## Overview

OpenClaw transforms how teams collaborate by integrating human conversation with AI-powered automation. Users can create channels, chat in real-time, and delegate tasks to specialized AI agents—all from a native iOS interface.

### Core Features

- **Real-time Messaging**: Instant chat with presence indicators and message history
- **Channel Management**: Create, organize, and manage conversation channels
- **AI Agent Orchestration**: Delegate tasks to specialized AI agents (GitHub, Supabase, QA automation)
- **Multi-agent Workflows**: Coordinate complex tasks across multiple agents
- **Mobile-First Design**: Native iOS experience with Human Interface Guidelines compliance

## Tech Stack

- **Frontend**: React Native 0.76+ with Expo SDK 52
- **Backend**: Supabase (PostgreSQL, PostgREST, Auth, Realtime)
- **State Management**: React Context + AsyncStorage
- **Navigation**: React Navigation 7.x (Stack + Bottom Tabs)
- **Testing**: Jest (unit), Detox (E2E), accessibility audits
- **CI/CD**: GitHub Actions with automated testing and build pipelines

## Architecture

### Frontend Structure
```
src/
├── screens/          # Channel list, chat, settings
├── components/       # Reusable UI components
├── navigation/       # React Navigation setup
├── services/         # API clients (Supabase, WebSocket)
├── context/          # Global state (auth, channels)
├── utils/            # Helpers and constants
└── types/            # TypeScript interfaces
```

### Backend (Supabase)
```
supabase/
├── migrations/       # Database schema
└── functions/        # Edge Functions
```

## Database Schema

- **users**: User profiles and authentication
- **channels**: Channel metadata and settings
- **messages**: Chat messages with sender and timestamps
- **agents**: AI agent configurations
- **tasks**: Delegated task tracking

## Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn
- Expo CLI (`npm install -g expo-cli`)
- iOS Simulator (Xcode) or physical iOS device
- Supabase account with project created

### Installation

```bash
# Clone the repository
git clone https://github.com/bouquet-garden/openclaw.git
cd openclaw

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your Supabase URL and anon key

# Start the development server
npx expo start
```

### Running on iOS

```bash
# iOS Simulator
npx expo run:ios

# Or press 'i' in the Expo terminal after 'expo start'
```

## Development Workflow

1. **Feature Development**: Create feature branches from `main`
2. **Testing**: Run unit tests (`npm test`) and E2E tests (`npm run test:e2e`)
3. **Accessibility**: Validate with `npm run test:a11y`
4. **Code Quality**: Lint with `npm run lint`
5. **CI/CD**: Push triggers automated GitHub Actions pipeline
6. **Build**: EAS Build for TestFlight distribution

## Testing

```bash
# Unit tests with Jest
npm test

# E2E tests with Detox
npm run test:e2e

# Accessibility audits
npm run test:a11y

# Test coverage
npm run test:coverage
```

## Deployment

- **Development Builds**: EAS Build preview channels
- **TestFlight**: Internal testing distribution
- **App Store**: Production releases

## Project Status

**Phase 1: MVP Foundation** (Current)
- [x] Technical specification
- [x] Architecture design
- [ ] Database schema implementation
- [ ] Authentication flow
- [ ] Channel and messaging UI
- [ ] AI agent integration
- [ ] Testing infrastructure

## Documentation

- [Project Specification](docs/project-openclaw-hardened-spec.md)
- [Execution Roadmap](docs/openclaw-execution-roadmap.md)
- [Build Strategy](docs/READY-TO-BUILD-SUMMARY.md)
- [MVP Tech Stack](docs/mvp-mobile-first-stack.md)

## Contributing

This is currently a private development project. Contribution guidelines will be added when the project enters public beta.

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Contact

Maintained by [@bouquet-garden](https://github.com/bouquet-garden)

---

**Built with ❤️ using React Native, Expo, and Supabase**