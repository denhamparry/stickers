# Stickers repository

This public repository holds sticker source artwork, print exports, metadata, and a README gallery with product links. `AGENTS.md` links to this file for Codex CLI portability.

## Editing rules

- Keep each sticker in `stickers/<slug>/` and follow the schema in `README.md`.
- Preserve source artwork and add a separate print export and gallery preview when needed.
- Verify a product link opens the published listing for the exact sticker before adding it to the gallery. If the owner explicitly approves a provisional URL, label its gallery link as pending verification until the exact published listing can be checked.
- Respect the artwork licence in each sticker's metadata. The root MIT licence applies only to software and configuration.
- Keep files small enough for ordinary Git unless a real asset warrants Git LFS.
- Use a pull request for changes to `main`; rebase-only merging and the `pre-commit` check are required.

## Validation

Run `pre-commit run --all-files` for repository checks. Check README image paths and product links against their target pages. No application build or test suite is required for artwork and metadata updates.
