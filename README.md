# GalaxyCut AI — Releases

Public distribution channel for **GalaxyCut AI**: the Linux AppImage, a FUSE-free
installer, and the auto-update feed the app reads on startup.

**Download the latest version:** [releases/latest](../../releases/latest)

## Release history

Every version, in order, with what actually changed:
**[RELEASE-HISTORY.md](RELEASE-HISTORY.md)** — and the per-version notes
(copy/paste for each GitHub Release) in [release-notes/](release-notes/).

## What each release ships

| Asset | Purpose |
|---|---|
| `GalaxyCut-AI-<version>.AppImage` | the app, built with the **no-FUSE runtime**: it mounts when FUSE works and falls back to extraction when it does not |
| `GalaxyCut-AI-<version>-Linux-Instalador.sh` | universal installer — no FUSE, no `sudo`; needs only `bash`, `tar` and `gzip` |
| `GalaxyCut-AI-<version>.tar.gz` | the unpacked Linux build |
| `latest-linux.yml` | the auto-update feed the app polls at startup |

## Auto-update

The app checks for a new version on startup and offers the download; installation
happens only after the user accepts. The feed is:

```
https://github.com/lucasgabrieldevgg/galaxycut-ai-releases/releases/latest/download/latest-linux.yml
```

The source code lives in a private repository. This repository only carries the
public build artifacts and the release history.
