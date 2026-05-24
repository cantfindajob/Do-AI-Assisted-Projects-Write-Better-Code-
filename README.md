# Do AI-Assisted Projects Write Better Code? An Empirical Study on Maintainability

> An empirical study investigating whether AI-assisted open-source projects produce more maintainable code than human-written projects, analyzed across four programming languages, four project scales, and three research questions.

---

## 📁 Repository Structure

```
Do-AI-Assisted-Projects-Write-Better-Code/
│
├── dataset/
│   ├── Maintainability issues corresponding to each project.xlsx
│   └── merged_repository_with_sonar_keys.xlsx
│
├── RQ1 experimental results/
│   ├── [small / small-to-medium / medium / large]/
│   │   ├── typescript/
│   │   ├── python/
│   │   ├── javascript/
│   │   └── java/
│   │       └── (C1–C16 maintainability issue density per SonarQube project key)
│   ├── ALL_Mann_Whitney_Results.xlsx
│   ├── heatmap.png
│   ├── sonarqube_Default_maintainability_rules.xlsx
│   └── The number of corresponding rules for each category c.xlsx
│
├── RQ2 experimental results/
│   ├── [small / small-to-medium / medium / large]/
│   │   ├── typescript/
│   │   ├── python/
│   │   ├── javascript/
│   │   └── java/
│   │       └── (5 severity levels issue density per SonarQube project key)
│   ├── Average of various languages and scales Issue Density.xlsx
│   └── matrix_plot_bold.png
│
├── RQ3 experimental results/
│   ├── rq3.1.xlsx
│   ├── rq3.2.xlsx
│   └── (PLS analysis result files)
│
└── README.md
```

---

## 📊 Dataset

Located in the `dataset/` folder:

| File | Description |
|------|-------------|
| `Maintainability issues corresponding to each project.xlsx` | All maintainability issues and their severity levels for each analyzed project |
| `merged_repository_with_sonar_keys.xlsx` | Mapping of repository name, GitHub key, and SonarQube project key used for static analysis |

---

## 🔬 Research Questions

### RQ1: Maintainability Issue Density Analysis.

The `RQ1 experimental results/` folder contains maintainability issue density data organized by:

- **4 Project Scales**: Small, Small-to-Medium, Medium, Large
- **4 Programming Languages**: TypeScript, Python, JavaScript, Java
- **16 Maintainability Categories**: C1–C16 (mapped from SonarQube default rule sets)

**Key files:**

| File | Description |
|------|-------------|
| Per-language/scale folders | Issue density per C1–C16 category for each SonarQube project key |
| `ALL_Mann_Whitney_Results.xlsx` | Results of 256 pairwise Mann–Whitney U tests comparing AI vs. Human projects |
| `heatmap.png` | Heatmap visualization of C1–C16 maintainability issue density across languages and scales for AI vs. Human projects |
| `sonarqube_Default_maintainability_rules.xlsx` | Default SonarQube maintainability rule sets for TypeScript, Python, JavaScript, and Java |
| `The number of corresponding rules for each category c.xlsx` | Mapping of project rules to the C1–C16 category taxonomy (Table 1) |

---

### RQ2 — RQ2:Issue Severity Density and Remediation Time Analysis.

The `RQ2 experimental results/` folder contains severity-level issue density data organized by:

- **4 Project Scales**: Small, Small-to-Medium, Medium, Large
- **4 Programming Languages**: TypeScript, Python, JavaScript, Java
- **5 Severity Levels**: (e.g., Info, Minor, Major, Critical, Blocker)

**Key files:**

| File | Description |
|------|-------------|
| Per-language/scale folders | Issue density per severity level for each SonarQube project key |
| `Average of various languages and scales Issue Density.xlsx` | Average severity-level issue density matrix across all languages and scales |
| `matrix_plot_bold.png` | Matrix visualization of average severity issue density across scales and languages |

---

### RQ3: Driver Analysis via PLS Regression.

The `RQ3 experimental results/` folder contains data and model outputs for a Partial Least Squares (PLS) analysis examining the relationship between project-level factors and maintainability outcomes.

| File | Description |
|------|-------------|
| `rq3.1.xlsx` | Independent variables (project characteristics / predictors) |
| `rq3.2.xlsx` | Dependent variables (maintainability issue density outcomes) |
| PLS result files | Output of two PLS regression models |

---

## 🛠️ Tools & Methods

- **Static Analysis**: [SonarQube](https://www.sonarqube.org/) — default rule sets for TypeScript, Python, JavaScript, and Java
- **Statistical Testing**: Mann–Whitney U test (non-parametric, 256 pairwise comparisons in RQ1)
- **Modeling**: Partial Least Squares (PLS) regression for RQ3
- **Visualization**: Heatmaps and matrix plots for RQ1 and RQ2

---



---

## 📬 Contact

For questions or collaboration, please open an [issue](https://github.com/cantfindajob/Do-AI-Assisted-Projects-Write-Better-Code-/issues) on this repository.
