# Supplementary Material C — Monte Carlo analysis notebook

**Paper:** *Durability, not logistics, determines the climate benefit of jeans repair*

**Journal:** *Sustainable Production and Consumption*

**Authors:** [Author list — update before publishing]

**DOI:** [Add DOI once available]

---

## Overview

This Jupyter notebook reproduces all figures and statistical analyses reported in the paper.
It reads the frozen Monte Carlo simulation data (Supplementary Material B) and generates:

| Section | Output | Paper reference |
|---------|--------|-----------------|
| Forest chart | `figures/Figure 2 - Forest_emissions_per_pair.{png,pdf}` | Figure 2 |
| Scenario comparison | `figures/Figure 3 - Scenario_comparison.{png,pdf}` | Figure 3 |
| Break-even distance | `figures/Figure 6 - Break_even_forest.{png,pdf}` | Figure 6 |
| Spearman tornado chart | `figures/Figure 3 - Spearman_tornado.{png,pdf}` | Figure 4 |
| Spearman heatmap | `figures/Figure A1 - Spearman_heatmap_filtered.{png,pdf}` | Supporting Material A Figure A1 |
| Driver scatter plots | `figures/spearman_scatter.{png,pdf}` | Extra figures not refered in the main text or Supporting Material A |
| Driver explanation (L₀, E_prod) | `figures/driver_explanation_L0_Eprod.{png,pdf}` | Figure 5 |
| Driver mechanism panels | `figures/driver_plots/driver_*.png` | Extra figures not refered in the main text or Supporting Material A |
| Spearman results | `results/spearman_results.xlsx` | Table for documentation |

> **Update the figure/table numbers** in this table to match the final manuscript before publishing.

## Repository structure

```
├── README.md                  ← This file
├── requirements.txt           ← Python dependencies (pinned versions)
├── LICENSE                    ← License file (choose one — see below)
├── .gitignore
├── data/
│   └── Climate_calculations_MC_runs_frozen_260227.xlsx   ← Supplementary Material B
├── MC_analysis_paper.ipynb    ← Main analysis notebook (this supplementary material)
├── figures/                   ← Generated figures (created by the notebook)
└── results/                   ← Generated tables (created by the notebook)
```

## Quick start

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Download the data

Place the Monte Carlo workbook (`Supplementary Material B.xlsx`,
Supplementary Material B) into the `data/` directory. If the file is included in
this repository, this step is already done.

### 3. Set up the Python environment

We recommend using a virtual environment to avoid dependency conflicts:

```bash
python -m venv venv
source venv/bin/activate        # Linux / macOS
# venv\Scripts\activate         # Windows

pip install -r requirements.txt
```

### 4. Run the notebook

```bash
jupyter notebook MC_analysis_paper.ipynb
```

Run all cells sequentially (Cell → Run All). Figures are saved to `figures/`
and tabular results to `results/`.

## Software versions

The analysis was developed and tested with:

- Python 3.11
- pandas 2.2
- numpy 1.26
- scipy 1.13
- matplotlib 3.9
- seaborn 0.13
- openpyxl 3.1

See `requirements.txt` for exact pinned versions.

## Data description

The workbook (`data/Supplementary Material B.xlsx`) contains
two sheets used by the notebook:

- **`MC_runs`** — 1,000 Monte Carlo iterations with all stochastic input
  parameters and computed functional-unit emissions for 18 repair sub-scenarios
  plus the linear baseline. Row 9 contains column headers; row 10 contains units.
- **`MC_break_even`** — Pre-computed break-even distance statistics (median,
  P5, P95) for each transport leg and scenario combination.

## License

- **CC BY 4.0** — common for data and non-software academic outputs

## Citation

If you use this code or data, please cite:

```bibtex
@article{AuthorYear,
  title   = {Durability, not logistics, determines the climate benefit of jeans repair},
  author  = {[Authors]},
  journal = {Sustainable Production and Consumption},
  year    = {2026},
  doi     = {[DOI]}
}
```


