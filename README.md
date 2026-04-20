# Acme Auth Service

Acme Auth Service is the identity and session boundary for the Acme banking platform. It handles sign-in, token issuance, session validation, and account security flows for customer-facing applications.

## Overview

This service provides authentication and authorization capabilities for the rest of the Acme ecosystem. It is designed to support secure login, session renewal, multi-factor verification, and identity checks for both mobile and web clients.

## Responsibilities

- Authenticate users and issue access tokens
- Validate sessions and refresh credentials
- Support multi-factor and step-up authentication flows
- Enforce login and account security policies
- Publish auth events for audit and monitoring

## Suggested Stack

- Backend service in Java, Kotlin, or Node.js
- OAuth2 / OIDC-style token flows
- Secret management and secure key rotation
- Centralized logging and audit trails
- Container-based deployment with health checks

## Repository Layout

- `.github/workflows/` - CI and DevXP automation
- `src/` - service code
- `security/` - auth policies and references
- `tests/` - automated test coverage
- `docs/` - authentication and integration notes

## Local Development

Typical developer steps:

1. Configure local identity and token settings.
2. Start the service with a development profile.
3. Run auth-focused tests for token, session, and policy flows.
4. Verify integration points used by the web and mobile clients.

## Security Notes

Because this service sits on the critical path for customer access, credentials, signing keys, and environment-specific secrets must be handled through approved secret storage and never committed to the repository.

## Automation

This repository includes a DevXP analysis workflow that runs on pushes to `main` and publishes repository metrics for internal reporting.

## Contributors
@bertram-gilfoyle
@richard-hendricks