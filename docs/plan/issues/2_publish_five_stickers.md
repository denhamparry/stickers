---
status: Complete
issue: https://github.com/denhamparry/stickers/issues/2
---

# Publish five sticker entries

Issue snapshot: 2026-11-04. The owner expanded the scope to five designs and supplied artwork hashes and product URLs in [the issue comment](https://github.com/denhamparry/stickers/issues/2#issuecomment-6639034260). The user authorized using those URLs as placeholders before public approval.

## Approach

- Copy the four owner supplied PNGs unchanged as both `source.png` and `print.png`; use each print image for the preview. Preserve the existing I See BMCs source and print files.
- Add metadata and gallery entries for all five designs. Use the supplied URL for each design, clearly label the URLs as pending public verification, and retain target sizes and finishes until the owner confirms the actual offerings.
- Update README guidance so its placeholder state and later verification requirement are explicit.

Expected files: `README.md`, `CONTRIBUTING.md`, `docs/redbubble-sticker-image-requirements.md`, four new `stickers/<slug>/source.png`, `print.png`, and `metadata.yaml` groups, `stickers/i-see-bmcs/metadata.yaml`, and this plan. No runtime build or service prerequisite is needed. The repository check is `pre-commit run --all-files`.

## Acceptance and traceability

| Issue item | Disposition and timing | Owner, prerequisite, evidence and result |
| --- | --- | --- |
| Five store items | Validated from owner report, external | Owner reported five listings in the issue comment; public shop state pending verification. |
| Publish exact sticker products and verify artwork, purchase option, and URLs | External/operator pending | Owner publishes and verifies each public product page; automated 404 was reported on 2026-11-04. User approved provisional URL use, not public listing acceptance. |
| Confirm offered size and finish | External/operator pending | Owner checks each listing and supplies actual options; repository records targets until then. |
| Four new artwork directories and five `purchase_url` values | Implemented, pre-merge | Owner-file SHA-256 prefixes, metadata paths, and URLs matched the issue comment on 2026-11-04. |
| Five gallery previews and buy links; remove `Listing pending` | Implemented, pre-merge | All relative image paths and URL mappings passed local checks on 2026-11-04. |
| Published README preview and buy-link check | Post-merge pending | Owner or maintainer checks rendered GitHub README after merge and each public listing. |
| PR #1 dependency | Validated without change | PR #1 merged; I See BMCs files are present on `main`. |
| Maintenance #173 deferred tracking | Intentionally out of scope | Keep that external issue open for its remaining post-merge checks. |

## Validation and risk

The four owner-file SHA-256 prefixes and the existing I See BMCs print hash matched the issue comment. PNG dimensions, metadata fields, previews, and exact URL mappings passed local checks on 2026-11-04. Run `pre-commit run --all-files` after all files are staged and review the complete diff. Public URL, actual product options, and published README acceptance remain deferred; use `Refs #2` in the PR so the issue stays open. The weekly external link workflow may flag these provisional URLs until the pages become public.
