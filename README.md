# GitRelease CLI

A zero-dependency, functionally pure CLI for enterprise release management.

## Features

- Semantic versioning control with automatic version determination
- Immutable release snapshots with full provenance
- Workflow enforcement with stage gates
- Conventional commits analysis and enforcement
- Automated verification and validation

## Installation

```bash
npm install -g gitrelease-cli
```

## Usage
See gitrelease help for full command documentation.

Usage: gitrelease [command] [options]

# GitRelease CLI

## Commands

| Command                 | Description |
|-------------------------|-------------|
| `init`                 | Initialize repository configuration |
| `config <path> <value>` | Set configuration value |
| `show-config`          | Display current configuration |
| `prepare [version]`    | Prepare a new release |
| `finalize`             | Finalize the current release |
| `next-version`         | Suggest next version based on commits |
| `list`                 | List all releases |
| `notes <version>`      | Show release notes for a version |
| `branch <type> <name>` | Create a branch with naming conventions |
| `verify`               | Verify repository status for release |
| `rollback [tag]`       | Rollback to a previous release |
| `hotfix <tag>`         | Create a hotfix for a previous release |
| `help`                 | Show this help message |

## Examples

```sh
gitrelease init
gitrelease config versioning.pattern calver
gitrelease prepare 1.2.0
gitrelease finalize
gitrelease branch feature user-authentication
