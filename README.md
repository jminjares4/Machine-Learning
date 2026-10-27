
# Machine Learning (AI391L)

Coursework for **AI391L: Machine Learning** in the **M.S. in Artificial Intelligence** program at **The University of Texas at Austin**.

This repository contains programming assignments, Jupyter notebooks, theoretical derivations, and LaTeX write-ups.

## Assignments

| Homework | Programming | Theory |
|---|---|---|
| [Homework 0](Homework_0/) | [Notebook](Homework_0/HW0.ipynb) | — |
| [Homework 1](Homework_1/) | [Notebook](Homework_1/programming/hw1_programming_base_notebook.ipynb) | [PDF](Homework_1/theory/hw1_theory.pdf) · [LaTeX](Homework_1/theory/hw1_theory.tex) |
| [Homework 2](Homework_2/) | [Notebook](Homework_2/programming/hw2_programming_base_notebook.ipynb) | [PDF](Homework_2/theory/hw2_theory.pdf) · [LaTeX](Homework_2/theory/hw2_theory.tex) |
| [Homework 3](Homework_3/) | [Notebook](Homework_3/programming/hw3_programming_base_notebook.ipynb) | [PDF](Homework_3/theory/hw3_theory.pdf) · [LaTeX](Homework_3/theory/hw3_theory.tex) |
| [Homework 4](Homework_4/) | — | [PDF](Homework_4/theory/hw4_theory.pdf) · [LaTeX](Homework_4/theory/hw4_theory.tex) |
| [Homework 5](Homework_5/) | [Notebook](Homework_5/programming/hw5_programming_base_notebook.ipynb) | [PDF](Homework_5/theory/hw5_theory.pdf) · [LaTeX](Homework_5/theory/hw5_theory.tex) |
## Repository Structure

```text
.
├── Homework_0/
├── Homework_1/
├── Homework_2/
├── Homework_3/
├── Homework_4/
├── Homework_5/
├── README.md
└── requirements.txt
```

Assignments are organized into `programming/` and `theory/` directories where applicable.

- **Programming:** Jupyter notebooks, assignment handouts, and PDF exports.
- **Theory:** Problem statements, LaTeX source files, and compiled PDFs.

## Setup

Requires Python 3 and VS Code with the Python and Jupyter extensions. Compiling theory assignments requires a LaTeX distribution such as TeX Live, MacTeX, or MiKTeX.

### Install Dependencies

```bash
python3 -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### Run Notebooks

Open the repository in VS Code, select the `.venv` Python interpreter, and choose the same environment as the Jupyter kernel.

Notebooks can also be run in [Google Colab](https://colab.research.google.com/).

### Compile Theory Assignments

For example, to compile Homework 4:

```bash
cd Homework_4/theory
pdflatex hw4_theory.tex
```

## Troubleshooting

- **Import errors:** Verify the notebook uses the correct Python kernel with `import sys; print(sys.executable)`.
- **Missing packages:** Restart the Jupyter kernel after installation.
- **Environment not detected:** Reload VS Code and reselect the Python interpreter.
- **LaTeX compilation errors:** Verify that `pdflatex` is installed or use [Overleaf](https://www.overleaf.com/).
