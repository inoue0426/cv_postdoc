# Yoshitaka Inoue — Academic CV and Bibliography

[![Build and Deploy LaTeX CV](https://github.com/inoue0426/cv_postdoc/actions/workflows/latex.yml/badge.svg)](https://github.com/inoue0426/cv_postdoc/actions/workflows/latex.yml)

**Academic CV and complete bibliography of Yoshitaka Inoue**, maintained in LaTeX and automatically compiled with GitHub Actions.

📄 **Latest CV:** [Yoshitaka_Inoue_CV.pdf](https://inoue0426.github.io/cv_postdoc/Yoshitaka_Inoue_CV.pdf)

📚 **Complete Bibliography:** [Yoshitaka_Inoue_Bibliography.pdf](https://inoue0426.github.io/cv_postdoc/Yoshitaka_Inoue_Bibliography.pdf)

🌐 **CV landing page:** [inoue0426.github.io/cv_postdoc](https://inoue0426.github.io/cv_postdoc/)

---

## Overview

This repository contains two separate LaTeX documents:

- `ecr-cv.tex` — academic CV for postdoctoral and academic applications, with a selected publication list.
- `bibliography.tex` — complete publication record, maintained independently from the CV.

The bibliography is based on the publication list in [Google Scholar](https://scholar.google.com/citations?user=aBizyLkAAAAJ&hl=en). It includes journal articles, preprints/workshop papers, and conference abstracts, including separate Scholar records for abstracts that later became journal publications.

## Automated PDF Build

GitHub Actions automatically compiles both documents and publishes the resulting PDFs.

### On every relevant push to `main`

1. `ecr-cv.tex` is compiled to `Yoshitaka_Inoue_CV.pdf`.
2. `bibliography.tex` is compiled to `Yoshitaka_Inoue_Bibliography.pdf`.
3. Both PDFs are uploaded as GitHub Actions artifacts.
4. Both PDFs are deployed to GitHub Pages.

Pull requests run the compilation step as a build check without deploying to Pages.

The workflow can also be triggered manually from the **Actions** tab.

## Repository Structure

```text
.
├── ecr-cv.tex
├── bibliography.tex
├── badges/
│   ├── opencode.png
│   ├── opendata.png
│   ├── openmaterial.png
│   ├── preregistered.png
│   └── preregisteredplus.png
├── .github/
│   └── workflows/
│       └── latex.yml
└── README.md
```

- `ecr-cv.tex` — main academic CV source
- `bibliography.tex` — complete bibliography source
- `badges/` — optional open-science badge assets
- `.github/workflows/latex.yml` — automated build and GitHub Pages deployment

## Compile Locally

A standard LaTeX distribution such as **TeX Live**, **MacTeX**, or **MiKTeX** is sufficient.

```bash
pdflatex ecr-cv.tex
pdflatex bibliography.tex
```

For a more robust build:

```bash
latexmk -pdf ecr-cv.tex
latexmk -pdf bibliography.tex
```

The outputs will be:

```text
ecr-cv.pdf
bibliography.pdf
```

## Updating Publications

Use the Google Scholar profile as the source list for the complete bibliography:

[Google Scholar — Yoshitaka Inoue](https://scholar.google.com/citations?user=aBizyLkAAAAJ&hl=en)

When a new item appears on Scholar:

1. Add it to the appropriate section of `bibliography.tex`.
2. Add it to `ecr-cv.tex` only if it belongs in the selected publication list for the CV.
3. Push the change; GitHub Actions will rebuild both PDFs automatically.

This keeps the complete publication record separate from the shorter, application-focused CV.

## Editing the CV

Personal and professional information is defined near the top of `ecr-cv.tex`, including:

```tex
\def\name{Yoshitaka Inoue}
\def\position{...}
\def\affiliation{...}
\def\address{...}
\def\email{...}
\def\website{...}
```

Sections can be edited directly in the LaTeX source. After changes are pushed to `main`, the public PDF is rebuilt automatically.

## Source Template

The CV is based on the **FORRT LaTeX Curriculum Vitae Template** by Emily Friedel, with subsequent customization for this academic CV.

Template information and attribution are retained in the LaTeX source.

---

**Yoshitaka Inoue**  
University of Minnesota, Twin Cities · National Institutes of Health  
[Website](https://inoue0426.github.io/) · [Google Scholar](https://scholar.google.com/citations?user=aBizyLkAAAAJ&hl=en) · [GitHub](https://github.com/inoue0426) · [LinkedIn](https://www.linkedin.com/in/inoue0426/)
