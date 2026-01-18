<div align="center">
  <img width="200" height=auto src=".github/logo.png" />
</div>

# repo-template

A template project.

# Configuration

## Containers

In `containers` folder:
- Create a new folder image. The name of the folder will be the name of the docker image.
- Add `PLATFORM` file to build image for a dedicated platform. Can add multiple platform separated by comma (i.g linux/amd64,linux/arm64)
- Add the new image in `.github/release-please-config.json` to get auto tag and changelog.

## Helm charts

In `helm` folder:
- Create a new folder image. The name of the folder will be the name of the helm chart.
- Add the new chart in `.github/release-please-config.json` to get auto tag and changelog.

## Pre-commit

Pre-requisite
```bash
python3 -m pip install pre-commit
# Detect-secrets
python3 -m pip install detect-secrets
secrets-secrets scan > .secrets.baseline
```

```bash
pre-commit install
```

## Enforcing conventional commit

This repo follows the angular [conventional commits](https://conventionalcommits.org/).
