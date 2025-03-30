# Plain mathematics book

A clean, simple, and ready-to-use LaTeX template for quickly starting your mathematics book.

## Table of Contents

- [Structure](#structure)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Compilation](#compilation)
- [Maintainers](#maintainers)
- [License](#license)

## Structure

The repository is structured as follows:

- main.tex: The root LaTeX file of the book.
- plainBook.sty: The LaTeX style file of the book.
- content: The directory of all the content of the book.
    - frontmatter: The directory of front matter of the book.
        - perface.tex: The perface of the book.
    - mainmatter: The directory of main matter of the book.
        - 1Part: A part of the book. You can rename this directory or create additional directories for other parts.
            - 1Chapter.tex: A chapter of the book. You can rename this file or create additional files for other chapters.
    - backmatter: The directory of back matter of the book.
        - index.tex: The file containing the LaTeX command that instructs LaTeX to insert the generated index into the document.
        - bibliography.tex: The file containing the LaTeX command that instructs LaTeX to insert the generated bibliography into the document.
        - bibliography.bib: The bibliography database file.
- main.pdf: The compiled PDF output of the book.
- README.md: The file providing information about the structure, features, prerequisites, compilation, maintainers, and license of this repository.
- LICENSE: The file containing the license terms defining how the repository can be used, shared, and modified.

## Features

- **Customizable page layout:** Allows easy customization of page margin and page size using the `geometry` package.

- **Essential mathematical environments:** Includes `amsmath`, `amssymb`, and `amsthm` packages for comprehensive mathematical typesetting, formulas, symbols, and theorem environments.

- **Predefined theorem styles:** Provides ready-to-use environments for `definition`, `axiom`, `theorem`, `corollary`, `lemma`, `proposition`, `example`, `exercise`, and `remark`.

- **Graphics support:** Embeds images using the `graphicx` package and creates vector graphics directly within LaTeX using the `tikz` package.

- **Indexing support:** Generates index entries using the `makeidx` package.

- **Clickable hyperlinks:** Creates clickable table of contents, references, index entries, URLs and more via the `hyperref` package.

- **High compatibility:** Works with standard LaTeX distributions like TeX Live across different operating systems and editors[^highCompatibility].

[^highCompatibility]: Tested with TeX Live + VS Code + LaTeX Workshop on Windows, and VerbTeX on Android.

## Prerequisites

A working LaTeX distribution (TeX Live, and etc.).

## Compilation

Clone or download the repository.

**(Recommended)** If you are using a LaTeX editor (like TeXstudio or Visual Studio Code with LaTeX Workshop), you can compile directly from the editor.

If you prefer to compile using the terminal or command prompt:

1. Navigate to the project directory:

    ```bash
    cd /your project directory
    ```

2.  Compile using one of these methods:

    **Recommended (`latexmk`):** The easiest and most reliable way to compile is using `latexmk` by executing:

    ```bash
    latexmk -pdf main.tex
    ```

    **Manual compilation:** If you need to compile manually, you can execute the following commands in sequence:

    ```bash
    pdflatex main.tex # First LaTeX compilation
    bibtex main.aux # Generate bibliography (if using BibTeX)
    makeindex main.idx # Generate index (if using index entries)
    pdflatex main.tex # Second LaTeX compilation (for cross-references)
    pdflatex main.tex # Third LaTeX compilation (for final output)
    ```

## Maintainers

- [@skrb-chisato](https://github.com/skrb-chisato)

## License

This repository is using [The Unlicense](https://github.com/skrb-chisato/plain_mathematics_book/blob/main/LICENSE).
