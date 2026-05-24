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
2. Comprehensive Component Details📂 dataset/This directory contains the foundational dataset mapping and raw static analysis outputs before multi-dimensional grouping.Maintainability issues corresponding to each project.xlsx: Houses the granular, row-level code maintainability issues identified by SonarQube across all sampled projects, alongside their designated severities.merged_repository_with_sonar_keys.xlsx: Serves as the master index file linking GitHub repository names, generalized identifiers, and the exact project keys generated for the SonarQube platform instances.📂 RQ1 experimental results/Contains the analytical outputs and statistical tests designed for Research Question 1 (RQ1), which investigates the density differences across 16 distinct maintainability categories (C1–C16).Metric Definition: Issue Density throughout this study is strictly normalized per thousand non-comment lines of code using the following formula:$$\text{Issue Density} = \left( \frac{\text{Total Violations in Category}}{\text{NCLOC}} \right) \times 1000$$ALL_Mann_Whitney_Results.xlsx: Contains the complete statistical output of the 256 distinct Mann-Whitney U test groups comparing the AI-generated code baseline against the Human-written baseline.heatmap.png: A 4×4 grouped matrix heatmap showing the comparative distribution of issue density for categories C1–C16, stratified by programming language and project scale.sonarqube_Default_maintainability_rules.xlsx: Documents the exact, unaltered default SonarQube profile quality gates and rule specifications applied to Java, Python, JavaScript, and TypeScript.The number of corresponding rules for each category c.xlsx: Provides an explicit mapping matrix that classifies individual technical SonarQube rules into the high-level conceptual categories (C1–C16) utilized in the paper.📂 RQ2 experimental results/Contains data assets associated with Research Question 2 (RQ2), which shifts the analytical focus from thematic issue categories to the structural impact categorized by issue severity profiles.Average of various languages and scales Issue Density.xlsx: Summarizes the mean issue density values for each of the 5 severity categories across the matrix of scales and languages, facilitating an aggregate comparison of AI vs. Human profiles.matrix_plot_bold.png: A high-resolution graphical matrix plot illustrating the distribution of severe issue types across the experimental groups.📂 RQ3 experimental results/Contains the empirical assets supporting Research Question 3 (RQ3), which models the structural paths and interactions between project attributes, code generation sources, and code quality outcomes.Variables Datasets: Data matrices containing the operationalized independent and dependent variables computed for each subject project in the sample.PLS Results Files: Statistical reporting sheets outlining the outer weights, loadings, path coefficients, and model fit criteria derived from the Partial Least Squares (PLS) modeling phase.3. Methodological & Analytical SetupTo replicate the statistical evaluations presented in the manuscript, the following scientific methodologies were applied:Non-parametric Significance Testing: Because the issue density counts exhibit non-normal distributions, the two-tailed Mann-Whitney U test was performed at $\alpha = 0.05$.Effect Size Estimation: Cliff's Delta ($\delta$) was utilized to quantify the magnitude of differences between the AI and Human distributions.Structural Equation Modeling: Partial Least Squares Path Modeling (PLS-PM) was performed to explore structural mediation effects.4. Software & Replication RequirementsThe analytical pipeline can be re-run using standard Python environments.Data Analysis DependenciesEnsure you have Python 3.10+ installed with the following scientific packages:
