# bradfordwagner.ansible-role-go-releaser-install

This is a generic installer role for Go Releaser-built binaries. It has no version of its own — the version is supplied by the calling playbook via the `app.tag` variable.

## Required variables

| Variable | Description |
|----------|-------------|
| `app.repo` | GitHub repo (e.g. `owner/repo`) |
| `app.tag` | Release tag to install (e.g. `v1.2.3`) |
| `app.binary_name` | Name of the installed binary |

Check the upstream repo's releases page for the tag to pass in.

## Renovate

Renovate (`bradfordwagner/renovate`, preset `ansible-role`) opens PRs for the version pins marked `# renovate:`, `meta/requirements.yml`, `config.yaml`'s `upstream.tag` and GitHub Actions. A merged PR labeled `release` is tagged with the next patch version and published to Galaxy by `.github/workflows/release.yml`.
