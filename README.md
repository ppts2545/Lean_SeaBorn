# Lean_SeaBorn

A practical Seaborn learning project for data analysis and teaching.

This repository is organized as a step-by-step visual analytics curriculum, from basic styling and single-variable plots to advanced multi-panel and regression visualizations.

## Project Goals
- Learn Seaborn chart types in a logical order.
- Build reusable plotting habits (theme, labels, readability, interpretation).
- Prepare notebook-based materials for self-study and classroom teaching.

## Repository Structure

```text
Lean_SeaBorn/
├── Data/
│   └── raws/
│       └── ComputerSales.csv
├── notebooks/
│   ├── Paleetes.ipynb
│   ├── styling.ipynb
│   ├── 01_Distribution-Plots/
│   │   ├── Distribution-Plots.ipynb
│   │   ├── Kde_Plot.ipynb
│   │   ├── Pair_Plot.ipynb
│   │   └── Rug_Plot.ipynb
│   ├── 02_Categorial-Plots/
│   │   ├── Bar_plots.ipynb
│   │   ├── Box_plots.ipynb
│   │   ├── Count_plots.ipynb
│   │   ├── Strip_plot.ipynb
│   │   ├── Swarm_plots.ipynb
│   │   └── Violin_plots.ipynb
│   ├── 03_Matrix Plots/
│   │   ├── Heat_Map.ipynb
│   │   └── Pivot_Table.ipynb
│   └── 04_Clustermap/
│       ├── Cluster_Map.ipynb
│       ├── FacetGrid.ipynb
│       ├── PairGrid.ipynb
│       ├── Regression_plots.ipynb
│       └── README.md
└── README.md
```

## Quick Start

### 1) Create and activate a Python environment

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 2) Install required libraries

```powershell
pip install seaborn matplotlib pandas numpy jupyter
```

### 3) Launch Jupyter

```powershell
jupyter notebook
```

Open notebooks in this order for best learning flow.

## Recommended Study Path

1. `notebooks/styling.ipynb`
2. `notebooks/Paleetes.ipynb`
3. `notebooks/01_Distribution-Plots/`
4. `notebooks/02_Categorial-Plots/`
5. `notebooks/03_Matrix Plots/`
6. `notebooks/04_Clustermap/`

## Module Guide

### Module 0: Styling and Palettes
- Files:
  - `notebooks/styling.ipynb`
  - `notebooks/Paleetes.ipynb`
- Focus:
  - Theme setup, context scaling, and color selection.
  - Building consistent visual style across notebooks.
- Why it matters:
  - Better readability, reproducibility, and cleaner teaching material.

### Module 1: Distribution Plots
- Folder: `notebooks/01_Distribution-Plots/`
- Files:
  - `Distribution-Plots.ipynb`
  - `Kde_Plot.ipynb`
  - `Pair_Plot.ipynb`
  - `Rug_Plot.ipynb`

Use for:
- Understanding single-variable shape and spread.
- Checking skewness, modality, and potential outliers.

Benefits:
- Fast first look at numerical variables.
- Useful before modeling or hypothesis testing.

Drawbacks:
- Can hide subgroup differences if categories are mixed together.
- Interpretation depends on bin width / KDE bandwidth.

Best-fit data:
- Continuous numeric variables.
- Moderate to large sample sizes for stable density patterns.

### Module 2: Categorical Plots
- Folder: `notebooks/02_Categorial-Plots/`
- Files:
  - `Bar_plots.ipynb`
  - `Box_plots.ipynb`
  - `Count_plots.ipynb`
  - `Strip_plot.ipynb`
  - `Swarm_plots.ipynb`
  - `Violin_plots.ipynb`

Use for:
- Comparing groups by category.
- Showing central tendency, spread, and category frequencies.

Benefits:
- Easy for students to interpret.
- Excellent for business and reporting scenarios.

Drawbacks:
- Too many categories reduce readability.
- Some plot types can hide raw point-level variation.

Best-fit data:
- One or more categorical variables plus numeric target variables.

