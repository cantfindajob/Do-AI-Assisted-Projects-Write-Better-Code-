# Do AI-Assisted Projects Write Better Code? An Empirical Study on Internal Quality of Real-World GitHub Repositorie
This repository contains the dataset and experimental results for our comparative empirical study evaluating the code quality and maintainability of AI-generated versus Human-written code. The study analyzes projects across four programming languages (Java, Python, JavaScript, TypeScript) and four distinct project scales (Small, MedSmall, Medium, Large) using SonarQube static analysis.

## Repository Structure

The directory structure of this repository maps directly to the core components and evaluation sections of our study:

```text
├── dataset/
│   ├── Maintainability issues corresponding to each project.xlsx
│   └── merged_repository_with_sonar_keys.xlsx
├── RQ1 experimental results/
│   ├── [Category Issue Density Files]
│   ├── ALL_Mann_Whitney_Results.xlsx
│   ├── heatmap.png
│   ├── sonarqube_Default_maintainability_rules.xlsx
│   └── The number of corresponding rules for each category c.xlsx
├── RQ2 experimental results/
│   ├── [Severity Density Files]
│   ├── Average of various languages and scales Issue Density.xlsx
│   └── matrix_plot_bold.png
├── RQ3 experimental results/
│   ├── [Variables Datasets]
│   └── [PLS Results Files]
└── README.md
This repository contains the dataset and experimental results for our comparative empirical study evaluating the code quality and maintainability of AI-generated versus Human-written code. The study analyzes projects across four programming languages (Java, Python, JavaScript, TypeScript) and four distinct project scales (Small, MedSmall, Medium, Large) using SonarQube static analysis.

## Repository Structure

### `dataset/`
* **`Maintainability issues corresponding to each project.xlsx`**: Contains the raw maintainability issues and their corresponding severity levels identified across all analyzed projects.
* **`merged_repository_with_sonar_keys.xlsx`**: A mapping file linking repository names, general keys, and the specific SonarQube Project Keys used within the SonarQube platform.

### `RQ1 experimental results/`
This directory contains data and visualizations addressing Research Question 1, focusing on 16 specific maintainability categories (C1–C16). 

* **Category Issue Density Files**: Data detailing the issue density for categories C1-C16 across all language and scale combinations. *Note: Issue Density is normalized across the study as (Total Violations in Category / NCLOC) * 1000.*
* **`ALL_Mann_Whitney_Results.xlsx`**: Statistical output containing the results of the 256 Mann-Whitney U tests comparing AI and Human project baselines.
* **`heatmap.png`**: A comparative heatmap visualization illustrating the issue density differences between AI and Human projects across the C1-C16 categories, partitioned by language and scale.
* **`sonarqube_Default_maintainability_rules.xlsx`**: The default SonarQube maintainability rule sets utilized for the static analysis of TypeScript, Python, JavaScript, and Java codebases.
* **`The number of corresponding rules for each category c.xlsx`**: A mapping document showing the relationship and count of specific SonarQube rules assigned to each of the C1-C16 conceptual categories.

### `RQ2 experimental results/`
This directory addresses Research Question 2, focusing on the distribution and density of issue severity.

* **Severity Density Files**: Files detailing the issue density across 5 distinct SonarQube severity levels for all evaluated scales, languages, and specific project keys.
* **`Average of various languages and scales Issue Density.xlsx`**: The aggregated average issue density for the five severity levels, providing a high-level summary across all language and scale variables.
* **`matrix_plot_bold.png`**: A visualization matrix plotting the severity issue density results for comparative analysis.

### `RQ3 experimental results/`
This directory contains the underlying data and modeling outputs related to Research Question 3.

* **Variables Datasets**: Contains the raw data files for the independent and dependent variables evaluated in this phase of the study.
* **PLS Results Files**: Contains the resultant data outputs from the Partial Least Squares (PLS) modeling.
