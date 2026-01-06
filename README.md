# LaTeX Document Templates

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![LaTeX](https://img.shields.io/badge/LaTeX-XeLaTeX%2FLuaLaTeX-green.svg)
![Language](https://img.shields.io/badge/language-CN%2FEN-orange.svg)
![GitHub Pages](https://img.shields.io/badge/docs-GitHub%20Pages-brightgreen.svg)

A collection of modern, clean LaTeX document templates for academic papers, lecture notes, reports, and books. Supports both Chinese and English typesetting with professional styling.

> **📌 Source**: These templates are sourced from [MIStatlE/math-to-ml-](https://github.com/MIStatlE/math-to-ml-). Special thanks to the original authors!

## Quick Start

1. **Navigate to the `templates` directory**:
   ```bash
   cd templates
   ```

2. **Choose a template**:
   - `article-cn.tex` - Chinese article template with colored boxes
   - `article-en.tex` - English lecture notes template
   - `article-modern.tex` - Modern article with sidebar design
   - `article-enhanced.tex` - Enhanced article with theorem environments
   - `book.tex` - Book template with parts and chapters

3. **Edit the template** - Update title, author, and content sections.

4. **Compile**:
   ```bash
   xelatex your-document.tex
   # or
   lualatex your-document.tex
   ```

   For VS Code users with the LaTeX Workshop extension, configure the compiler to use XeLaTeX or LuaLaTeX.

## Templates Overview

| Template | Description | Best For |
|----------|-------------|----------|
| `article-cn.tex` | Chinese template with theorem boxes | Academic papers, research notes |
| `article-en.tex` | English lecture notes format | Course notes, tutorials |
| `article-modern.tex` | Modern design with left sidebar | Technical notes, series articles |
| `article-enhanced.tex` | Enhanced theorem environments | Mathematics, proofs |
| `book.tex` | Full book structure | Textbooks, comprehensive guides |

## Features

- ✨ Modern design with professional typography
- 🎨 Colored theorem boxes (theorems, lemmas, definitions)
- 📚 Support for Chinese and English documents
- 📝 Pre-configured algorithm environments
- 🖼️ Sidebar and highlight boxes
- 📖 Book template with parts, chapters, and appendices

## Requirements

- TeX distribution with XeLaTeX or LuaLaTeX
- Chinese fonts (for CN templates):
  - `Noto Serif CJK SC` (preferred) or `FandolSong`
- English fonts:
  - `Times New Roman`

## Documentation

For detailed usage instructions, examples, and customization options, see the [comprehensive guide](docs/GUIDE.md).

## Examples

Check out the templates in the `templates/` directory for ready-to-use examples with sample content demonstrating various features.

## Project Structure

```
├── .github/
│   └── workflows/       # GitHub Actions workflows
│       ├── deploy.yml   # GitHub Pages deployment
│       └── latex-check.yml
├── templates/           # LaTeX templates
│   ├── article-cn.tex   # Chinese article template
│   ├── article-en.tex   # English lecture notes
│   ├── article-modern.tex
│   ├── article-enhanced.tex
│   └── book.tex         # Book template
├── docs/
│   └── GUIDE.md         # Comprehensive documentation
├── index.html           # GitHub Pages landing page
├── LICENSE
└── README.md
```

## Credits

These LaTeX templates are sourced from:

- **Original Repository**: [MIStatlE/math-to-ml-](https://github.com/MIStatlE/math-to-ml-)
- **Authors**: MIStatlE and contributors

We extend our gratitude to the original authors for creating and sharing these beautiful templates.

## Citation

If you use these templates in your work, please cite:

```bibtex
@misc{latex-templates-2025,
  author = {MIStatlE},
  title = {LaTeX Document Templates},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/MIStatlE/math-to-ml-}
}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.

---

**Happy writing!** ✍️
