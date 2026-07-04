# Shiori 栞

One cross-platform media hub for watch and read, with a library and progress that outlive dead sources.

Personal project by [Shiori HQ](https://github.com/shiori-hq). Not on app stores. Invite-only development.

## What it is

Shiori combines video (movies, series, anime, cartoons) and reading (manga, comics) in one Flutter app, backed by a Go service. Your watchlists, bookmarks, and continue positions are yours: they persist across reinstalls, source changes, and devices.

This is a learning and personal-use project, not a commercial streaming platform.

## Pillars

- **Permanence** - library, watchlist, and progress stay intact when sources change or apps disappear
- **Resilience** - multiple sources per format with automatic failover when one is unreachable

## Stack

| Layer | Tech | Targets |
|-------|------|---------|
| Client | Flutter | Phone, tablet, desktop |
| Backend | Go | API, routing, sync |

## Architecture

```
┌─────────────────┐     HTTP/API      ┌──────────────────┐
│   shiori-app    │ ◄───────────────► │  shiori-backend  │
│   (Flutter)     │                   │      (Go)        │
└─────────────────┘                   └────────┬─────────┘
                                               │
                                    ┌──────────▼──────────┐
                                    │  Content providers  │
                                    │  (per format/type)  │
                                    └─────────────────────┘
```

## Repositories

| Repo | Visibility | Role |
|------|------------|------|
| [shiori](https://github.com/shiori-hq/shiori) | Public | Project overview (shareable link) |
| [shiori-app](https://github.com/shiori-hq/shiori-app) | Private | Flutter client |
| [shiori-backend](https://github.com/shiori-hq/shiori-backend) | Private | Go backend |

Source code and dev setup live in the private repos. Access is by invitation only.

## Status

Early development. Watch core and unified library in progress.

## License

All rights reserved. Personal project.
