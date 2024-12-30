# Propensity Score Matching: The Consequences of Child Soldiering

## Project Overview

This project analyzes data from the study by **Christopher Blattman and J. Annan (2010)**, *The Consequences of Child Soldiering* (Review of Economics and Statistics). The study focuses on the impact of forced military service on youth in war-affected regions of Uganda, specifically examining the effects of abduction by the Lord's Resistance Army (LRA) on various outcomes such as education, emotional distress, and wages.

## Data Description

The dataset contains information from a panel survey of male youth, including those who were abducted by the LRA and those who were not. Key variables include:

- **abd**: Whether the individual was abducted (treatment variable)
- **educ**: Years of education
- **distress**: Index of emotional distress (0-15)
- **logwage**: Log of average daily wage earned in the last 4 weeks
- **c_ach - c_pal**: Location indicators
- **age**: Age of the individual
- **fthr_ed**: Father's years of education
- **mthr_ed**: Mother's years of education
- **orphan96**: Indicator if the individual's parent died before 1996
- **hh_fthr_frm**: Indicator if father is a farmer
- **hh_size96**: Household size in 1996

## Methodology

In this project, we use **Propensity Score Matching (PSM)** to estimate the **Average Treatment Effect (ATE)** of abduction on education, distress, and wages. The steps include:

1. **Logit Model**: A parametric model (Logit) is used to calculate the propensity score for each individual, based on observed covariates.
2. **Propensity Score Matching**: We match individuals who were abducted with those who were not, based on their propensity scores, to estimate the ATE.
3. **Matching**: Optimal matching is performed over the entire dataset to find comparable treated and untreated individuals.
4. **Love Plot**: A Love plot is created to visualize balance after matching.

## Key Results

- The impact of abduction on years of education, emotional distress, and wages is estimated.
- The propensity score matching method helps control for confounding variables and estimate a more reliable treatment effect.

## Tools and Libraries Used

- **Programming Language**: R
- **Key Libraries**: `MatchIt`, `ggplot2`, `dplyr`

## How to Run

1. Clone the repository to your local machine.
2. Open the R Markdown file in RStudio.
3. Run the analysis by knitting the file.

## License

This project is open-source under the [MIT License](LICENSE).
