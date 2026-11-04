# Contributing stickers

Open a pull request for each new or changed sticker. Include:

- Artwork you own or have permission to publish under the licence recorded in `metadata.yaml`.
- The original source file and a print PNG or PDF in `stickers/<slug>/`.
- A `metadata.yaml` file following the schema in [README.md](README.md).
- A README gallery row with a preview and the exact published product URL, or “Listing pending” until the listing is live. If the owner explicitly approves a provisional URL, label it as pending verification in the gallery.

Check that image paths resolve and that the product page shows the intended design, size, and finish. Run `pre-commit run --all-files` before requesting review. Keep pull requests focused and use a conventional commit subject.
