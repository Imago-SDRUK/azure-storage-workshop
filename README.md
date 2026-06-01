[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18771673.svg)](https://doi.org/10.5281/zenodo.18771673)
# Azure Storage Workshop — Imago Team

This repository contains the materials for a short, hands-on workshop teaching the
Imago team how to access our **Azure Cloud storage**. It's designed for a **mixed
audience** — you do not need to be a developer to follow along — and is delivered
live in roughly **one hour** during an Imago Tuesday meeting, then kept as
self-serve reference docs.

Attendees are given **read-only** access, so there is nothing in the storage they
can break, change, or delete.

## What's covered

The site is built as a Quarto book with two parallel **tracks** — attendees pick
whichever suits them:

- **Track A — Azure Storage Explorer:** a GUI walkthrough for non-technical users —
  installing the app, connecting with the access we provide, browsing containers,
  and downloading files.
- **Track B — Python:** for developers — using the `azure-storage-blob` SDK to
  authenticate, list contents, and download blobs, with runnable code.

A shared **Prerequisites & access** page covers what we hand out and what
read-only means, and a **Troubleshooting** page covers common errors and where to
get help.

> **Terminology note:** Azure calls things *storage account → container → blob*.
> If you know the AWS/GCS words, that maps to *account → bucket → object*. The
> material uses the Azure terms throughout.

The design follows the same principles as Imago's other training material: avoid
jargon and minimise cognitive load for a mixed-ability audience.

## Placeholders

Anything specific to our real storage — the storage account name, container
names, the SAS URL, example file names, and support contacts — is left as a
clearly-marked `PLACEHOLDER-...` value. Fill these in (or hand out the real values
on the day) before delivering the workshop. The chosen auth method is a
**read-only SAS URL** (a container URL with a SAS token on the end); Azure AD and
connection-string alternatives are noted in the material but not used.

## Build & preview

The site is built with [Quarto](https://quarto.org/). With Quarto installed:

```bash
# live preview with auto-reload (opens in your browser)
quarto preview

# one-off render to the docs/ output directory
quarto render
```

The rendered HTML is written to `docs/` (configured in `_quarto.yml`).

## Publishing

Publishing is automated: the GitHub Actions workflow in
`.github/workflows/build_quarto.yml` renders the site and publishes it to GitHub
Pages (the `gh-pages` branch) on every push to `main`.

## Repository layout

```
index.qmd            landing page / overview
prerequisites.qmd    shared "Prerequisites & access"
track-a/             Track A — Azure Storage Explorer (index + 3 steps)
track-b/             Track B — Python (index + 3 steps)
troubleshooting.qmd  troubleshooting & where to get help
_quarto.yml          site config, navigation, theme
styles.css           custom styles
assets/              images (logo, screenshots)
```
