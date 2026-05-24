# Do AI-Assisted Projects Write Better Code? An Empirical Study on Internal Quality of Real-World GitHub Repositorie


This repository serves as the official replication package for our empirical study evaluating and comparing the maintainability and structural code quality of AI-generated versus Human-written software projects. 

The study systematically evaluates codebases across:
* **4 Programming Languages:** Java, Python, JavaScript, and TypeScript.
* **4 Project Scales:** Small, MedSmall, Medium, and Large.
* **16 Maintainability Categories (C1–C16):** Mapped directly from standard static analysis profiles.
* **5 Issue Severity Levels:** Info, Minor, Major, Critical, and Blocker.

---

## 1. Repository Directory Structure

The directory tree below maps the core data assets directly to the methodology and Research Questions (RQs) discussed in our study:

```text
.
├── dataset/
│   ├── Maintainability issues corresponding to each project.xlsx
│   └── merged_repository_with_sonar_keys.xlsx
├── RQ1 experimental results/
│   ├── ALL_Mann_Whitney_Results.xlsx
│   ├── heatmap.png
│   ├── sonarqube_Default_maintainability_rules.xlsx
│   └── The number of corresponding rules for each category c.xlsx
├── RQ2 experimental results/
│   ├── Average of various languages and scales Issue Density.xlsx
│   └── matrix_plot_bold.png
├── RQ3 experimental results/
│   ├── [Variables Datasets]
│   └── [PLS Results Files]
└── README.md
