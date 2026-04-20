![LaTeX](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)
![Build](https://github.com/meyer-nils/thesis_template/actions/workflows/compile.yml/badge.svg)
[![Download thesis.pdf](https://img.shields.io/badge/Download-thesis.pdf-blue)](https://github.com/meyer-nils/thesis_template/releases/download/latest/thesis.pdf)
[![Download expose.pdf](https://img.shields.io/badge/Download-expose.pdf-blue)](https://github.com/meyer-nils/thesis_template/releases/download/latest/expose.pdf)

# LaTeX Thesis Template 

This repository provides a **LaTeX template** for student theses (lab projects, bachelor's and master's theses) at the **Institute of Materials Resource Management (MRM)** of the **University of Augsburg**.

> **Important: discuss everything with your supervisor first.**
> This template is a *suggestion* to help you get started. The exact structure, chapter titles, length, and formatting requirements must be agreed upon with your individual supervisor *before* you begin writing. Different chairs and research groups within the MRM may have specific conventions that differ from these defaults.

---

## Quick start

### Option A — Overleaf (recommended, no installation required)

Click the button below to open a copy of the template directly in Overleaf:

[![Open in Overleaf](https://img.shields.io/badge/Open%20in-Overleaf-47a141?logo=overleaf)](https://www.overleaf.com/docs?snip_uri=https://github.com/meyer-nils/thesis_template/archive/refs/heads/main.zip)

Alternatively, do it manually:
1. Download this repository as a ZIP file (`Code → Download ZIP` on GitHub).
2. In Overleaf: **New Project → Upload Project** and select the ZIP.
3. Set the main document to `thesis.tex` (Overleaf usually detects this automatically).

> The free tier on Overleaf offers only limited compile time. If you or your supervisor do not have access to Overleaf with sufficient compile time, simply use Option B below. 

### Option B — Local installation

You need a working LaTeX distribution and the `latexmk` tool.

| OS | Recommended distribution |
|----|--------------------------|
| Windows | [MiKTeX](https://miktex.org/) or [TeX Live](https://tug.org/texlive/) |
| macOS | [MacTeX](https://www.tug.org/mactex/) |
| Linux | TeX Live via your package manager (`texlive-full`) |


Clone or download the repository, then compile from the project root:

```bash
# Compile the thesis
latexmk -pdf thesis.tex

# Compile the exposé
latexmk -pdf expose.tex
```

All output files are placed in the project root. To clean up auxiliary files:

```bash
latexmk -c
```

---

## How to fill in the template

1. **`metadata.tex`** — Start here. Fill in your name, thesis type, study programme, supervisors, and professorship. Every field that needs your input is currently shown in **orange** in the compiled PDF. Read the comments in the file for guidance.

   To write your thesis in **German**, change the language toggle at the top of `metadata.tex`:
   ```latex
   \newcommand{\ThesisLanguage}{ngerman}  % was: english
   ```
   This switches hyphenation rules, all automatically generated labels (Contents → Inhaltsverzeichnis, Figure → Abbildung, etc.), the title page wording, and the declaration to German. Your chapter text still needs to be written in German by you.

2. **`chapters/`** — Write your thesis text in the numbered chapter files. The orange-coloured placeholder text in the compiled PDF explains what each section should contain. You can adjust this structure according to your needs - discuss this with your individual supervisor. 

3. **`literature.bib`** — Add your references in BibTeX format. Use a reference manager (Zotero, JabRef, Mendeley, etc.) to export entries automatically.

4. **`templates/`** — Fill in the abstract and declaration. Optional chapters (graphical abstract, acronyms, appendix, acknowledgments) can be removed by commenting out the corresponding `\input{...}` lines in `thesis.tex`.

5. **`expose.tex`** — Optional. If your supervisor asks for a written project outline before the thesis, use this file.

---

## Thesis length guidelines

The following are approximate page counts for the main body (introduction to conclusion). Front and back matter (abstract, acknowledgments, appendices, etc.) are not counted.

| Thesis type | Main body |
|-------------|-----------|
| Lab Project | 20–30 pages |
| Bachelor's thesis | 30–50 pages |
| Master's thesis | 50–80 pages |

Larger deviations from these ranges should be discussed with your supervisor.

---

## Downloading the compiled PDFs

Every push to `main` automatically compiles the template and attaches the PDFs to the [latest release](https://github.com/meyer-nils/thesis_template/releases/latest). Use the download buttons at the top of this page, or go to **Releases → latest** on the repository page.

---

## Notes on logos and university branding

The logo files in `images/logos/` (`mrm.png`, `uni_a.png`) are the property of the University of Augsburg and are subject to the university's branding guidelines. They are included here solely for use by students and staff of the University of Augsburg when preparing official thesis documents. They are **not** covered by the license that applies to the template code.

