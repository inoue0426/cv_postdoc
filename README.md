# Yoshitaka Inoue — Academic CV

[![Build and Deploy LaTeX CV](https://github.com/inoue0426/cv_postdoc/actions/workflows/latex.yml/badge.svg)](https://github.com/inoue0426/cv_postdoc/actions/workflows/latex.yml)

**Academic CV of Yoshitaka Inoue**, maintained in LaTeX and automatically compiled with GitHub Actions.

📄 **Latest CV:** [Yoshitaka_Inoue_CV.pdf](https://inoue0426.github.io/cv_postdoc/Yoshitaka_Inoue_CV.pdf)

🌐 **CV landing page:** [inoue0426.github.io/cv_postdoc](https://inoue0426.github.io/cv_postdoc/)

---

## Overview

This repository contains the LaTeX source for my academic CV, including research experience, publications, education, awards, service, and other academic activities.

The CV is designed for academic and postdoctoral applications and is continuously maintained as the source of record for the public PDF.

## Automated PDF Build

GitHub Actions automatically compiles `ecr-cv.tex` and publishes the resulting PDF.

### On every push to `main`

1. `ecr-cv.tex` is compiled with LaTeX.
2. The generated PDF is renamed to `Yoshitaka_Inoue_CV.pdf`.
3. The PDF is uploaded as a GitHub Actions artifact.
4. The latest version is deployed to GitHub Pages.

Pull requests run the compilation step as a build check without deploying to Pages.

The workflow can also be triggered manually from the **Actions** tab.

## Repository Structure

```text
.
├── ecr-cv.tex
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

- `ecr-cv.tex` — main LaTeX source
- `badges/` — optional open-science badge assets
- `.github/workflows/latex.yml` — automated build and GitHub Pages deployment

## Compile Locally

A standard LaTeX distribution such as **TeX Live**, **MacTeX**, or **MiKTeX** is sufficient.

```bash
pdflatex ecr-cv.tex
```

For a more robust build that automatically handles repeated compilation passes:

```bash
latexmk -pdf ecr-cv.tex
```

The output will be:

```text
ecr-cv.pdf
```

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

## Open Science Badges

The `badges/` directory contains optional assets for annotating publications with open-science indicators:

- Open Code
- Open Data
- Open Materials
- Preregistered
- Preregistered+

These assets are retained as part of the original CV template design and can be used where appropriate.

## Source Template

This CV is based on the **FORRT LaTeX Curriculum Vitae Template** by Emily Friedel, with subsequent customization for my academic CV.

Template information and attribution are retained in the LaTeX source.

---

**Yoshitaka Inoue**  
University of Minnesota, Twin Cities · National Institutes of Health  
[Website](https://inoue0426.github.io/) · [Google Scholar](https://scholar.google.co.jp/citations?user=aBizyLkAAAAJ&hl=en) · [GitHub](https://github.com/inoue0426) · [LinkedIn](https://www.linkedin.com/in/inoue0426/)
