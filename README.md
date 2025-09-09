<div align="center">
  <a href="https://taskfile.dev">
    <img src="./res/task.png"  width="200px" height="200px" />
  </a>
  <a href="https://github.com/features/actions">
    <img src="./res/actions.png" width="200px" height="200px" />
  </a>

  <h1>Task GitHub Action</h1>

  <p>
    A <a href="https://docs.github.com/en/actions">GitHub Actions</a> action that makes the <a href="https://taskfile.dev">Task</a> task runner / build tool available to use in your workflow.
  </p>

  <p>
    <a href="https://taskfile.dev/installation/">Installation</a> | <a href="https://taskfile.dev/usage/">Documentation</a> | <a href="https://twitter.com/taskfiledev">Twitter</a> | <a href="https://bsky.app/profile/taskfile.dev">Bluesky</a> | <a href="https://fosstodon.org/@task">Mastodon</a> | <a href="https://discord.gg/6TY36E39UK">Discord</a>
  </p>
</div>

[![Test TypeScript status](https://github.com/go-task/action/actions/workflows/test-typescript-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/test-typescript-task.yml)
[![Check TypeScript status](https://github.com/go-task/action/actions/workflows/check-typescript-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/check-typescript-task.yml)
[![Check TypeScript Configuration status](https://github.com/go-task/action/actions/workflows/check-tsconfig-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/check-tsconfig-task.yml)
[![Check npm status](https://github.com/go-task/action/actions/workflows/check-npm-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/check-npm-task.yml)
[![Integration Tests status](https://github.com/go-task/action/actions/workflows/test-integration.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/test-integration.yml)
[![Check Action Metadata status](https://github.com/go-task/action/actions/workflows/check-action-metadata-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/check-action-metadata-task.yml)
[![Check Prettier Formatting status](https://github.com/go-task/action/actions/workflows/check-prettier-formatting-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/check-prettier-formatting-task.yml)
[![Check Markdown status](https://github.com/go-task/action/actions/workflows/check-markdown-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/check-markdown-task.yml)
[![Spell Check status](https://github.com/go-task/action/actions/workflows/spell-check-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/spell-check-task.yml)
[![Check License status](https://github.com/go-task/action/actions/workflows/check-license.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/check-license.yml)
[![Check npm Dependencies status](https://github.com/go-task/action/actions/workflows/check-npm-dependencies-task.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/check-npm-dependencies-task.yml)
[![Sync Labels status](https://github.com/go-task/action/actions/workflows/sync-labels-npm.yml/badge.svg)](https://github.com/go-task/action/actions/workflows/sync-labels-npm.yml)

## Inputs

### `version`

The version of [Task](https://taskfile.dev) to install.
Can be an exact version (e.g., `3.4.2`) or a version range (e.g., `3.x`).

**Default**: `3.x`

### `repo-token`

[GitHub access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token) used for GitHub API requests.

**Default**: [`GITHUB_TOKEN`](https://docs.github.com/actions/security-guides/automatic-token-authentication)

## Usage

To get the action's default version of Task just add this step:

```yaml
- name: Install Task
  uses: go-task/action@v1
```

If you want to pin a major or minor version you can use the `.x` wildcard:

```yaml
- name: Install Task
  uses: go-task/action@v1
  with:
    version: 2.x
```

To pin the exact version:

```yaml
- name: Install Task
  uses: go-task/action@v1
  with:
    version: 2.6.1
```
