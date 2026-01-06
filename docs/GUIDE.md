# LaTeX Document Templates - Comprehensive Guide

This guide provides detailed instructions for using the LaTeX templates in this repository.

## Table of Contents

- [Getting Started](#getting-started)
- [Template Descriptions](#template-descriptions)
- [Customization](#customization)
- [Theorem Environments](#theorem-environments)
- [Colored Boxes](#colored-boxes)
- [Compilation](#compilation)
- [Troubleshooting](#troubleshooting)

## Getting Started

### Prerequisites

1. **TeX Distribution**: Install a TeX distribution that includes XeLaTeX or LuaLaTeX:
   - Windows: [MiKTeX](https://miktex.org/) or [TeX Live](https://www.tug.org/texlive/)
   - macOS: [MacTeX](https://www.tug.org/mactex/)
   - Linux: TeX Live (via package manager)

2. **Fonts**:
   - For Chinese templates: `Noto Serif CJK SC` or `FandolSong`
   - For English templates: `Times New Roman`

### First Steps

1. Copy the desired template to your working directory
2. Open the `.tex` file in your preferred editor
3. Modify the title, author, and content
4. Compile using XeLaTeX or LuaLaTeX

## Template Descriptions

### article-cn.tex (Chinese Article)

A clean Chinese article template optimized for academic papers and research notes.

**Features:**
- Chinese font support with `ctex`
- Colored theorem environments (blue shaded)
- Algorithm environment (`algorithm2e`)
- Analysis and Remark boxes
- Professional section styling

**Best for:** Chinese academic papers, research reports, course notes

### article-en.tex (English Lecture Notes)

Traditional lecture notes format inspired by academic course materials.

**Features:**
- Lecture header with course info, date, and instructor
- Section numbering tied to lecture number
- Theorem/Lemma/Definition environments
- Analysis boxes with `tcolorbox`
- Clean reference styling

**Best for:** Course lecture notes, tutorials, academic handouts

### article-modern.tex (Modern Article)

A visually appealing modern template with sidebar design elements.

**Features:**
- Left sidebar bands on every page
- Key Idea and Takeaway highlight boxes
- SideBar environment for context/introductions
- Chapter mechanism for multi-chapter articles
- Series navigation cards
- Shaded theorem environments

**Best for:** Technical blog posts, series articles, modern academic notes

### article-enhanced.tex (Enhanced Article)

Enhanced version with beautiful colored theorem environments.

**Features:**
- Color-coded theorem environments:
  - **Theorems**: Blue left bar, light blue background
  - **Lemmas**: Red left bar, light pink background
  - **Definitions**: Teal left bar, light teal background
- Semantic highlight shortcuts (`\KeyIdea`, `\Term`, `\Emph`, `\Confuse`)
- Example boxes with purple styling
- All features from article-modern.tex

**Best for:** Mathematics papers, proof-heavy documents, advanced lecture notes

### book.tex (Book Template)

Complete book template with frontmatter, mainmatter, and backmatter.

**Features:**
- Part/Chapter/Section hierarchy
- Styled title pages for Parts and Chapters
- Table of Contents with configurable depth
- Cover page macro
- Chapter epigraphs
- Appendix support
- Optional mini table of contents per chapter (minitoc)

**Best for:** Textbooks, comprehensive guides, thesis documents

## Customization

### Colors

All templates use a consistent color palette that you can customize:

```latex
\definecolor{brand}{HTML}{1A9D8F}      % Primary teal
\definecolor{brandD}{HTML}{2A7F6F}     % Dark teal
\definecolor{keybg}{HTML}{E8F4F1}      % Light teal background
\definecolor{keydark}{HTML}{2F5E58}    % Dark teal for text
\definecolor{accent}{HTML}{FF6B6B}     % Accent red
\definecolor{accentD}{HTML}{D94F4F}    % Dark accent red
```

### Page Layout

Modify page dimensions in the geometry package:

```latex
\geometry{paperwidth=7.5in, paperheight=10in, margin=0.7in}
```

For standard A4:
```latex
\geometry{a4paper, margin=1in}
```

### Fonts

Change the main font:
```latex
\setmainfont{Your Font Name}
\setCJKmainfont{Your CJK Font}  % For Chinese
```

### Headers and Footers

Customize using `fancyhdr`:

```latex
\fancyhead[L]{Left Header}
\fancyhead[R]{Right Header}
\fancyfoot[C]{\thepage}
```

## Theorem Environments

### Basic Usage

```latex
\begin{theorem}[Optional Title]
Your theorem statement here.
\end{theorem}

\begin{lemma}
A supporting lemma.
\end{lemma}

\begin{definition}[Key Concept]
Your definition here.
\end{definition}
```

### Proof Environment

```latex
\begin{proof}
Your proof steps here.
\end{proof}

% Custom proof title (Chinese)
\begin{proof}[证明]
证明步骤...
\end{proof}
```

## Colored Boxes

### Key Idea Box

```latex
\begin{KeyBox}
Main insight or key concept to remember.
\end{KeyBox}
```

### Takeaway Box

```latex
\begin{Takeaway}
Summary of important points.
\end{Takeaway}
```

### Example Box

```latex
\begin{Example}
A worked example demonstrating the concept.
\end{Example}
```

### Sidebar

```latex
\begin{SideBar}
\textbf{Context:} Background information or reading notes.
\end{SideBar}
```

### Semantic Highlights (article-enhanced.tex)

```latex
\KeyIdea{Important concept}    % Light teal background
\Term{Technical term}          % Deep blue bold text
\Emph{Emphasized text}         % Red bold text
\Confuse{Unclear part}         % Red background highlight
\Info{Additional information}  % Blue informational text
```

## Compilation

### Command Line

```bash
# Single compilation
xelatex document.tex

# With bibliography
xelatex document.tex
biber document
xelatex document.tex
xelatex document.tex
```

### VS Code + LaTeX Workshop

Add to your `settings.json`:

```json
{
  "latex-workshop.latex.tools": [
    {
      "name": "xelatex",
      "command": "xelatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOC%"
      ]
    }
  ],
  "latex-workshop.latex.recipes": [
    {
      "name": "xelatex",
      "tools": ["xelatex"]
    }
  ]
}
```

### Overleaf

1. Upload the template files
2. Set the compiler to XeLaTeX in project settings
3. Compile as usual

## Troubleshooting

### Font Not Found

**Error:** `Font "Noto Serif CJK SC" not found`

**Solution:** Install the font or use the fallback:
```latex
\setCJKmainfont{FandolSong}
```

### Chinese Characters Not Displaying

**Solution:** Ensure you're using XeLaTeX or LuaLaTeX, not pdfLaTeX.

### Package Conflicts

**Error:** `Option clash for package xxx`

**Solution:** Load conflicting packages before `\documentclass` or remove duplicate loads.

### tcolorbox Errors

**Solution:** Make sure you have `tcolorbox` with the `most` library:
```latex
\usepackage[most]{tcolorbox}
```

### Undefined Control Sequence

**Solution:** Check for missing packages or typos in command names.

---

For additional help, please open an issue on the GitHub repository.
