# Watchdog 🐾

<p align="center">
  <img src="build/appicon.png" alt="Watchdog 🐾 Logo" width="150" />
</p>

<h3 align="center">Modern Security Scanning Platform with AI-Powered Analysis</h3>

<p align="center">
  <strong>Secure. Scan. Analyze. Remediate.</strong>
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#screenshots">Screenshots</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#installation">Installation</a> •
  <a href="#development">Development</a> •
  <a href="#roadmap">Roadmap</a>
</p>

---

## Overview

Watchdog 🐾 is a powerful, modern GUI-based security scanner that provides comprehensive vulnerability detection, technology stack identification, and AI-powered security analysis for web applications. Built with a sleek, modern UI using Wails, React, and Tailwind CSS v4, it brings enterprise-level security scanning capabilities to the desktop.

## Features

### 🔍 Advanced Security Scanning
- **Comprehensive Vulnerability Detection**: Identifies security vulnerabilities with CVSS scoring
- **Technology Stack Identification**: Detects frameworks, languages, and libraries
- **SSL/TLS Analysis**: Analyzes certificates and protocols with security grading
- **DNS Information Gathering**: Collects DNS records and configuration data
- **Real-time Progress Tracking**: Monitor scans with live progress updates

### 🤖 AI-Powered Analysis
- **Multi-Provider AI Integration**:
  - OpenAI GPT support
  - Google Gemini support
  - Claude support (placeholder)
- **Automated Security Reports**: Generate detailed analysis of vulnerabilities
- **Remediation Recommendations**: AI-generated security improvement suggestions

### 📊 Modern Dashboard & UI
- **Clean, Modern Interface**: Glassmorphism design with subtle gradients
- **Responsive Design**: Works seamlessly across all screen sizes
- **Real-time Analytics**: Security scoring and vulnerability metrics
- **Scan History Management**: Browse, filter, and search past scans

### 📝 Comprehensive Reporting
- **Multiple Export Formats**: PDF and JSON export options
- **Customizable Reports**: Configure report content and branding
- **Shareable Results**: Easy export and sharing capabilities

## Tech Stack

### Backend
- **Go**: Core application logic
- **Wails v2**: Native desktop application framework
- **LevelDB**: Local storage for scan results and configuration
- **AI Integration**:
  - Google Generative AI SDK
  - OpenAI API
  - Claude API (placeholder)

### Frontend
- **React**: UI component framework
- **Tailwind CSS v4**: Modern styling with the latest features
- **React Router v6**: Navigation and routing
- **Framer Motion**: Smooth animations and transitions
- **Recharts**: Data visualization
- **Lucide Icons**: Clean, consistent iconography

## Screenshots

*[Screenshots would be placed here]*

## Architecture

Watchdog 🐾 follows a clean architecture pattern with clear separation of concerns:

### Backend Services

```
backend/
├── scanner/service.go   # Core scanning functionality
├── ai/service.go        # AI integration with multiple providers
├── config/manager.go    # Configuration and API key management
└── storage/manager.go   # Data persistence and report generation
```

### Frontend Structure

```
frontend/
├── src/
│   ├── pages/           # Main application screens
│   ├── components/      # Reusable UI components
│   ├── styles/          # Tailwind v4 styling
│   └── types/           # TypeScript definitions
└── wailsjs/            # Generated Wails bindings
```

### Key Components

1. **Scanner Service**: Handles all security scanning operations
2. **AI Service**: Manages AI provider integrations and report generation
3. **Storage Manager**: Handles data persistence and exports
4. **Configuration Manager**: Manages application settings and API keys

## Installation

### Prerequisites
- Go 1.19+
- Node.js 16+
- Wails v2.10.1+

### Build from Source

```bash
# Clone repository
git clone https://github.com/btwshivam/watchdog.git
cd watchdog

# Install dependencies
go mod download
cd frontend && npm install
cd ..

# Build application
wails build
```

Pre-built binaries for Windows, macOS, and Linux are available in the releases section.

## Development

### Setup Development Environment

```bash
# Install Wails if not already installed
go install github.com/wailsapp/wails/v2/cmd/wails@latest

# Start development server with hot reload
wails dev
```

### Directory Structure

```
watchdog/
├── app.go                # Main Wails application context
├── main.go               # Application entry point
├── backend/              # Backend Go services
├── frontend/             # React frontend
├── build/                # Build configuration and resources
└── cmd/                  # CLI tools and testing utilities
```

### Testing

The project includes comprehensive test suites:

```bash
# Run backend integration tests
cd cmd/test
go run main.go

# Run API integration tests
cd cmd/test-api
go run main.go
```

## Roadmap

### Near-term Improvements
- Real-time scan progress with WebSocket updates
- Advanced dashboard analytics and metrics
- Scan scheduling and automation
- Custom vulnerability rules and filters

### Future Enhancements
- Plugin system for custom security scanners
- Cloud integration for result storage
- Team collaboration features
- Mobile companion app for monitoring

## License

MIT

## Author

[Shivam](https://github.com/btwshivam)
