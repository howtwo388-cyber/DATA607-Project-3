DATA607 Project 3: Most Valued Data Science Skills

## Project Overview

This project examines the technical skills most valued in the artificial intelligence job market. It uses job-posting data to study how frequently technical skills are requested and how skill requirements relate to salaries, job categories, and experience levels.

This is an individual project completed by **Patricio Romero**, as permitted by the instructor.

## Research Questions

1. Which technical skills are most frequently requested?
2. Which skills are associated with higher salaries?
3. How do skill requirements vary across job categories?
4. How does experience level relate to salary?

## Data Source

The project uses the **AI Jobs Market 2025–2026 | Salaries** dataset from Kaggle:

[AI Jobs Market 2025–2026 | Salaries](https://www.kaggle.com/datasets/alitaqishah/ai-jobs-market-2025-2026-salaries)

The dataset contains 1,500 AI-related job postings with information about job titles, categories, required skills, experience levels, salaries, locations, industries, and other employment characteristics.

## Database Structure

The data is stored in a normalized PostgreSQL database named `data607_project3`. The database contains four related tables:

- **Job Categories:** 12 job categories.
- **Job Postings:** 1,500 job records.
- **Skills:** 93 unique technical skills.
- **Job Skills:** 9,428 relationships between job postings and required skills.

The Job Skills table serves as a bridge between Job Postings and Skills, resolving their many-to-many relationship and reducing duplicated skill information.

## Tools

- **RStudio and Quarto:** analysis and project documentation.
- **PostgreSQL:** relational data storage.
- **pgAdmin 4:** database administration.
- **GitHub:** version control, code sharing, and project documentation.

## Repository Contents

- `DATA607-Project-3-Data-Science-Skills.qmd` — Quarto source document for the Project 3 Approach.
- `DATA607-Project-3-Data-Science-Skills.html` — self-contained rendered report.
- `load_project3_database.R` — R script used to prepare and load the normalized PostgreSQL tables.
- `data/ai_jobs_market_2025_2026.csv` — source dataset used in the project.
- `_quarto.yml` — Quarto project configuration.

## Viewing the Report

Download and open `DATA607-Project-3-Data-Science-Skills.html` in a web browser. The HTML file is self-contained and does not require additional folders or supporting files.

## Reproducing the Approach

The Quarto document requires R with the `DBI`, `RPostgres`, and `knitr` packages. A local PostgreSQL connection can be used to reproduce the live database verification. The report also preserves the verified table structure and record counts when that local connection is unavailable.

To render the report from RStudio, open `DATA607-Project-3-Data-Science-Skills.qmd` and select **Render**.

## Project Status

The Approach phase is complete. It documents the research questions, data source, loading strategy, normalized database design, database relationships, and planned analysis. The next phase will develop the complete analysis, visualizations, findings, and presentation video.

## Author

**Patricio Romero**  
DATA607 — Data Acquisition and Management
