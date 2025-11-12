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

---

## 🧩 Repository Workflow and Collaboration Guide

This section explains how to collaborate, track progress, and maintain consistency within the _Privacy Standards Project_ repository.

---

### 🐞 1. Creating and Managing Issues

Issues are used to **track every unit of work**, whether it’s writing a section, fixing a LaTeX error, or updating references.

**When to open an Issue:**

- You are starting a new section or major paragraph in LaTeX  
  → _e.g., “Add section on ISO/IEC 29151”_
- You need to fix a formatting or compilation error  
  → _e.g., “Fix table overflow in section 5”_
- You want to request a review or improvement  
  → _e.g., “Review comparison table between ISO and NIST”_
- You are preparing a release or milestone deliverable

**Steps:**

1. Go to **Issues → New Issue**
2. Give it a clear title and short description
3. Add one or more **labels** (see below)
4. Assign a **milestone** (e.g., `v0.5 - First Full Draft`)
5. Optionally, assign it to yourself
6. Link it to the Project board (appears under _To Do_)

---

### 🏷️ 2. Label Usage

Labels classify the type and status of each Issue.  
Use the following standardized set:

| Label          | Purpose                                   | Example                                       |
| :------------- | :---------------------------------------- | :-------------------------------------------- |
| `content`      | Writing new LaTeX sections or major edits | “Draft ISO/IEC 29100 section”                 |
| `review`       | Proofreading, improving wording or flow   | “Reword NIST objectives paragraph”            |
| `latex`        | Fixes or formatting problems in LaTeX     | “Fix table margin overflow in comparison.tex” |
| `bibliography` | Updating references or BibTeX entries     | “Add ENISA citation to ISO 29134 section”     |
| `slides`       | Tasks related to presentation materials   | “Summarize standards for Beamer slides”       |

---

### 🎯 3. Assigning Milestones

Each Issue should belong to a **milestone** representing a stage of progress.

| Milestone                 | Description                                  |
| :------------------------ | :------------------------------------------- |
| `v0.1 - Outline`          | Initial structure and intro                  |
| `v0.3 - Core Draft`       | First main sections written                  |
| `v0.5 - First Full Draft` | All sections drafted                         |
| `v0.8 - Reviewed Version` | Revisions, diagrams, and citations finalized |
| `v1.0 - Final Release`    | Ready for publication and PDF generation     |

**To assign:**  
When creating or editing an Issue → right sidebar → _Milestone_ → select the corresponding one

---

### 🧱 4. Workflow (From Issue to Release)

1. **Open an Issue** describing the task
2. **Create a branch** named after it (use scope/kebab-case, where scope can feat, fix or other from the commit style convention):  
   `git checkout -b feat/iso29100-section`
3. **Work locally** on the related `.tex` file inside `/sections/`
4. **Commit your changes** using the convention below
5. **Push** the branch to GitHub:  
   `git push -u origin feat/iso29100-section`
6. **Open a Pull Request**, referencing the Issue:  
   `Closes #12`
7. Once merged → the Issue is closed automatically
8. Move the Issue card in the **Project Board** to **Done**

---

### 🧩 5. Commit Style Convention

To keep a clean and readable Git history, follow this syntax:

`type(scope): short-description`

> Use **kebab-case** for the scope (lowercase words separated by hyphens).

| Type    | Meaning                                     |
| ------- | ------------------------------------------- |
| `feat`  | Added a new feature, section, or paragraph  |
| `fix`   | Fixed a bug, LaTeX or formatting issue      |
| `chore` | Repository maintenance or cleanup           |
| `docs`  | Edited documentation or README              |
| `style` | Cosmetic edits (spacing, indentation, etc.) |

**Examples:**

- `feat(iso29100-section): add first draft of privacy principles`
- `fix(latex): correct table alignment in comparison section`
- `docs(readme): explain issue labeling process`

---

### 🚀 6. Creating a Release (Automatic PDF Build)

When the project reaches a stable version:

1. Go to **Releases → Draft a new release**
2. Choose a tag (e.g., `v1.0`)
3. Add a title and short description
4. Click **Publish release**

GitHub Actions will automatically:

- Compile `main.tex`
- Build the `main.pdf`
- Rename it to `Privacy-Standards-v1.0.pdf`
- Attach it to the release page

---

### 🧭 7. Project Board Overview

Use the **Project Board (Kanban)** to visualize progress:

| Column          | Purpose                        |
| --------------- | ------------------------------ |
| **To Do**       | Tasks not started yet          |
| **In Progress** | Active writing or editing      |
| **Review**      | Needs proofreading or feedback |
| **Done**        | Completed and merged           |

Each new Issue appears in _To Do_ and moves across as you work on it.

---

### 🧠 8. Best Practices

- Always **link Issues to Pull Requests** → keeps traceability
- **Commit often** with meaningful messages
- Keep each branch focused on **one Issue/task**
- Use **milestones** for release tracking
- Prefer **English** for Issues and commits
- Use **kebab-case** (no spaces, no uppercase) for branch and file names, e.g.:
  - `sections/iso29100-framework.tex`
  - `feat/nist-summary`

---
