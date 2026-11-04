---
status: Complete
issue: https://github.com/denhamparry/stickers/issues/5
---

# Align provisional buy-link rules

Issue snapshot: 2026-11-04T19:27Z; no comments. PR #4 and issue #2 record the owner's approval for five provisional product URLs while public verification remains pending.

## Approach

- Add the owner-approved provisional exception to `CLAUDE.md`, requiring a pending-verification gallery label and later verification against the exact published sticker.
- Temporarily ignore only the five owner-supplied Redbubble product IDs in `.lycheeignore`, with an issue #2 removal note. Other product links remain subject to the weekly check.
- No application build, service, generated artifact, or target-side command is involved.

Expected files: `CLAUDE.md`, `.lycheeignore`, and this plan.

## Issue traceability and acceptance

| Issue item | Disposition | Timing, owner, prerequisite, evidence |
| --- | --- | --- |
| Agent rule agrees with README and CONTRIBUTING | Implement in this PR | Pre-merge, Codex; compare wording and require owner approval plus pending label. |
| Prevent known provisional 404s from generating the weekly issue | Implement in this PR | Pre-merge, Codex; match all five existing URLs and reject an unrelated product ID. Remove the ignore after issue #2 public-listing checks. |
| `pre-commit run --all-files` passes | Validate in this PR | Pre-merge, Codex; run after staging all intended files. |
| PR #4 and issue #2 context | Validate without change | PR #4 merged; issue #2 owns public listing, size, finish, and published README verification. |
| Alternative weekly-issue reminder | Not applicable | The scoped temporary ignore is the selected solution. |

## Validation and risk

Check the five README and metadata URL mappings, confirm the ignore pattern matches only those IDs, inspect the full diff, and run `pre-commit run --all-files`. The ignore must be removed when the listings are public; public product availability remains unverified under issue #2.
