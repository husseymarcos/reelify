# Reelify

Reelify is an AI-powered platform that automatically generates and manages short-form video content for local businesses. We transform your existing photos and descriptions into platform-optimized TikToks and Reels, helping you grow your online presence without the hassle of content creation.

## Features

- **AI-Powered Video Generation** – Automatically create engaging short-form videos from your photos and descriptions
- **Platform Optimization** – Videos are optimized for TikTok, Instagram Reels, and other platforms
- **Local Business Focus** – Built specifically for local businesses to showcase their products and services
- **Content Management** – Schedule, manage, and track your video content in one place

## Requirements

- Ruby 3.2+
- SQLite3
- Node.js (for Tailwind CSS)
- FFmpeg (for video processing)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/reelify.git
cd reelify
```

2. Install dependencies:
```bash
bundle install
```

3. Setup the database:
```bash
rails db:create db:migrate
```

4. Install JavaScript dependencies:
```bash
bin/importmap
```

## Running the Application

Start the Rails server:
```bash
bin/rails server
```

Or use the dev script for full stack development:
```bash
bin/dev
```

Visit http://localhost:3000 to view the application.

## Database

### Database Creation
```bash
rails db:create
```

### Database Migrations
```bash
rails db:migrate
```

### Database Seeding
```bash
rails db:seed
```

### Reset Database
```bash
rails db:drop db:create db:migrate db:seed
```

## Running Tests

Run the full test suite:
```bash
rails test
```

Run system tests:
```bash
rails test:system
```

Run RuboCop for code style checks:
```bash
bundle exec rubocop
```

Run Brakeman for security analysis:
```bash
bundle exec brakeman
```

## Services

The application uses several background services:

- **Solid Queue** – Processes background jobs (video generation, uploads)
- **Solid Cache** – Provides database-backed caching
- **Solid Cable** – Handles WebSocket connections for real-time features

Start background workers:
```bash
bin/jobs
```

## Deployment

This application is configured for deployment with Kamal:

```bash
kamal setup
kamal deploy
```

See `config/deploy.yml` for deployment configuration.
