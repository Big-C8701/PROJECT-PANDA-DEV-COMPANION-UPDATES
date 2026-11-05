# Public Bible feed — no GitHub login required

The P.A.N.D.A. Developer Companion should obtain approved Bible catalogue releases anonymously over HTTPS. Do not embed GitHub personal access tokens, device-flow refresh tokens or private GitHub App credentials in the APK.

## Client contract

1. Fetch `https://raw.githubusercontent.com/Big-C8701/PROJECT-PANDA-DEV-COMPANION-UPDATES/main/bible/current.json` without an Authorization header.
2. Read `bible_version`, `catalogue_url`, `schema_url`, `catalogue_sha256`, and `catalogue_schema_version`. Reject unknown schemas, invalid HTTPS URLs and mismatched checksums.
3. Download the catalogue to a temporary file, validate JSON/schema and preserve the existing reference IDs, then atomically replace the local snapshot. Retain the last-known-good version if any step fails.
4. Show the current version and a clear error on failure. Do not request sign-in or a device code for public Bible updates.
5. Existing private tracking/authoring connections, if any, remain separate; no personal notes or credentials are published.

## Publisher contract

Publish only explicitly approved, non-sensitive Bible material. Upload the immutable versioned catalogue and schema under `bible/versions/vX.Y/`; validate hashes; update `bible/current.json` **last**, after the files are accessible. Never publish private journals, user data, secrets or internal implementation tracking.

## Status

This document is a **client migration specification**, not a claim that the currently installed v0.4.0 APK has been rebuilt. v0.4.0 uses a private Bible connection and requires a client update to read this public feed.
