# Stack Overflow Developer Survey 2025 Analysis

## Project Overview

This project analyzes the Stack Overflow Developer Survey 2025 data to uncover insights about developer careers, AI adoption, job satisfaction, and salary trends. The analysis follows the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology.

## Motivation

With AI tools becoming increasingly prevalent in software development, understanding how developers perceive and adopt these technologies is crucial. This project aims to answer:

1. **What factors predict whether a developer perceives AI as a threat to their job?**
2. **How does remote work arrangement affect job satisfaction?**
3. **What characteristics are associated with higher developer salaries?**
4. **What drives AI tool adoption among developers?**

## Libraries Used

- **pandas** (2.2.3) - Data manipulation and analysis
- **numpy** (1.26.4) - Numerical computing
- **scikit-learn** (1.5.2) - Machine learning models and evaluation
- **matplotlib** (3.10.3) - Data visualization
- **seaborn** (0.13.2) - Statistical data visualization

## Files in the Repository

| File | Description |
|------|-------------|
| `stackoverflow_analysis.ipynb` | Main Jupyter notebook containing all analysis, visualizations, and modeling |
| `survey_results_schema.csv` | Data dictionary describing survey questions and response options |
| `README.md` | Project documentation (this file) |

## Dataset

The analysis uses the **Stack Overflow Developer Survey 2025** dataset containing 53,921 responses from developers worldwide.

### Download Instructions

The main data file (`survey_results_public.csv`, ~135MB) is not included in this repository due to size constraints. To run the notebook:

1. Visit the [Stack Overflow Developer Survey](https://survey.stackoverflow.co/) page
2. Download the 2025 survey results (or latest available)
3. Extract the ZIP file
4. Place `survey_results_public.csv` in the same directory as the notebook

Alternatively, download directly from Stack Overflow's data archive.

## Summary of Results

### Key Findings

#### 1. AI Threat Perception
- Only **13% of developers** perceive AI as a threat to their job
- A Random Forest classifier achieved **83.7% accuracy** in predicting AI threat perception
- The most important predictors are: years of coding experience, work experience, and developer type
- Developers who use AI tools daily are **less likely** to see AI as a threat

#### 2. Remote Work and Job Satisfaction
- Job satisfaction is relatively consistent across remote work arrangements (mean ~6.5-7.0 on 0-10 scale)
- Remote work flexibility alone is not a major driver of job satisfaction
- Other factors like autonomy, compensation, and team collaboration matter more

#### 3. Salary Analysis (USD)
- Median salary for US developers: **$140,000**
- Mean salary: $146,866
- Salary range: $10,000 - $500,000 (filtered for outliers)
- Higher education levels correlate with higher salaries

#### 4. AI Tool Adoption
- The vast majority of developers now use AI tools
- Daily AI tool users represent the largest group
- AI adoption is consistent across age groups, with slightly higher rates among younger developers (18-24)

### Model Performance

| Metric | Value |
|--------|-------|
| Accuracy | 83.7% |
| Precision (No Threat) | 0.86 |
| Recall (No Threat) | 0.97 |
| F1-Score (No Threat) | 0.91 |

*Note: The model shows class imbalance effects, with lower performance on the minority class (threat perception).*

### Prediction Example

For a typical developer profile:
- Age: 25-34 years old
- Education: Bachelor's degree
- Remote work: Fully remote
- AI usage: Daily

**Prediction:** Does NOT see AI as a threat (90.3% confidence)

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/stackoverflow-survey-analysis.git
   cd stackoverflow-survey-analysis
   ```

2. Download the dataset (see [Dataset](#dataset) section above)

3. Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
   ```

4. Open and run the Jupyter notebook:
   ```bash
   jupyter notebook stackoverflow_analysis.ipynb
   ```

## Blog Post

Read the non-technical summary of findings: [Do Developers Fear AI? What 54,000 Programmers Told Us](https://medium.com/@mauriziopinto/do-developers-fear-ai-what-54-000-programmers-told-us-cedb1fcf0aaf)

## Acknowledgments

- **Stack Overflow** for providing the Developer Survey data
- **Udacity** Data Science Nanodegree program for project guidance
- Survey data source: [Stack Overflow Developer Survey 2025](https://survey.stackoverflow.co/2025/)

## License

This project is for educational purposes as part of the Udacity Data Science Nanodegree program. The Stack Overflow Developer Survey data is made available under the [Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/1.0/).
