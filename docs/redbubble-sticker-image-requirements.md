# Redbubble sticker image brief

Checked against Redbubble's published guidance on 2026-11-04. This brief is for
creating one original sticker image at a time for the
[DenhamParry shop](https://www.redbubble.com/people/DenhamParry/shop).

## Store and creative context

- Creator: Lewis Denham-Parry, a Cardiff-based technologist and speaker.
- Direction: bold, playful digital illustrations inspired by technology,
  everyday absurdities, and community. Give each design a clear silhouette and
  a joke or idea that reads quickly. The first artwork,
  [I See BMCs](../stickers/i-see-bmcs/print.png), is a reference, not a template
  that every new design must copy.
- Rights: use original artwork that the creator can publish under the recorded
  artwork licence, currently CC BY 4.0. Do not include third-party characters,
  logos, or assets without permission.
- Store setup: the owner reports needing five items before the shop can open;
  each item still needs its own artwork and product listing. Redbubble's
  [getting-started guide](https://blog.redbubble.com/2020/05/getting-started-on-redbubble-2/)
  recommends at least five artworks when setting up a shop. Treat the owner's
  five-item requirement as an account-specific prerequisite, not a universal
  platform rule.

## Print image requirements

1. Create a single isolated illustration, not a product mockup or a photo of a
   sticker. Export a PNG with a genuinely transparent background. Keep clean
   alpha edges and remove stray pixels outside the intended shape. Redbubble
   uses the artwork edge to make its kiss-cut outline, so do not add a production
   cut border; an intentional border may be part of the illustration.
2. Aim for a **2800 × 2800 pixel** transparent print PNG when a square canvas
   suits the design. Redbubble recommends that size to make all four sticker
   sizes available. A smaller file may limit the sizes offered. Generate or
   export from a source with enough real detail; simply enlarging a small
   raster image does not add detail.
3. Keep shapes, contrast, and any text readable at the smallest offered size.
   If text is required, specify its exact words and proofread the final pixels.
   Check light and white areas in Redbubble's matte, glossy, and transparent
   previews because the finishes use different backgrounds.
4. Inspect the uploaded product preview for the selected sizes and finishes.
   Confirm that no parts are clipped, no stray pixels create extra cut areas,
   and the actual listing matches the metadata. The store owner chooses the
   final product options in Redbubble.

These image and preview points follow Redbubble's
[sticker design guide](https://blog.redbubble.com/2024/10/tips-on-designing-for-stickers-2/)
and [transparent-background guide](https://blog.redbubble.com/2017/03/how-to-create-transparent-backgrounds/).
The current [I See BMCs print PNG](../stickers/i-see-bmcs/print.png) is 1254 ×
1254 pixels and predates this preferred full-size target. Do not present its
draft 75 mm glossy target as a verified Redbubble listing specification.

## Repository handoff

Keep an editable `source.<ext>`, the transparent `print.png`, and
`metadata.yaml` in `stickers/<slug>/` as described in the
[README](../README.md#adding-a-sticker). A gallery preview may reuse the print
PNG. Set `purchase_url: null` until the exact sticker product page is public and
verified; the general shop URL is not a product buy link.

## Copy-ready generation prompt

> Create one original sticker illustration for Lewis Denham-Parry's DenhamParry
> Redbubble shop. Lewis is a Cardiff-based technologist and speaker. The shop's
> direction is bold, playful digital art inspired by the funny side of
> technology and everyday life. This is one of five initial original designs;
> use only elements Lewis can publish under CC BY 4.0. The first sticker,
> I See BMCs, sets an expressive tech-humour tone without prescribing the
> subject of this new design. The specific idea is **[describe the subject,
> action, and joke]**. Use **[palette and mood]** with a strong silhouette,
> expressive details, and high contrast that remains clear at small sticker
> size. Include exactly **[text, or "no text"]**; if text is used, make it
> legible and check the spelling. Make one isolated design on a fully
> transparent background with clean edges and no stray pixels. Do not draw a
> production white cut border, product mockup, background scene, watermark, or
> unlicensed character or logo. Deliver a 2800 × 2800 pixel transparent PNG
> suitable for Redbubble's sticker preview, plus an editable source if the tool
> supports one. If the tool cannot produce that resolution with real detail,
> retain the best source for a proper export rather than upscaling a small
> raster output. Leave product size, finish, price, and purchase URL for the
> owner to set and verify in Redbubble.
