# Self-hosted fonts

These unmodified Latin WOFF2 files are distributed under the SIL Open Font License 1.1. The matching copyright notices and full licenses are included here.

- DM Serif Display, Google Fonts version 17: `dm-serif-display-latin-regular.woff2` and `dm-serif-display-latin-italic.woff2`. License: `DM-Serif-Display-OFL.txt`.
- Manrope, Google Fonts version 20: `manrope-latin-variable.woff2`, weights 400 through 800. License: `Manrope-OFL.txt`.

Downloaded from the official Google Fonts distribution. Visitors load only these local files, not the URLs below. The Latin subsets include the accented letters and ligatures used by the French and English pages. Check glyph coverage again when adding names in another character set.

## Sources

- [DM Serif Display regular WOFF2](https://fonts.gstatic.com/s/dmserifdisplay/v17/-nFnOHM81r4j6k0gjAW3mujVU2B2G_Bx0vrx52g.woff2)
- [DM Serif Display italic WOFF2](https://fonts.gstatic.com/s/dmserifdisplay/v17/-nFhOHM81r4j6k0gjAW3mujVU2B2G_VB0PD2xWr53A.woff2)
- [Manrope variable WOFF2](https://fonts.gstatic.com/s/manrope/v20/xn7gYHE41ni1AdIRggexSvfedN4.woff2)
- [DM Serif Display license](https://github.com/google/fonts/blob/main/ofl/dmserifdisplay/OFL.txt)
- [Manrope license](https://github.com/google/fonts/blob/main/ofl/manrope/OFL.txt)

## Fallback metrics

The stylesheet adjusts Georgia (regular and italic) and Arial (regular and bold) to match each display/body face's x-height. Ascent, descent and line-gap overrides use the target font's hhea table, divided by the size adjustment. The bundled Manrope file has a consistent x-height across the used weight range. Explicit line heights keep line boxes stable; glyph widths can still differ during font swap. FontTools was used only for inspection, not to modify the font files, and is not a site dependency.
