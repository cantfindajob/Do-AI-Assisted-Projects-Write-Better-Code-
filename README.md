# Maintainability Analysis of AI-Generated vs. Human-Written Code

This repository contains the datasets, experimental results, and analysis scripts supporting the empirical study on maintainability differences between AI-generated and human-written code across multiple programming languages and project scales.

---

## Repository Structure

```
├── dataset/
│   ├── Maintainability issues corresponding to each project.xlsx
│   └── merged_repository_with_sonar_keys.xlsx
├── RQ1 experimental results/
│   ├── <Language>_<Scale>/               (16 folders: 4 languages × 4 scales)
│   │   └── <SonarQube_Project_Key>.xlsx  (maintainability issue density per category)
│   ├── ALL_Mann_Whitney_Results.xlsx
│   ├── heatmap.png
│   ├── sonarqube_Default_maintainability_rules.xlsx
│   └── The number of corresponding rules for each category c.xlsx
├── RQ2 experimental results/
│   ├── <Language>_<Scale>/               (16 folders: 4 languages × 4 scales)
│   │   └── <SonarQube_Project_Key>.xlsx  (severity issue density per level)
│   ├── Average of various languages and scales Issue Density.xlsx
│   └── matrix_plot_bold.png
├── RQ3 experimental results/
│   ├── independent_dependent_variables.xlsx
│   └── pls_results.xlsx
└── README.md
```

---

## Dataset

The `dataset/` folder contains the foundational data used across all three research questions.

| File | Description |
|------|-------------|
| `Maintainability issues corresponding to each project.xlsx` | Lists all maintainability issues detected for each project, along with their corresponding severity levels. |
| `merged_repository_with_sonar_keys.xlsx` | Maps each repository to its repository name, key identifier, and SonarQube project key (used to reference the project within the SonarQube platform). |

---

## RQ1 — Maintainability Issue Density by Category

> **RQ1:** Do AI-generated and human-written projects differ in maintainability issue density across the 16 maintainability categories (C1–C16)?

The `RQ1 experimental results/` folder is organized into **16 sub-folders**, one for each combination of the 4 programming languages (Java, JavaScript, Python, TypeScript) and 4 project scales. Each sub-folder contains per-project maintainability issue density data grouped by the 16 SonarQube maintainability categories (C1–C16).

| File | Description |
|------|-------------|
| `<Language>_<Scale>/<SonarQube_Project_Key>.xlsx` | Maintainability issue density for each category (C1–C16) for a given project, language, and scale. |
| `ALL_Mann_Whitney_Results.xlsx` | Results of 256 pairwise Mann–Whitney U tests comparing AI-generated vs. human-written projects across all language–scale–category combinations. |
| `heatmap.png` | Heatmap visualizing average maintainability issue density (C1–C16) for AI-generated and human-written projects, broken down by language and scale. |
| `sonarqube_Default_maintainability_rules.xlsx` | The default SonarQube maintainability rule sets applied for TypeScript, Python, JavaScript, and Java. |
| `The number of corresponding rules for each category c.xlsx` | Maps the number of SonarQube rules associated with each of the 16 maintainability categories (C1–C16) as used in this study (corresponding to Table 1 in the paper). |

---

## RQ2 — Severity Issue Density by Level

> **RQ2:** Do AI-generated and human-written projects differ in issue density across the 5 severity levels?

The `RQ2 experimental results/` folder is organized into **16 sub-folders** (4 languages × 4 scales). Each sub-folder contains per-project issue density data for each of the 5 SonarQube severity levels (Info, Minor, Major, Critical, Blocker).

| File | Description |
|------|-------------|
| `<Language>_<Scale>/<SonarQube_Project_Key>.xlsx` | Severity issue density per level for each project, language, and scale. |
| `Average of various languages and scales Issue Density.xlsx` | Aggregated matrix of average severity issue density across all 5 levels, grouped by language and scale. |
| `matrix_plot_bold.png` | Matrix plot visualizing the averaged severity issue density results across all languages and scales. |

---

## RQ3 — Influencing Factors on Maintainability

> **RQ3:** What project-level factors (independent variables) significantly influence maintainability issue density (dependent variable) in AI-generated and human-written code?

The `RQ3 experimental results/` folder contains the input data and output results for the Partial Least Squares (PLS) regression analysis.

| File | Description |
|------|-------------|
| `independent_dependent_variables.xlsx` | Project-level independent variables (e.g., size, complexity, language) and dependent variables (maintainability issue density) used in the PLS models. |
| `pls_results.xlsx` | Results of the two PLS regression models (one for AI-generated projects, one for human-written projects), including path coefficients, R², and significance values. |

---

## Analysis Tools

- **Static Analysis:** [SonarQube](https://www.sonarqube.org/) — used to detect and classify maintainability issues across all projects.
- **Statistical Testing:** Mann–Whitney U test (non-parametric, two-sided) for RQ1 and RQ2 comparisons.
- **Regression Modeling:** Partial Least Squares (PLS) regression for RQ3 factor analysis.

---

## Languages and Scales

| Dimension | Values |
|-----------|--------|
| Programming Languages | Java, JavaScript, Python, TypeScript |
| Project Scales | 4 levels (Small, Medium, Large, Extra-Large) |
| Maintainability Categories | C1–C16 (see Table 1 in the paper) |
| Severity Levels | Info, Minor, Major, Critical, Blocker |

---

## Contact

For questions or collaboration, please open an issue or contact the repository owner.
