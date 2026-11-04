---
status: Complete
---

# Issue #3: Remove template leftovers and duplicate artwork

**Issue:** [stickers #3](https://github.com/denhamparry/stickers/issues/3)
**Source snapshot:** 2026-11-04 UTC; no issue comments.

## Problem and approach

The Code of Conduct and flake retain template text, six inherited plans point
to `denhamparry/template`, and the I See BMCs source and print images have the
same bytes. Use the maintainer email already published in this repository's
Git history as the conduct contact. Remove the inherited plans. Keep the
original PNG as both source and print asset, with metadata and gallery paths
updated, because it already serves as the print image. Move the README image
brief below the file list and clarify that one file may serve multiple roles.

## Expected files

- `CODE_OF_CONDUCT.md`, `flake.nix`, `README.md`,
  `docs/redbubble-sticker-image-requirements.md`
- `stickers/i-see-bmcs/metadata.yaml`; remove its redundant `print.png`
- Remove the six `docs/plan/issues/` files whose issue links target
  `denhamparry/template`; keep the stickers issue #2 plan.
- This plan.

## Issue traceability and acceptance

| Issue item | Disposition | Timing, owner, prerequisite and evidence |
| --- | --- | --- |
| Real enforcement contact; no placeholder in conduct or flake | Implement in this PR | Pre-merge, Codex; `rg` returns no matches and contact matches published commit author email. |
| No plan links to `denhamparry/template` | Implement in this PR | Pre-merge, Codex; inspect all remaining plan issue links and `rg`. |
| No duplicate I See BMCs files; metadata paths exist | Implement in this PR | Pre-merge, Codex; file hashes and path checks. Preserve source bytes. |
| File list immediately follows its introduction | Implement in this PR | Pre-merge, Codex; inspect rendered README source. |
| Image brief references removed print PNG | Implement in this PR | Pre-merge, Codex; all local Markdown links resolve. Found by post-PR review and Links CI. |
| `pre-commit run --all-files` passes | Validate in this PR | Pre-merge, Codex; full hook run after all intended files are staged. |
| Suggested distinct print export or reuse source | Reuse source in this PR | The duplicate has no separate export value; metadata `print` and `preview` may name `source.png`. |
| Linked stickers #1 and maintenance #173 | Context only | No separate action requested here. |

## Validation and risk

Inspect README image paths, existing product links, and metadata references;
run targeted assertions and `pre-commit run --all-files`. No build, service,
generated artifact, or target VM command is involved. The existing product
listings remain provisional; do not claim public listing verification if the
storefront cannot be reached. The contact email is already public in commit
metadata, but publishing it in conduct text makes it easier to find.
