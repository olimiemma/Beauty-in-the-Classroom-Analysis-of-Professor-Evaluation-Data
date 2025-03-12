# Beauty in the Classroom: Analysis of Professor Evaluation Data

## Overview

This repository contains a statistical analysis of professor evaluation data from the University of Texas at Austin, exploring factors that influence student evaluations of teaching. The analysis examines the relationship between professors' physical appearance ratings and their teaching evaluation scores, along with various other demographic and course-related variables.

The project is based on data from the study "Beauty in the classroom: instructors' pulchritude and putative pedagogical productivity" by Hamermesh and Parker (2005), which investigated whether instructors who are viewed as better looking receive higher instructional ratings.

## Dataset

The dataset (`evals.csv`) contains end-of-semester student evaluations for 463 courses taught by 94 professors. Six students also rated the professors' physical appearance. Key variables include:

- `score`: Average professor evaluation score (1-5 scale)
- `bty_avg`: Average beauty rating of the professor
- `gender`: Gender of professor (female, male)
- `age`: Age of professor
- `ethnicity`: Ethnicity of professor (not minority, minority)
- `language`: Language of school where professor received education (English, non-English)
- `rank`: Rank of professor (teaching, tenure track, tenured)
- `cls_perc_eval`: Percent of students in class who completed evaluation
- `cls_students`: Total number of students in class
- `cls_level`: Class level (lower, upper)
- `cls_credits`: Number of credits (one credit, multi credit)
- `pic_outfit`: Outfit of professor in picture (not formal, formal)
- `pic_color`: Color of professor's picture (color, black & white)

## Research Questions

This analysis explores:

1. Is there a relationship between a professor's physical attractiveness and their teaching evaluation scores?
2. What other factors influence teaching evaluation scores?
3. What are the characteristics of professors who receive high evaluation scores?
4. Are teaching evaluations potentially biased by factors unrelated to teaching effectiveness?

## Analysis Approach

The analysis follows these key steps:

1. Exploratory data analysis of evaluation scores and beauty ratings
2. Simple linear regression of scores on beauty ratings
3. Multiple regression incorporating additional predictors
4. Model selection using backward elimination
5. Diagnostic checks of regression assumptions
6. Interpretation of the final model

## Key Findings

1. Physical attractiveness is a statistically significant predictor of teaching evaluation scores, even after controlling for other variables.
2. The final model identified several significant predictors:
   - Gender (male professors receive higher ratings)
   - Language (non-English educated professors receive lower ratings)
   - Age (younger professors receive higher ratings)
   - Class evaluation participation (higher participation correlates with higher ratings)
   - Course credits (one-credit courses receive higher ratings)
   - Beauty ratings (more attractive professors receive higher ratings)
   - Photo color (black & white photos associate with higher ratings)

3. These findings raise important questions about potential biases in student evaluations of teaching.

## File Structure

- `evals.csv`: The dataset
- `professor_evaluations_analysis.Rmd`: R Markdown file containing the complete analysis
- `professor_evaluations_analysis.html`: Rendered output of the analysis
- `LICENSE`: License information
- `images/`: Directory containing visualizations

## Requirements

To run the analysis:

- R (version 4.0.0 or higher)
- RStudio (recommended for working with R Markdown)

Required R packages:
- `tidyverse`
- `ggplot2`
- `GGally`
- `gridExtra`
- `knitr`

## Usage

1. Clone this repository
2. Open the R Markdown file in RStudio
3. Install required packages if needed:
   ```r
   install.packages(c("tidyverse", "ggplot2", "GGally", "gridExtra", "knitr"))
   ```
4. Run the entire R Markdown document or execute code chunks sequentially

## Reproducing the Analysis

The analysis can be reproduced by running the R Markdown file. All data transformations and modeling steps are included in the code.

## Limitations

- Data is from a single university (University of Texas at Austin)
- The final model explains only about 16.3% of the variance in evaluation scores
- The study design is observational, limiting causal inferences
- Results may not generalize to other institutions or time periods

## Citation

When using this analysis or dataset, please cite the original research:

Hamermesh, D. S., & Parker, A. (2005). Beauty in the classroom: instructors' pulchritude and putative pedagogical productivity. Economics of Education Review, 24(4), 369-376.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Thanks to the original researchers for making this dataset available
- This analysis was completed as part of a statistical modeling course
