# NYC Community Schools Initiative: SAT Score Disparities Analysis

**Course:** ECO225 | University of Toronto  
**Author:** Mariana Garcia Mejia

## Overview
This paper investigates the effect of New York City's Community Schools 
Initiative (2014) on SAT scores across 435 NYC public high schools. 
The study finds that while the initiative improved SAT performance in 
targeted schools, structural socioeconomic and racial inequalities continue 
to shape student outcomes — particularly for Black and Hispanic students 
with higher Economic Need Index scores.

## Research Questions
1. Which schools were selected as Community Schools, and what 
   characteristics do they share?
2. Did the Community Schools Initiative improve SAT performance?
3. What socioeconomic and racial factors predict SAT score disparities 
   across NYC high schools?

## Data
Two datasets from NYC Public High Schools (2012–2016), sourced from Kaggle:
- **College Board SAT dataset:** Average SAT scores for 435 accredited 
  NYC high schools (2014–2015)
- **PASSNYC demographic dataset:** Community school status, Economic Need 
  Index, School Income Estimate, School Disadvantage Index, and racial 
  composition for 1,273 high schools (2016)

## Methods

### Exploratory Data Analysis
- SAT score distributions before (2012) and after (2016) the initiative
- Geographic mapping of Community Schools vs. disadvantaged neighborhoods
- Racial and economic composition analysis across boroughs

### Linear Regression
Two sets of regression models predicting Average Total SAT Score:

**Regression 1** — Economic and racial predictors:
- Economic Need Index, School Income Estimate, Racial Composition
- Key finding: Economic Need Index (β = −814) and Majority Black 
  (β = −90) are significant even when controlling for each other

**Regression 2** — Broader socioeconomic predictors:
- School Disadvantage Index, Percent Tested, Chronic Absenteeism
- Key finding: Percent Tested is positive and significant; 
  absenteeism is not

### Machine Learning
- **Regression Tree:** Splits on Percent White (>20.25%) as the 
  primary predictor, followed by Percent Asian and Percent Hispanic
- **Random Forest:** Three models with different feature sets; 
  preferred model uses Economic Need Index, Percent White, 
  Percent Black, and Chronic Absenteeism — Economic Need Index 
  is the most important predictor

## Key Findings
- Community Schools improved SAT scores: median rose from below 
  1170 (2012) to above 1200 (2016)
- Community Schools were correctly targeted at high-need schools 
  (Medium/High Economic Need Index only)
- Economic Need Index is the strongest predictor of SAT performance 
  (β = −814 per unit increase)
- Racial disparities persist even after controlling for economic 
  factors — Majority Black schools score ~90 points lower
- Only 60% of students in majority Black/Hispanic schools take the SAT 
  vs. ~90% in majority White/Asian schools
- Community Schools cluster in the Bronx, Brooklyn, and Manhattan — 
  the three boroughs with the lowest average SAT scores

## Policy Recommendations
- Expand Community Schools to all high-need schools not yet designated
- Implement school-specific SAT preparation programs in high-need areas
- Foster a college-going culture to bridge the gap in SAT participation 
  rates between racial groups
- Address broader socioeconomic inequalities alongside academic 
  interventions

  ## Repository Structure
- Code
- Final Paper (PDF)
