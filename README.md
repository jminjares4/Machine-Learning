# Machine Learning (AI391L)

Coursework for AI391L Machine Learning, UT Austin MSAI.

## Setup

Requires Python 3 and VS Code with the Python and Jupyter extensions. Building the theory write-ups from source also requires a LaTeX distribution (TeX Live, MacTeX, or MiKTeX).

```bash
python3 -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate

pip install --upgrade pip
pip install -r requirements.txt
```

In VS Code: `Cmd+Shift+P` → **Python: Select Interpreter** → select `.venv/bin/python`. Then open the notebook, click the kernel selector in the top right, and choose the same environment.

## Contents

```
.
├── Homework_0/
│   ├── HW0.ipynb
│   └── hw0_programming_handout-1.pdf
├── Homework_1/
│   ├── programming/
│   │   ├── hw1_programming_base_notebook.ipynb
│   │   ├── hw1_programming_base_notebook.pdf
│   │   └── hw1_programming_handout.pdf
│   └── theory/
│       ├── hw1_theory_handout.pdf
│       ├── hw1_theory.tex
│       └── hw1_theory.pdf
├── requirements.txt
└── README.md
```

Each assignment folder holds the instructor handouts alongside the submitted work. From Homework 1 on, assignments split into a `programming/` half (Jupyter notebook, exported to PDF for submission) and a `theory/` half (LaTeX source and its compiled PDF).

### Homework 0

Environment setup and an introduction to the Python data stack. Uses the breast cancer dataset from `sklearn.datasets` to practice loading data into a DataFrame, inspecting its shape, and visualizing feature relationships with scatterplots and pairwise plots.

### Homework 1

- **programming/** — `hw1_programming_base_notebook.ipynb` is the working notebook, with `hw1_programming_base_notebook.pdf` as the exported submission copy. `hw1_programming_handout.pdf` is the instructions.
- **theory/** — `hw1_theory.tex` holds the written derivations; `hw1_theory.pdf` is the compiled output. `hw1_theory_handout.pdf` is the problem set.

Compile the theory write-up with:

```bash
cd Homework_1/theory
pdflatex hw1_theory.tex
```

## Dependencies

| Package | Purpose |
|---|---|
| jupyter | Notebook environment |
| scikit-learn | Machine learning models and datasets |
| pandas | Data manipulation |
| matplotlib | Plotting |
| seaborn | Statistical visualization |

`numpy` and `scipy` install automatically as dependencies.

## Notes

Notebooks can also be run in [Google Colab](https://colab.research.google.com/) with no local setup.

## Troubleshooting

**Imports fail in a notebook but work in the terminal** — the kernel is pointing at the wrong environment. Run `import sys; print(sys.executable)` in a cell and reselect the kernel if it isn't the `.venv` path.

**Newly installed packages aren't found** — restart the kernel (⟳ in the notebook toolbar).

**`.venv` doesn't appear in the kernel list** — reload the window (`Cmd+Shift+P` → **Developer: Reload Window**). Confirm VS Code is opened at the repo root, not a parent or subfolder.

**`pdflatex` not found** — install a LaTeX distribution, or compile `hw1_theory.tex` in [Overleaf](https://www.overleaf.com/) instead.