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
   -    - Class evaluation participation (higher participation correlates with higher ratings)
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
![171ec8eb-12a5-424f-a1fe-6836a962e640](https://github.com/user-attachments/assets/90279efc-40be-4322-8818-bdde70d146ec)
![5a9faf87-d096-4c1e-bca0-a167c3d3444c](https://github.com/user-attachments/assets/47f070e9-a7fa-49fd-802c-0043856aa3e6)

![d82bd09a-7df1-4bca-80d6-c0412f4e06d0](https://github.com/user-attachments/assets/0c808200-4661-4985-82c1-991d8e0d634e)
![0d892ae0-3d22-46b4-9e96-15ed11034ea9](https://github.com/user-attachments/assets/25621bc3-55e8-4742-9b1a-1c1d31462328)

![f8309830-2af1-438f-8c3b-1542d6ba72d4](https://github.com/user-attachments/assets/4b4b245d-6831-45ce-a37e-e69206efa2b8)
![f74a2955-1d81-4aaf-91eb-f9abb08c31fc](https://github.com/user-attachments/assets/a78ae568-6d2b-4772-9c44-330127881035)
