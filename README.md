# Privacy Standards Project

Theoretical analysis of international privacy standards:

- ISO/IEC 29100 — Privacy Framework
- ISO/IEC 29151 — Code of Practice for PII Protection
- ISO/IEC 29134 — Privacy Impact Assessment
- NIST SP 800-122 — Guide to Protecting the Confidentiality of PII

## 📄 Deliverables

- **Report:** LaTeX-based document (`main.tex`)
- **Slides:** Beamer/PowerPoint presentation (`slides/presentation.tex`)
- **PDF Release:** Automatically generated when a new release is published

## ⚙️ How to Compile Locally

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## 📁 Project Structure

```bash
privacy-standards-project/
│
├── main.tex
├── references.bib
├── README.md
├── LICENSE
├── .gitignore
│
├── sections/
│   ├── section01.tex
│   ├── section02.tex
│   ├── ...
│
├── images/
├── slides/
│   └── presentation.tex
│
└── .github/
    └── workflows/
        └── latex-on-release.yml

```
