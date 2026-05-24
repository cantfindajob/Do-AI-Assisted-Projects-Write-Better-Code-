# Do AI-Assisted Projects Write Better Code? — Maintainability Analysis

> An empirical study examining whether AI-assisted software projects exhibit better code maintainability than human-written projects, using static analysis across four programming languages and multiple project scales.

---

## 📌 Repository Overview

This repository contains the dataset, experimental results, and analysis artifacts for the study:

**"Do AI-Assisted Projects Write Better Code? A Maintainability Perspective"**

We analyze maintainability issue density and severity across **AI-assisted** and **human-written** open-source projects using **SonarQube** static analysis, covering **4 programming languages**, **4 project scales**, **16 maintainability categories (C1–C16)**, and **5 severity levels**.

---

## 📁 Repository Structure

```
Do-AI-Assisted-Projects-Write-Better-Code-/
│
├── dataset/
│   ├── Maintainability issues corresponding to each project.xlsx
│   └── merged_repository_with_sonar_keys.xlsx
│
├── RQ1 experimental results/
│   ├── [Language]_[Scale]/                    # 16 folders (4 langs × 4 scales)
│   │   └── *.xlsx                             # C1–C16 issue density per project key
│   ├── ALL_Mann_Whitney_Results.xlsx
│   ├── heatmap.png
│   ├── sonarqube_Default_maintainability_rules.xlsx
│   └── The number of corresponding rules for each category c.xlsx
│
├── RQ2 experimental results/
│   ├── [Language]_[Scale]/                    # 16 folders (4 langs × 4 scales)
│   │   └── *.xlsx                             # 5 severity levels issue density per project
│   ├── Average of various languages and scales Issue Density.xlsx
│   ├── matrix_plot_bold.png
│   ├── Remediation Time.xlsx
│   └── Remediation Time.png
│
├── RQ3 experimental results/
│   ├── rq3.1.xlsx
│   ├── rq3.2.xlsx
│   ├── PLS result 1.xlsx
│   └── PLS result 2.xlsx
│
└── README.md
```

---

## 🗂️ Dataset Description

Located in `dataset/`

| File | Description |
|------|-------------|
| `Maintainability issues corresponding to each project.xlsx` | All projects with their corresponding maintainability issues and severity levels as detected by SonarQube |
| `merged_repository_with_sonar_keys.xlsx` | Maps each repository name, GitHub key, and SonarQube project key (used to identify projects in the SonarQube dashboard) |

---

## 🔬 Research Questions & Experimental Results

### RQ1: Maintainability Issue Density Analysis.

Located in `RQ1 experimental results/`

This RQ investigates maintainability issue density across **16 categories (C1–C16)** for each project, broken down by:

- **Languages:** TypeScript, Python, JavaScript, Java
- **Scales:** Small, Small-to-Medium, Medium, Large

| File / Folder | Description |
|---------------|-------------|
| `[Language]_[Scale]/` | 16 sub-folders containing per-project issue density data for each of the C1–C16 maintainability categories, indexed by SonarQube project key |
| `ALL_Mann_Whitney_Results.xlsx` | Results of **256 pairwise Mann-Whitney U tests** comparing AI vs. Human projects across all category × language × scale combinations |
| `heatmap.png` | Heatmap visualizing maintainability issue density for AI vs. Human projects across C1–C16 categories, all languages, and all scales |
| `sonarqube_Default_maintainability_rules.xlsx` | Default SonarQube maintainability rule sets for TypeScript, Python, JavaScript, and Java |
| `The number of corresponding rules for each category c.xlsx` | Mapping between C1–C16 categories and the number of applicable SonarQube rules used in this study (corresponds to Table 1 in the paper) |

**Maintainability Categories (C1–C16)** cover dimensions such as code duplication, complexity, naming conventions, documentation, and more, as defined by SonarQube's default rule taxonomy.

---

### RQ2:Issue Severity Density and Remediation Time Analysis.

Located in `RQ2 experimental results/`

This RQ examines **severity-level issue density** and **estimated remediation time** across:

- **Languages:** TypeScript, Python, JavaScript, Java
- **Scales:** Small, Small-to-Medium, Medium, Large
- **Severity Levels:** 5 levels (Blocker, Critical, Major, Minor, Info)

| File / Folder | Description |
|---------------|-------------|
| `[Language]_[Scale]/` | 16 sub-folders with per-project issue density data for each of the 5 severity levels, indexed by SonarQube project key |
| `Average of various languages and scales Issue Density.xlsx` | Average severity-level issue density matrix across all languages and scales |
| `matrix_plot_bold.png` | Visual matrix plot of average issue density per severity level, language, and scale |
| `Remediation Time.xlsx` | Estimated remediation time (technical debt) per project as reported by SonarQube |
| `Remediation Time.png` | Bar chart comparing average remediation time between AI-assisted and human-written projects across all languages and scales |

---

### RQ3: Driver Analysis via PLS Regression.

Located in `RQ3 experimental results/`

This RQ uses **Partial Least Squares (PLS)** regression to identify relationships between project characteristics (independent variables) and maintainability outcomes (dependent variables).

| File | Description |
|------|-------------|
| `rq3.1.xlsx` | The dependent variable is data on the problem density of 16 maintainability categories|
| `rq3.2.xlsx` | The dependent variable is data with a density of 5 severity issues |
| `Maintainability issue density pls-results.csv` | The PLS results corresponding to the rq3.1 file |
| `Severity issue density pls-results.xlsx` | The PLS results corresponding to the rq3.2 file |

---

## 🛠️ Tools & Environment

| Tool | Purpose |
|------|---------|
| [SonarQube](https://www.sonarqube.org/) | Static code analysis — maintainability issue detection |
| SonarQube Default Rules | TypeScript, Python, JavaScript, Java rule sets |
| Python / R | Statistical analysis (Mann-Whitney U test, PLS) |
| Excel / XLSX | Data storage and result presentation |

---

## 📊 Key Visualizations

**RQ1 — Issue Density Heatmap (AI vs. Human, C1–C16)**

> `RQ1 experimental results/heatmap.png`

Compares maintainability issue density between AI-assisted and human-written projects across 16 categories, 4 languages, and 4 project scales.

**RQ2 — Severity Density Matrix**

> `RQ2 experimental results/matrix_plot_bold.png`

Visual matrix of average issue density at each severity level per language and scale.

**RQ2 — Remediation Time Comparison**

> `RQ2 experimental results/Remediation Time.png`

Bar chart comparing average estimated fix time (technical debt) between AI and Human projects.

---

## 📬 Contact

For questions or collaboration, please open an issue in this repository or reach out via GitHub: [@cantfindajob](https://github.com/cantfindajob)

---

## 📄 License

This repository is for academic research purposes. Please cite this work if you use the dataset or results in your own research.
