# ubuntubase2404

A base Docker image built on Ubuntu 24.04, pre-configured with common tools for CI/CD and development environments.

## What's Included

- **Ubuntu 24.04** base
- **Node.js 22** (via NodeSource)
- **Python 3** with pip and venv
- **.NET** runtime dependencies (libicu74, libssl3t64)
- Common tools: `curl`, `wget`, `git`, `jq`, `unzip`, `bash`, `openssh-client`, `iptables`, `gosu`, `iputils-ping`

## Docker Hub

Image: [`khdevnet/ubuntubase2404`](https://hub.docker.com/r/khdevnet/ubuntubase2404)

```
docker pull khdevnet/ubuntubase2404:latest
```

## Tags

| Tag | Description |
|-----|-------------|
| `latest` | Latest build from `main` branch |
| `main`, `dev` | Branch builds |
| `1.2.3` | Specific release version |
| `1.2` | Major.minor version |

## CI/CD

The image is automatically built and pushed to Docker Hub via GitHub Actions on:
- Push to `main` or `dev` branches
- Push of a version tag (`v*.*.*`)

## Usage

Use this image as a base in your own Dockerfile:

```dockerfile
FROM khdevnet/ubuntubase2404:latest

# Your customizations here
```

## Local Build

```bash
docker build -t ubuntubase2404 .
```
