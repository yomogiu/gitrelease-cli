# GitRelease CLI

gitrelease-cli is an independent tool and is not affiliated with the Git project or Software Freedom Conservancy.

It's a zero-dependency, functionally pure CLI for release management. 

## Features

- Semantic versioning control with automatic version setting
- Release snapshot record
- Workflow enforcement (confirms code follows dev -> test -> staging -> prod)
- Forced commit message patterns
- Automated verification and validation (checks for CI/CD pipeline passed, no uncommitted changes, etc.)
  - Right now the test is skipped for now but you can modify this for your own purpose
- SBOM generation based on package.json

## Installation

```bash
clone this repository
cd gitrelease-cli
npm link
gitrelease help
```

## Usage
See gitrelease help for full command documentation.

Usage: gitrelease [command] [options]

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
```

## TODO
Currently **gitrelease-cli** stores the configuration separately. So if you've made a change to the local repo, you'll have to run **gitrelease init** again to perform a manual refresh.
