# Dynamic Pricing & Discount Strategy Analysis

A data science project analysing retail markdown data to uncover price elasticity patterns
by category and season, culminating in a data-backed discount strategy recommendation.

## Project Overview

Retailers constantly face a core question: when and how much should we discount?
Discount too little and inventory doesn't move, discount too much and margin is wasted on
customers who would've bought anyway. This project analyses real markdown event data to
answer that question with evidence rather than guesswork.

## Objective

Using a retail markdown dataset, this project investigates:
1) How price elasticity varies across the product categories Skincare, Bodycare, Makeup.
2) Whether discount effectiveness changes by season
3) Whether brand identity affects pricing power
4) The overall relationship between discount depth and sales lift

## Dataset

[Retail Markdown Optimization: Discounts & Sales](https://www.kaggle.com/datasets/arbaaztamboli/retail-markdown-optimization-discounts-and-sales): 43,750 product records across 4 markdown events each, including original price, competitor price, discount rate, sales before/after each markdown, customer ratings, and more.

## Tools & Libraries

- **Python** (Google Colab)
- **pandas**: data cleaning, aggregation, groupby analysis
- **matplotlib** & **seaborn**: data visualization
- **NumPy** (via pandas): numerical calculations

## Methodology

1. Loaded and explored the dataset structure
2. Calculated discount percentage and sales lift percentage per markdown event
3. Calculated price elasticity per product, per markdown level
4. Averaged elasticity across all 4 markdown levels for a robust score
5. Analysed elasticity by category, by season, and by category × season combined
6. Analysed brand-level pricing power
7. Visualised findings and synthesised results into a business recommendation

## Key Findings

1. **All categories show inelastic to moderate price sensitivity overall**: no category is highly responsive to discounting on average.
2. **Season matters more than category alone.** Each category has a specific season where discounting is largely ineffective:
   Skincare: has weak response in Rainy and Spring
   Bodycare: has weak response in Spring
   Makeup: has weak response in Rainy
   
   This pattern held consistently across all 4 markdown levels.
3. **Brand is not a meaningful differentiator.** All 6 brands showed nearly identical elasticity, customer ratings, and pricing relative to competitors; meaning, pricing strategy should be driven by category and season, not brand.
4. **Discount depth and sales lift are strongly, near linearly related** across the full range tested.

## Recommendation

- Skincare and Bodycare markdowns should be timed around their effective seasons rather than
applied year-round uniformly.
- Avoid discounting Skincare during Rainy and Spring, and Bodycare during Spring since both show minimal sales response in these windows, meaning markdown margin is likely being wasted.
- Concentrate markdown budget on Summer and Winter, where all three categories show stronger elasticity.
- Since brand does not meaningfully affect price sensitivity, pricing strategy should be driven by category and season, not brand identity.

## Visualizations

The notebook includes:
- Bar chart of average elasticity by category
- Heatmap of elasticity by category × season
- Scatter plot of discount % vs. sales lift %


## References

See the References section at the end of the notebook for full citations, including the dataset source, libraries used, and learning resources.

## Skills Demonstrated

Data cleaning - Exploratory data analysis - pandas (groupby, aggregation, feature engineering) - Data visualisation (matplotlib, seaborn) - Price elasticity analysis - Business-oriented data storytelling
