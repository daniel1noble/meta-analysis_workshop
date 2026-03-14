# Meta-Analysis Workshop

Materials for a 1.5-2 day meta-analysis workshop built with [Quarto](https://quarto.org/).

## Overview

This repository contains a comprehensive Quarto book covering meta-analytic methods, from basic concepts to advanced topics including:

- Introduction to meta-analysis
- Calculating and interpreting effect sizes
- Effect size assumptions
- Fixed-effect vs. random-effects models
- Heterogeneity and nuisance heterogeneity
- Meta-regression
- Multi-level models
- Complex non-independence
- Phylogenetic meta-analysis
- Publication bias

## Viewing the Book

The book is published at: `https://<username>.github.io/meta-analysis_workshop/`

## Local Development

### Prerequisites

- [Quarto](https://quarto.org/docs/get-started/)
- [R](https://www.r-project.org/) (version 4.0 or higher)
- Required R packages (see below)

### Installing R Dependencies

```r
install.packages(c(
  "knitr", "rmarkdown", "metafor", "flextable", 
  "tidyverse", "orchaRd", "pander", "mathjaxr", 
  "equatags", "vembedr", "bookdown"
))
```

### Building the Book Locally

To preview the book locally:

```bash
quarto preview
```

To render the complete book:

```bash
quarto render
```

The rendered book will be in the `_book/` directory.

## GitHub Pages Setup

The book is automatically deployed to GitHub Pages via GitHub Actions whenever changes are pushed to the main/master branch.

### First-time Setup

1. Go to your repository Settings
2. Navigate to Pages (under "Code and automation")
3. Under "Build and deployment":
   - Source: Select "GitHub Actions"
4. Push changes to trigger the workflow

The site will be available at `https://<username>.github.io/<repository-name>/`

## Repository Structure

- `*.qmd` - Quarto markdown files for each chapter
- `_quarto.yml` - Quarto book configuration
- `index.qmd` - Book landing page
- `.github/workflows/publish.yml` - GitHub Actions workflow for deployment
- `bib/` - Bibliography files (if present)

## Contributing

To add or modify content:

1. Edit the relevant `.qmd` file
2. Preview changes locally with `quarto preview`
3. Commit and push to trigger automatic deployment

## License

Materials for meta-analysis workshop
