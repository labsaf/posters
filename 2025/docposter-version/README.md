# Docposter - Academic Poster using Quarto

This directory contains a poster created using the **docposter** Quarto extension, adapted from the original posterdown RMarkdown template.

## What is Docposter?

Docposter is an experimental Quarto extension that allows you to create academic posters using Markdown and HTML/CSS instead of traditional slide software or LaTeX. It's based on the [bbucior/docposter](https://github.com/bbucior/docposter) project.

## Prerequisites

To render this poster, you need:

1. **Quarto** - Install from [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)
2. **Docposter extension** - Install using the command below

## Installation

### Option 1: Using this existing template

If you're using this already-created template, you need to install the docposter extension:

```bash
cd 2025/docposter-version
quarto add bbucior/docposter
```

### Option 2: Creating a new docposter project from scratch

If you want to start fresh with the official template:

```bash
quarto use template bbucior/docposter
```

This will create a new directory with the docposter template.

## File Structure

```
docposter-version/
├── _quarto.yml          # Quarto configuration
├── poster.qmd           # Main poster content (Markdown)
├── custom.css           # Custom styling
├── references.bib       # Bibliography references
├── packages.bib         # R package citations
├── mdpi.csl            # Citation style
├── apa.csl             # Alternative citation style
└── resources/          # Images and figures
```

## How to Use

### 1. Edit the Content

Edit `poster.qmd` to modify the poster content. The structure uses:

- **Level 1 headers (`#`)** with classes like `{.col-2}`, `{.col-3}`, or `{.col-4}` define column layouts
- **Level 2 headers (`##`)** create individual content blocks within columns

Example structure:
```markdown
# {.col-3}
## Introduction
Content here...

## Methods
Content here...

## Results
Content here...

# {.col-2}
## Discussion
Content here...

## Conclusions
Content here...
```

### 2. Customize the Appearance

Edit `custom.css` to change:
- Colors (primary, secondary, accent)
- Fonts and typography
- Block styling
- Spacing and layout

### 3. Render the Poster

To generate the poster, run:

```bash
quarto render
```

Or to preview while editing:

```bash
quarto preview
```

This will create an HTML file that you can:
- Open in a web browser
- Print to PDF
- Share online

### 4. Convert to PDF (Optional)

To convert the HTML poster to PDF, you can:

1. Open the HTML file in Chrome/Chromium
2. Use Print → Save as PDF
3. Or uncomment the `post-render` section in `_quarto.yml` to automate this

## Key Differences from Posterdown

| Feature | Posterdown (RMarkdown) | Docposter (Quarto) |
|---------|----------------------|-------------------|
| **Format** | RMarkdown (.Rmd) | Quarto Markdown (.qmd) |
| **Rendering** | knitr + rmarkdown | Quarto engine |
| **Styling** | R-based styling | HTML/CSS |
| **Layout** | YAML parameters | Header classes |
| **Code chunks** | R chunks | Multiple languages |

## Tips

1. **Images**: Place all images in the `resources/` folder
2. **Citations**: Add references to `references.bib` and cite with `[@citation_key]`
3. **Layout**: Use `.col-2`, `.col-3`, or `.col-4` classes to control column numbers
4. **Preview**: Use `quarto preview` for live updates while editing

## Original Content

This poster contains content about:
**"Implementación de computación en la nube para el mapeo digital de propiedades de suelos agrícolas a partir de imágenes multiespectrales UAV de alta resolución"**

A research project on cloud computing implementation for digital mapping of agricultural soil properties using high-resolution UAV multispectral images.

## References

- Docposter GitHub: [https://github.com/bbucior/docposter](https://github.com/bbucior/docposter)
- Quarto Documentation: [https://quarto.org/docs/](https://quarto.org/docs/)

## Note

The docposter extension is experimental and not actively maintained. For production use, consider alternatives like:
- [posterdown](https://github.com/brentthorne/posterdown) (RMarkdown)
- Quarto dashboards
- Traditional LaTeX beamerposter

## License

Content follows the original project's GPL-3.0 license.
