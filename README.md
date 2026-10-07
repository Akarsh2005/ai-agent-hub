# AI Agent Hub 🤖

Central automated AI Dispatcher for engineering repositories.

## Overview
This repository serves as the central hub connecting Jira Cloud automation with GitHub. It receives dispatch events from Jira and dynamically:
1. Clones the requested target repository (`Akarsh2005/demo1`, etc.).
2. Creates a feature branch named after the Jira ticket (e.g. `feature/SCRUM-1-implement-...`).
3. Invokes an autonomous AI coding agent (**Gemini** or **Claude Code**).
4. Pushes changes and opens a Draft Pull Request in the target repository.
5. Jira native integration detects the PR and auto-transitions the ticket to `In Review`.

## Secrets Required
- `GEMINI_API_KEY`: API Key for Google Gemini 2.5 Pro.
- `ANTHROPIC_API_KEY`: API Key for Anthropic Claude Code CLI.
- `CENTRAL_HUB_PAT`: GitHub Fine-grained PAT with read/write access to target repos.
