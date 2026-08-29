# Machine Learning (AI391L)

Coursework for AI391L Machine Learning, UT Austin MSAI.

## Setup

Requires Python 3 and VS Code with the Python and Jupyter extensions.

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
├── requirements.txt
└── README.md
```

### Homework 0

Environment setup and an introduction to the Python data stack. Uses the breast cancer dataset from `sklearn.datasets` to practice loading data into a DataFrame, inspecting its shape, and visualizing feature relationships with scatterplots and pairwise plots.

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