# 🌐 CELTEN Hub - Unified Command Center

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?logo=php)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![PWA](https://img.shields.io/badge/PWA-Enabled-5A0FC8?logo=pwa)

**The architect doesn't just write code; he builds ecosystems.**

[🚀 Demo](https://celten.net)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Architecture](#-architecture)
- [Ecosystem Services](#-ecosystem-services)
- [Key Features](#-key-features)
- [Tech Stack](#%EF%B8%8F-tech-stack)
- [Installation](#-installation)
- [Configuration](#%EF%B8%8F-configuration)
- [API Documentation](#-api-documentation)
- [Security](#-security)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 Overview

**CELTEN Hub** is a futuristic, microservices-based ecosystem designed for managing digital assets, documentation workflows, and gaming experiences through a unified Command Center. Built on Docker containerization, this platform enables PHP-based microservices to communicate via secure API protocols, creating a seamless, integrated digital environment.

### Why CELTEN Hub?

- 🔗 **Unified Experience**: Single sign-on across all services with synchronized sessions
- 🎮 **Gamified Economy**: XP and CELTEN Coin system connecting gaming achievements to real benefits
- 📱 **Progressive Web App**: Browser-independent, full-screen application experience
- 🔐 **Enterprise Security**: XSS/CSRF protection, flood control, and advanced session management
- 🚀 **Modular Architecture**: Add new services (Web3, AI tools) in seconds

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────────────────┐
│                  CELTEN Command Center                  │
│         (Main Hub - Global State Manager)               │
└─────────────────┬───────────────────────────────────────┘
                  │
        ┌─────────┼─────────┬─────────────┐
        │         │         │             │
   ┌────▼───┐ ┌──▼────┐ ┌──▼──────┐ ┌───▼─────┐
   │CelNote │ │ Neon  │ │CelStore │ │Architect│
   │  Docs  │ │Arcade │ │  Shop   │ │Portfolio│
   └────┬───┘ └──┬────┘ └──┬──────┘ └───┬─────┘
        │        │         │             │
        └────────┴─────────┴─────────────┘
                     │
            ┌────────▼─────────┐
            │  Global Services │
            │  • Notifications │
            │  • Economy       │
            │  • Auth Sync     │
            └──────────────────┘
```

### Service Communication Flow

```
User Action → Service API → Hub Gateway → Global State Update → 
→ Broadcast Notification → All Services Sync → User Feedback
```

---

## 🎪 Ecosystem Services

### 1. 🎯 CELTEN Command Center (Main Hub)
**Subdomain**: `hub.celten.net`

The nerve center of the entire ecosystem.

**Features**:
- 📊 Real-time system status monitoring
- 🔔 Global notification management
- 👥 User permission and role management
- 🎨 Unified dashboard with glassmorphism UI
- 📈 Analytics and usage statistics

**Tech**: PHP 8.x, SQLite, Real-time WebSocket notifications

---

### 2. 📝 CelNote (Cloud Docs)
**Subdomain**: `note.celten.net`

Advanced cloud documentation tool with markdown support.

**Features**:
- ✍️ Rich markdown editor with live preview
- 📁 Folder organization and tagging
- 💾 User-based storage quota management
- 🔍 Full-text search across all documents
- 🔗 Share links with permission control
- 📱 Mobile-optimized PWA interface

**Storage Tiers**:
- Free: 50MB
- Silver: 500MB (100 CELTEN Coins)
- Gold: 2GB (250 CELTEN Coins)
- Platinum: Unlimited (500 CELTEN Coins)

---

### 3. 🎮 Neon Arcade (Fun Ecosystem)
**Subdomain**: `fun.celten.net`

Retro-futuristic gaming platform with integrated progression system.

**Features**:
- 🕹️ SQLite-based real-time score tracking
- 🏆 Global leaderboards with rank decay system
- ⭐ XP and ranking system (Bronze → Diamond)
- 🎯 Achievement badges and milestones
- 🔔 Hub-integrated world record notifications
- 💰 Earn CELTEN Coins through gameplay

**Games**:
- **Snake Classic**: Nostalgic gameplay with modern scoring
- **2048 Fusion**: Number puzzle with combo multipliers
- **Space Invaders**: Defend Earth, climb ranks
- _More games coming soon..._

**Ranking System**:
```
Bronze   →  0-999 XP
Silver   →  1000-2499 XP
Gold     →  2500-4999 XP
Platinum →  5000-9999 XP
Diamond  →  10000+ XP
```

---

### 4. 🛒 CelStore (Digital Marketplace)
**Subdomain**: `store.celten.net`

Digital asset marketplace with integrated economy.

**Features**:
- 💎 Digital asset listings (themes, tools, services)
- 💰 CELTEN Coin payment system
- 📦 Automatic inventory delivery
- 🎁 Gift system for digital goods
- 📊 Sales analytics and revenue tracking
- 🏷️ Dynamic pricing and discount system

**Economy Integration**:
- Earn coins through gaming achievements
- Spend coins on storage upgrades
- Trade coins for marketplace items
- Architect's exclusive items

---

### 5. 👨‍💻 Architect Identity
**Domain**: `celten.info`

Personal portfolio and blog integration for the ecosystem's architect.

**Features**:
- 📰 Technical blog with code snippets
- 💼 Portfolio showcase
- 🎓 Tutorial and guide repository
- 🔗 Social media integration
- 📧 Direct contact system

---

## ✨ Key Features

### 🔗 Global Notification Bridge

Real-time event propagation across all services:

```php
// Example: World record notification
Hub::broadcast([
    'type' => 'achievement',
    'service' => 'Neon Arcade',
    'message' => 'New world record in Snake!',
    'user' => 'Player123',
    'score' => 9999
]);
```

### 💰 Unified Economy Gateway

Cross-service coin and XP exchange:

- **Gaming → Storage**: Convert XP to storage quota
- **Store → Services**: Purchase premium features
- **Achievements → Discounts**: Unlock marketplace deals
- **Community → Rewards**: Referral bonus system

### 🔒 Protocol Synchronization

Single action, ecosystem-wide effect:

- Password change → All services logout
- Profile update → Instant sync across platforms
- Permission revoke → Immediate access restriction
- Session expiry → Universal logout

### 🎨 Cyberpunk Aesthetic

Consistent visual identity with:

- Glassmorphism UI components
- Neon accent colors (#00ff00, #00ffff, #ff00ff)
- Smooth animations and transitions
- Dark mode optimized
- Responsive grid layouts

---

## 🛠️ Tech Stack

### Backend
- **Language**: PHP 8.x
- **Database**: SQLite 3.x (PDO)
- **Containerization**: Docker & Docker Compose
- **API**: RESTful architecture with JSON responses
- **Session**: Secure cookie-based with CSRF tokens

### Frontend
- **Styling**: Custom CSS3 (Glassmorphism, Flexbox, Grid)
- **Icons**: Lucide Icons (via CDN)
- **JavaScript**: Vanilla ES6+ (no frameworks)
- **PWA**: Service Worker for offline capability
- **Responsive**: Mobile-first design approach

### DevOps
- **Version Control**: Git
- **CI/CD**: GitHub Actions (planned)
- **Monitoring**: Built-in health checks
- **Logging**: Structured JSON logs

### Security
- **XSS Protection**: Input sanitization with `htmlspecialchars()`
- **CSRF Protection**: Token-based validation
- **SQL Injection**: PDO prepared statements
- **Flood Control**: Rate limiting on API endpoints
- **File Protection**: `.htaccess` rules for data directory
- **Session Security**: HTTP-only, Secure, SameSite cookies

---

## 🚀 Installation

### Prerequisites

- Docker 20.x or higher
- Docker Compose 2.x or higher
- Git
- Port 80/443 available (or configure alternative ports)

### Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/Celtenn/celten-hub.git
cd celten-hub

# 2. Copy environment configuration
cp .env.example .env

# 3. Configure your domain settings (edit .env)
nano .env

# 4. Start Docker containers
docker-compose up -d

# 5. Set database permissions
chmod 777 data/
chmod 666 data/*.db

# 6. Initialize databases
docker exec -it celten_hub php init/setup.php

# 7. Verify installation
curl http://localhost
```

### Manual Installation (Without Docker)

```bash
# 1. Clone repository
git clone https://github.com/Celtenn/celten-hub.git
cd celten-hub

# 2. Install PHP dependencies (if using Composer)
composer install

# 3. Configure web server (Apache/Nginx)
# Point document root to /public directory

# 4. Set permissions
chmod 777 data/
chmod 666 data/*.db

# 5. Initialize databases
php init/setup.php

# 6. Configure virtual hosts for subdomains
# See docs/apache-config.md or docs/nginx-config.md
```

---

## ⚙️ Configuration

### Environment Variables (`.env`)

```env
# Application
APP_NAME="CELTEN Hub"
APP_ENV=production
APP_DEBUG=false

# Domains
DOMAIN_HUB=hub.celten.net
DOMAIN_NOTE=note.celten.net
DOMAIN_FUN=fun.celten.net
DOMAIN_STORE=store.celten.net

# Database
DB_CONNECTION=sqlite
DB_DATABASE=./data/celten_hub.db

# Security
SESSION_LIFETIME=7200
CSRF_TOKEN_NAME=celten_token
FLOOD_THRESHOLD=100

# Economy
COIN_STARTING_BALANCE=100
XP_TO_COIN_RATIO=0.1

# API
API_RATE_LIMIT=1000
API_KEY_LENGTH=32
```

### Service Configuration

Each service has its own `config.php`:

```php
// services/note/config.php
return [
    'storage_quotas' => [
        'free' => 50 * 1024 * 1024,      // 50MB
        'silver' => 500 * 1024 * 1024,   // 500MB
        'gold' => 2 * 1024 * 1024 * 1024 // 2GB
    ],
    'allowed_extensions' => ['md', 'txt', 'json'],
    'max_file_size' => 10 * 1024 * 1024 // 10MB
];
```

---

## 📡 API Documentation

### Authentication

All API requests require authentication via session cookie or API key.

```bash
# Login
curl -X POST https://hub.celten.net/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{"username":"user","password":"pass"}'

# Response
{
  "success": true,
  "token": "abc123...",
  "user": {
    "id": 1,
    "username": "user",
    "rank": "Gold",
    "coins": 250
  }
}
```

### Hub API Endpoints

#### Get System Status
```bash
GET /api/status
```

**Response**:
```json
{
  "status": "operational",
  "services": {
    "note": "online",
    "fun": "online",
    "store": "online"
  },
  "users_online": 42,
  "uptime": 86400
}
```

#### Send Global Notification
```bash
POST /api/notifications/broadcast
Content-Type: application/json
Authorization: Bearer {token}

{
  "type": "info",
  "title": "System Update",
  "message": "New features available!",
  "target": "all"
}
```

### CelNote API Endpoints

#### Create Document
```bash
POST /api/docs/create
Content-Type: application/json

{
  "title": "My Document",
  "content": "# Hello World\n\nThis is markdown!",
  "folder": "personal"
}
```

### Neon Arcade API Endpoints

#### Submit Score
```bash
POST /api/games/submit-score
Content-Type: application/json

{
  "game": "snake",
  "score": 1337,
  "metadata": {
    "level": 15,
    "time": 245
  }
}
```

**Full API documentation**: [docs/API.md](docs/API.md)

---

## 🛡 Security

### Security Measures

1. **Input Validation**: All user inputs sanitized and validated
2. **Prepared Statements**: SQLite queries use PDO with parameter binding
3. **CSRF Protection**: Token validation on all state-changing requests
4. **Rate Limiting**: Flood protection on authentication and API endpoints
5. **Session Security**: Secure, HTTP-only cookies with SameSite policy
6. **File Upload**: Whitelist-based extension checking and MIME validation
7. **Error Handling**: No sensitive information in error messages

### Reporting Security Issues

Please report security vulnerabilities to: **security@celten.info**

Do not open public issues for security concerns.

---

## 🗺 Roadmap

### Phase 1: Foundation (✅ Complete)
- [x] Core hub architecture
- [x] User authentication system
- [x] Basic service integration
- [x] Docker containerization

### Phase 2: Enhancement (🚧 In Progress)
- [x] Global notification system
- [x] CELTEN Coin economy
- [ ] Advanced analytics dashboard
- [ ] Mobile app (React Native)
- [ ] API documentation portal

### Phase 3: Expansion (📋 Planned)
- [ ] Web3 wallet integration
- [ ] NFT marketplace module
- [ ] AI-powered document assistant
- [ ] Real-time collaboration tools
- [ ] Third-party OAuth (Google, GitHub)
- [ ] Internationalization (i18n)

### Phase 4: Scale (🔮 Future)
- [ ] Kubernetes orchestration
- [ ] Multi-region deployment
- [ ] GraphQL API layer
- [ ] Microservices mesh
- [ ] Machine learning insights

---

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

### Development Setup

```bash
# Fork and clone
git clone https://github.com/yourusername/celten-hub.git
cd celten-hub

# Create feature branch
git checkout -b feature/amazing-feature

# Make changes and test
docker-compose up -d
# ... develop ...

# Commit with conventional commits
git commit -m "feat: add amazing feature"

# Push and create PR
git push origin feature/amazing-feature
```

### Commit Convention

We use [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code style changes (formatting)
- `refactor:` Code refactoring
- `test:` Adding tests
- `chore:` Maintenance tasks

### Code Style

- **PHP**: PSR-12 coding standard
- **JavaScript**: ESLint with Airbnb config
- **CSS**: BEM methodology

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Celten

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 📞 Contact

**Enes Celten** - Ecosystem Architect

- 🌐 Website: [celten.net](https://celten.net)
- 📧 Email: enescelten@gmail.com
- 🐙 GitHub: [@Celtenn](https://github.com/Celtenn)
- 💼 LinkedIn: [linkedin.com/in/celten](https://www.linkedin.com/in/enes-kahraman-99230336b/)
- 📸 Instagram: [@celten_dev](https://www.instagram.com/celten_dev)

---

## 🙏 Acknowledgments

- [Docker](https://www.docker.com/) - Containerization platform
- [Lucide Icons](https://lucide.dev/) - Beautiful icon set
- [SQLite](https://www.sqlite.org/) - Lightweight database
- [PHP](https://www.php.net/) - Server-side scripting

---

<div align="center">

**Built with ❤️ by Celten**

⭐ Star this repo if you find it useful!

[🔝 Back to Top](#-celten-hub---unified-command-center)

</div>
