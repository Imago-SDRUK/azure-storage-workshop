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

The design follows the same principles as Imago's other training material: avoid
jargon and minimise cognitive load for a mixed-ability audience.
