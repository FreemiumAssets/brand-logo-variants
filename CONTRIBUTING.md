# Contributing to Brand Logo Variants

Thanks for helping grow this collection! Whether you're adding a new brand, fixing a distorted logo, or improving the docs, every contribution makes the project more useful for designers and developers.

## Ways to Contribute

- **Add a new brand** with all four variants
- **Fix an existing logo** that is outdated, distorted or inaccurate
- **Improve a conversion**, such as a cleaner outline or a better-optimized path
- **Request a brand** by opening an issue
- **Improve the documentation** or usage examples

## Adding a New Brand

1. **Fork** the repository and create a branch:

```bash
   git checkout -b add-brand-name
```

2. **Create a folder** in `logos/` named after the brand, in lowercase with hyphens:

```
   logos/visual-studio-code/
```

3. **Add all four variants** using these exact file names:

```
   logos/visual-studio-code/
   ├── primary.svg
   ├── black.svg
   ├── white.svg
   └── outline.svg
```

4. **Optimize** each SVG (see [Optimizing SVGs](#optimizing-svgs)).
5. **Update the README** by adding the brand, in alphabetical order, to  the **Available Brands** table.
6. **Open a pull request** using the checklist below.

Incomplete submissions (for example, only one or two variants) will be asked to add the missing files before merging.

## Variant Guidelines

| Variant | Requirements |
| :-- | :-- |
| **Primary** | The brand's official colors, matching its current mark |
| **Black** | Solid `#000000` only, no gradients or opacity |
| **White** | Solid `#FFFFFF` only, no gradients or opacity |
| **Outline** | Strokes only: `stroke="#000000"`, `stroke-width="5"` and `fill="none"` |

For brands whose mark is already a single color, Primary may match Black or White. That is fine.

## SVG Standards

Every file should:

- Be a clean, optimized vector with **no embedded raster images** (no base64 PNG/JPEG)
- Include a valid `viewBox`, and use a square one where the logo allows it
- Have **no** `<script>`, external references, fonts or tracking metadata
- Convert text to paths so it renders the same everywhere
- Stay recognizable as the **official mark**, with no redesigns, restyling or reinterpretations
- Be reasonably small, ideally a few KB

## Optimizing SVGs

Run every file through [SVGO](https://github.com/svg/svgo) before submitting:

```bash
npx svgo logos/your-brand/*.svg
```

Then open each file in a browser and check that it still renders correctly. Optimization can occasionally break complex paths or strokes, especially in outline variants.

## Sourcing Logos

- Start from the brand's **official press kit or brand guidelines** whenever possible.
- Only submit logos you have a reasonable basis to share. Don't submit files taken from paid or restricted asset libraries.
- Do not submit logos of brands that explicitly prohibit redistribution of their marks.

## Pull Request Checklist

Copy this into your pull request description:

```markdown
- [ ] Folder name is lowercase with hyphens
- [ ] All four files are included: primary, black, white, outline
- [ ] File names match the convention exactly
- [ ] SVGs are optimized with SVGO and render correctly
- [ ] Black is `#000000` and White is `#FFFFFF`
- [ ] Outline uses `stroke="#000000"`, `stroke-width="5"` and `fill="none"`
- [ ] No embedded raster images, scripts or external references
- [ ] The logo matches the brand's current official mark
- [ ] The brand is added to the README Available Brands table
```

## Commit and PR Style

Keep commit messages short and descriptive:

```
Add Notion logo variants
Fix Figma white variant viewBox
Update GitHub outline stroke width
```

Use one brand per pull request where possible. It makes review faster and easier to revert if something needs to change.

## Reporting Problems

Open an [issue](../../issues/new) if you find:

- A logo that is outdated, distorted or visually inaccurate
- A file that fails to render or has the wrong colors
- A missing variant
- A brand you'd like to see added

Please include the brand name, the file path, and a screenshot if it helps.

## Takedown Requests

All logos remain the property of their respective owners. If you are a rights holder and want a logo corrected or removed, [open an issue](../../issues/new) with the brand name and file path, and it will be handled promptly.

## Code of Conduct

Be respectful and constructive. Assume good intent, give clear feedback, and keep discussions focused on making the collection better for everyone. Harassment or discrimination of any kind is not tolerated.

## License

By contributing, you agree that your contributions to the repository's tooling, documentation and file organization are licensed under the [MIT License](LICENSE). Logos remain the property of their respective trademark owners, as described in the [README](README.md#license-and-trademark-disclaimer).

---

Thank you for contributing! ⭐