# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Renovate configuration repository that provides a base configuration for dependency management. The main configuration is stored in `default.json` which extends Renovate's recommended configuration with custom settings for automated dependency updates.

## Architecture

- **Configuration File**: `default.json` - Contains the Renovate bot configuration
- **Schema**: Uses the official Renovate schema for validation
- **Base Configuration**: Extends `config:recommended` with additional presets for auto-merging and Docker major updates

## Key Configuration Details

The Renovate configuration includes:
- Timezone set to Europe/Warsaw
- Scheduled runs on Saturdays between 10:00-16:00 (hours 1-7 of the week)
- Auto-merge enabled for pull requests
- Docker major version updates enabled
- ArgoCD and Kubernetes YAML file pattern matching
- Rebase when conflicted
- No concurrent PR limit
- Automatic labeling with "renovate"

## Development Commands

Since this is a configuration repository, there are no build, test, or lint commands. Changes are typically made directly to the `default.json` file and validated against the Renovate schema.

## Repository Details

- **License**: MIT License (see `LICENSE`)
- **Owner**: Marcin Jasion (see `.github/CODEOWNERS`)
- **Git Ignore**: Configured for Go projects but contains general patterns

## File Structure

```
.
├── README.md              # Project documentation
├── default.json           # Main Renovate configuration
├── LICENSE               # MIT license
├── .github/CODEOWNERS    # Repository ownership
├── .gitignore           # Git ignore patterns (Go-based template)
└── CLAUDE.md            # This file
```