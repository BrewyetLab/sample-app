# Sample App

## Purpose

This repository is the reference application used to validate the home-server development and deployment workflow.

## Development

- Development occurs on dev01.
- Test changes locally before committing.
- The application runs with Docker Compose.
- Do not expose unnecessary host ports.
- Applications intended for the shared web tier should use the external Docker network named `proxy`.

## Deployment

Production runs on app01.

Deployment flow:

dev01 -> GitHub -> GitHub Actions -> app01 -> Docker Compose -> Caddy

A push or merge to the main branch triggers the production deployment workflow.

Do not manually copy application code to app01.

## Production Files

Production path:

/opt/apps/production/sample-app

Do not commit production `.env` files or other secrets.

## Documentation

If this application's architecture, dependencies, ports, deployment method, or infrastructure requirements change, update the corresponding documentation in Obsidian.
