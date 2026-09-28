# MDS DSCI 521 Milestone 3 -- Palmer Penguins Quarto Website

This repository contains a multi-language Quarto website analyzing the `palmerpenguins` dataset using **R**, **Python**, and a polyglot integration with **Reticulate**.

---

## 🛠️ Prerequisites

Before getting started, make sure you have the following installed on your system:

1. **Quarto CLI** (v1.3+ recommended): [Download Quarto](https://quarto.org/docs/get-started/)
2. **R** (v4.0+ recommended): [Download R](https://cloud.r-project.org/)
3. **Python** (v3.8+ recommended): [Download Python](https://www.python.org/downloads/)
4. **Git**: [Download Git](https://git-scm.com/)

---

## 🚀 Quickstart Guide

Follow these step-by-step instructions to clone the repository, set up your development environments, and preview the site locally.

### 1. Clone the Repository

Open your terminal or command prompt and clone this repository:

```bash
git https://github.com/lymine1996/lymine_milestone_3.github.io.git
cd lymine_milestone_3.github.io
```

---

### 2. Set Up the R Environment (`renv`)

This project uses `renv` to manage R package dependencies reproducibly. Run the restore command to install all required R packages (`knitr`, `rmarkdown`, `tidyverse`, `palmerpenguins`, `reticulate`, etc.):

**Using Terminal / PowerShell:**

```bash
Rscript -e "renv::restore()"
```

*Alternatively, open R in the project root and run:*

```r
renv::restore()
```

### 3. Set Up the Python Environment (`uv`)

This project uses `uv` for fast, reproducible Python environment management. 

To create the virtual environment and synchronize all required dependencies (`jupyter`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `palmerpenguins`), run:

```bash
uv sync
```

---

## 🔨 Building / Rendering Static Files

To render the static HTML files into the `_site/` directory (e.g., for production deployment):

```bash
uv run quarto render
```
---

### 4. Render and Preview the Website

Once both environments are configured, you can build and serve the Quarto website locally with live reloading:

```bash
quarto preview
```

This will automatically start a local development server (usually at `http://localhost:4200`) and open the website in your default web browser. Any changes made to `.qmd` files will trigger an automatic preview rebuild.

---

## 📁 Repository Structure

```text
├── _quarto.yml               # Main Quarto site configuration
├── .gitignore                # Git ignore rules for build artifacts & temp files
├── renv.lock                 # R package dependency lockfile
├── renv/                     # R environment directory
├── posts/
│   ├── python-post/
│   │   └── index.qmd         # Python analysis post
│   ├── r-post/
│   │   └── index.qmd         # R analysis post
│   └── combined-post/
│       └── index.qmd         # Combined R & Python (reticulate) post
└── README.md                 # Project documentation
```

---

## 📊 Dataset Attribution

The dataset used across this project is the **palmerpenguins** dataset:
* **Authors**: Dr. Kristen Gorman and the Palmer Station, Antarctica LTER.
* **Official Site**: [https://allisonhorst.github.io/palmerpenguins/](https://allisonhorst.github.io/palmerpenguins/)