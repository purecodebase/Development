# PureCodeBase Public Pages

## Purpose

This repository publishes the public PureCodeBase landing page, imprint,
support, privacy, terms, and app-specific legal pages through GitHub Pages.

## Source of truth

- `apps/manifest.yml` maps each publisher slug to its immutable public slug and
  URLs.
- Every app-specific package lives under `apps/<public-slug>/`.
- `app-ads.txt` is served from the site root and must contain only the approved
  advertising publisher records.

## Rules

- Keep app-specific privacy and support claims aligned with the shipped app.
- Do not claim that an app is offline-only when advertising or consent uses the
  network.
- Do not claim ATT is requested unless the released binary actually requests it.
- Preserve the shared controller identity and support address already published
  in the imprint.
- Validate links and pages locally before publishing.

## Current work

- App-specific public pages for Minimal Dungeon and Drillbound are maintained
  under `apps/<public-slug>/`.
- Drillbound uses `apps/drillbound/` with an app landing page, privacy policy,
  support page, and terms of service; it is registered in `apps/manifest.yml`.
- Otter Dive uses `apps/otter-dive/` with an app landing page, privacy policy,
  support page, and terms of service; it is registered in `apps/manifest.yml`.
- OddScene uses apps/oddscene/ with an app landing page, privacy policy,
  privacy choices, support page, and terms of service; it is registered in
  apps/manifest.yml. These pages describe the current offline MVP and must be
  updated before any StoreKit, advertising, consent, or analytics provider is
  enabled in a release.
- Publishing to GitHub Pages remains a separate external action.
