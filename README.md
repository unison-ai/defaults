# Unison Defaults

Official default snippets included in every Unison user's base profile. These are referenced automatically during onboarding and kept up to date by the Unison daemon.

## Contents

| Snippet | Type | Description |
|---------|------|-------------|
| `rules/unison-agent.md` | Rule | Teaches AI agents how to create, edit, and delete Unison snippets during conversations |

## How it works

When a new user signs up, their repository manifest references snippets from this repo via the `source` field in `unison.yaml`. The Unison daemon syncs these snippets locally and auto-applies updates when new versions are pushed here.

Users don't need to take any action — updates are applied automatically in the background.

## Learn more

Visit [rununison.ai](https://rununison.ai) for documentation, guides, and to get started.
