# Stickers

Source artwork, print exports, and purchase links for stickers by Lewis Denham-Parry.

## Gallery

These five owner-supplied product URLs are placeholders pending public listing
verification. Sizes and finishes below are targets pending owner confirmation.

| Preview | Sticker | Size | Finish | Licence | Buy |
| --- | --- | --- | --- | --- | --- |
| ![I See BMCs artwork](stickers/i-see-bmcs/print.png) | I See BMCs | 75 × 75 mm target | Glossy target | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Buy (pending verification)](https://www.redbubble.com/shop/ap/185333538) |
| ![I Debug on Slack artwork](stickers/debug-on-slack/print.png) | I Debug on Slack | 75 × 75 mm target | Glossy target | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Buy (pending verification)](https://www.redbubble.com/shop/ap/185334972) |
| ![Yes Queen artwork](stickers/yes-queen/print.png) | Yes Queen | 69 × 75 mm target | Glossy target | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Buy (pending verification)](https://www.redbubble.com/shop/ap/185334877) |
| ![I Now Wat I'm Doin artwork](stickers/i-now-wat-im-doin/print.png) | I Now Wat I'm Doin | 75 × 25 mm target | Glossy target | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Buy (pending verification)](https://www.redbubble.com/shop/ap/185334475) |
| ![Guess Who's the Mid Dad? artwork](stickers/guess-whos-the-mid-dad/print.png) | Guess Who's the Mid Dad? | 75 × 75 mm target | Glossy target | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Buy (pending verification)](https://www.redbubble.com/shop/ap/185334310) |

## Adding a sticker

Put each sticker in `stickers/<slug>/`, using a short lowercase slug with hyphens. Keep these files together:

For new artwork, use the [Redbubble sticker image brief](docs/redbubble-sticker-image-requirements.md)
to prepare and review the print image.

- `source.<ext>`: editable original artwork, preferably vector format.
- `print.<ext>`: print-ready PNG or PDF export at the dimensions accepted by the printer.
- `preview.<ext>`: small image for the README gallery, if the print export is unsuitable as a preview. The preview field may point to the print export.
- `metadata.yaml`: the sticker's name, physical size, finish, licence, and product URL.

`metadata.yaml` uses this schema:

```yaml
name: Example sticker
size_mm: [75, 75]
finish: matte
license: CC BY 4.0
source: source.svg
print: print.png
preview: preview.png
purchase_url: https://example.com/product-page
```

All fields are required. `size_mm` is the target `[width, height]` in millimetres. The file fields are paths relative to that sticker's directory. Set `purchase_url: null` until a product listing is published; then use its URL for the exact design. The five initial product URLs were provided by the owner and are provisional pending public verification; their gallery links are marked accordingly. A product's final size and finish must match its published listing.

The planned storefront is [DenhamParry on Redbubble](https://www.redbubble.com/people/DenhamParry/shop). The owner reports five listings, but their public availability still needs verification. Product listings and prices are managed in the owner's Redbubble artist account. The gallery links to the owner-provided product URLs rather than to the general shop.

## Licensing

Artwork in `stickers/` is © Lewis Denham-Parry and licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/), unless a sticker's metadata explicitly says otherwise. Attribute the creator as “Lewis Denham-Parry” and link to this repository and the licence when reusing an artwork file. The repository's `LICENSE` covers its software and configuration, not the sticker artwork.

## Contributing

Open a pull request with the source artwork, print export, metadata, and gallery row. Confirm that the artwork is yours to license and that the product link is live. The required `pre-commit` check validates repository formatting before a PR can merge.
