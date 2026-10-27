# Reinyard

**A controlled place for agents to work.**

Reinyard is where a company builds, versions and runs agents and automations
without losing sight of what they did. The name is the idea: a _rein_ to guide
and restrain, and a _yard_ to work in.

## What it does

- **Agents are versioned like code.** Each agent's pipeline lives in Git, with
  commits, branches and merges, so every change has an author and a history.
- **Runs happen in isolation.** Pipelines execute in Docker Sandboxes
  (microVMs) that are removed afterwards. Only the outputs come back.
- **Every run leaves a record.** Logs, exit codes and generated files are kept
  and tied to the exact version that produced them.
- **Access is scoped per agent.** An agent can read only the Google Drive
  folders it has been granted, and nothing else.
- **Teams stay in control.** Sign-in is invite-only, work is organised in
  workspaces with roles, and administrators can see and manage every
  workspace.
- **Problems are visible.** An overview shows execution health and what needs
  attention next, from your real run history.

## How it is built

A Go backend with SQLite or Postgres, a small Go frontend server, and Docker
Sandboxes for execution. You can self-host it, and an optional managed cloud is
planned.

## Status

Reinyard is under active development. Self-hosting is the supported path
today, and a managed cloud is planned. It is not yet ready for public
multi-tenant hosting. See the repository documentation for the current
security model and limits.

## Links

- Website: [reinyard.com](https://reinyard.com)
- Security reports: [security@reinyard.com](mailto:security@reinyard.com)
