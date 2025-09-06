# renovate-config

thinceller's shared Renovate config.

## Usage
Add a Renovate config in your repo (e.g. .github/renovate.json) that extends this preset:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>thinceller/renovate-config"]
}
```

This preset is based on blog.thinceller.net and includes:
- config:recommended + customManagers:biomeVersions
- Weekly schedule (every weekend)
- Default label: dependencies
- PR limits: prHourlyLimit=5, prConcurrentLimit=20
- minimumReleaseAge: major=7d, minor=3d, patch=2d
- Patch updates are automerged and labeled with "automerge: enabled"
- Package grouping for @opennextjs/* and textlint packages

## Notes
- Public repository: can be referenced from any repo using GitHub-hosted presets.
- If you need a different variant later, add another file (e.g. node-apps.json) and reference `github>thinceller/renovate-config:node-apps`.
