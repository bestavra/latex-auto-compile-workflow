# latex-auto-compile-workflow

This repository provides an automated GitHub Actions workflow for building LaTeX projects using the [xu-cheng/latex-action](https://github.com/xu-cheng/latex-action.git). It automates the process of compiling LaTeX `.tex` files into PDFs and managing the output within your repository.

## Folder Structure

The workflow is designed to work with the following folder structure:
```
.
├── docs
│   ├── doc1.pdf
│   ├── doc2.pdf
│   └── doc3.pdf
└── src
    ├── doc1
    │   └── main.tex
    ├── doc2
    │   └── main.tex
    └── doc3
        └── main.tex
```

- The **`src`** folder contains subfolders (e.g., `doc1`, `doc2`, `doc3`), each containing a `main.tex` file. These are the LaTeX files that will be compiled.
- The **`docs`** folder will contain the generated PDFs. Each PDF will be named after its respective folder in `src` (e.g., `doc1.pdf`, `doc2.pdf`).

## How It Works:
   - Only the `main.tex` files are compiled.
   - Each `main.tex` file must be placed inside its own folder in the `src` directory.
   - The generated PDF will be named after the folder in which the `main.tex` file resides (e.g., the `main.tex` in the `doc1` folder will produce `doc1.pdf`).
   - The PDF will be placed in the `docs` folder, which will be automatically created if it does not exist.

> **_NOTE_** The workflow only compiles LaTeX files that have been changed in the latest commit, ensuring faster builds by avoiding unnecessary recompilation.