### Module 3: Matrix Plots
- Folder: `notebooks/03_Matrix Plots/`
- Files:
  - `Pivot_Table.ipynb`
  - `Heat_Map.ipynb`

Use for:
- Summarized, matrix-shaped relationships.
- Visual comparison across two dimensions.

Benefits:
- Very compact view of many values.
- Strong at spotting high/low regions and structure.

Drawbacks:
- Exact values can be hard to read without annotations.
- Bad scaling/color choices can mislead interpretation.

Best-fit data:
- Aggregated or pivoted tabular data.
- Correlation matrices or time/category grids.

### Module 4: Advanced Grids and Regression
- Folder: `notebooks/04_Clustermap/`
- Files:
  - `Cluster_Map.ipynb`
  - `FacetGrid.ipynb`
  - `PairGrid.ipynb`
  - `Regression_plots.ipynb`

Use for:
- Discovering hidden structure (clusters).
- Comparing patterns across many subsets.
- Exploring pairwise relationships at scale.
- Visualizing trend lines and uncertainty.

Benefits:
- High analytical depth.
- Great for advanced EDA and teaching interpretation skills.

Drawbacks:
- More complex to explain to beginners.
- Requires careful control of plot size, labels, and context.

Best-fit data:
- Multivariate datasets with enough samples per group.
- Numeric features (plus optional categorical grouping variables).

Detailed teaching notes for this module are in:
- `notebooks/04_Clustermap/README.md`

## Four Core Visualization Families (Teach-Ready Summary)

1. Distribution charts
- Main question: What does one variable look like?
- Typical charts: histogram, KDE, rug.
- Strength: fastest way to inspect shape.
- Limitation: weak for subgroup comparison.

2. Categorical comparison charts
- Main question: How do groups differ?
- Typical charts: bar, box, violin, count, strip, swarm.
- Strength: clear group-level comparisons.
- Limitation: clutter with too many categories.

3. Matrix charts
- Main question: How do values vary across row-column combinations?
- Typical charts: heatmap from pivot/correlation matrix.
- Strength: compact multivariate summary.
- Limitation: can hide detail at point level.

4. Advanced relationship charts
- Main question: What multivariate patterns and trends exist?
- Typical charts: clustermap, facetgrid, pairgrid, regression plots.
- Strength: deep exploration and pattern discovery.
- Limitation: higher interpretation complexity.

## Data Used

- Primary local file:
  - `Data/raws/ComputerSales.csv`
- Common Seaborn built-in datasets used in notebooks:
  - `tips`, `iris`, `flights`, `attention`

## Teaching Use Plan

Suggested 4-session classroom outline:

1. Session 1: Style + distribution basics
- Theme setup, palette selection, histogram/KDE interpretation.

2. Session 2: Categorical analysis
- Box/violin/count charts, choosing chart type by question.

3. Session 3: Matrix and pivot thinking
- Pivot tables, heatmaps, color scaling.

4. Session 4: Advanced EDA
- PairGrid, FacetGrid, Clustermap, lmplot storytelling.

Student deliverable idea:
- Pick one dataset and produce:
  - 1 distribution chart
  - 1 categorical chart
  - 1 matrix chart
  - 1 advanced relationship chart
- Add 2-3 interpretation bullets per chart.

## Good Notebook Practices

- Keep titles explicit: what, who, and timeframe.
- Always label axes with units when possible.
- Use consistent style/palette per notebook.
- Add short markdown interpretation under each major plot.
- Prefer readable figure sizes over dense default layouts.

## Troubleshooting

- Plot does not render:
  - Restart kernel and run cells from top.
- Seaborn dataset load fails:
  - Check internet connection or use local CSV data.
- Text/labels overlap:
  - Increase figure size, rotate ticks, use `tight_layout()`.

## Future Improvements

- Add exercises and answer keys for each module.
- Add one capstone notebook using `ComputerSales.csv` end-to-end.
- Add exported static images for quick preview in README.

## License / Usage

This project is intended for educational and training use.
If used in class, keep source attributions for external datasets and libraries.
