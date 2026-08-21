# Influencer Post Engagement Analysis

## Overview

This project analyzes influencer post engagement data for a marketing agency to determine which post format — Image, Video, or Carousel — generates the highest engagement for a client brand.

The experiments use Python, Pandas, SciPy, Matplotlib, and Seaborn to clean the dataset, perform statistical analysis, and visualize the engagement differences between post formats.

---

## Dataset

The dataset contains influencer post information including:

- Post ID
- Post Type
- Followers
- Engagement Rate (%)
- Engagement Count

Dataset file:

`Q20_influencer_engagement.csv`

---

# Round 2 — One-Way ANOVA

## Objective

To determine whether there is a statistically significant difference in mean engagement rate among Image, Video, and Carousel influencer posts.

## Methodology

1. Read the dataset using Pandas.
2. Checked for missing values.
3. Treated missing engagement counts using the median.
4. Removed duplicate posts using `post_id`.
5. Removed records with missing post type or engagement rate.
6. Calculated descriptive statistics for each post format.
7. Performed One-Way ANOVA using SciPy.
8. Compared the p-value with the significance level of 0.05.

## Hypotheses

**H₀:** There is no significant difference in mean engagement rate among Image, Video, and Carousel posts.

**H₁:** There is a significant difference in mean engagement rate among the post formats.

## Results

| Post Type | Mean Engagement Rate |
|-----------|----------------------:|
| Image | 3.37% |
| Carousel | 3.84% |
| Video | 4.55% |

### ANOVA Result

- F-statistic: **11.080238981131705**
- p-value: **3.9761140913525e-05**
- Significance level: **0.05**

Since the p-value is less than 0.05, the null hypothesis is rejected.

### Finding

There is a **statistically significant difference** in engagement rates among Image, Video, and Carousel posts.

### Output

<img width="693" height="340" alt="image" src="https://github.com/user-attachments/assets/1a02055d-dd85-4b18-915e-d99cc987630a" />


---

# Round 3 — Box Plot and Bar Chart

## Objective

To visually compare engagement rates across Image, Video, and Carousel posts and identify the best-performing content format.

## Visualizations

### Box Plot

The box plot compares the distribution of engagement rates for the three post formats. It shows the median, spread, and variation of engagement for each format.

<img width="672" height="458" alt="image" src="https://github.com/user-attachments/assets/0a56d641-8148-4cf4-a83a-8964c374ef12" />


### Bar Chart

The bar chart compares the average engagement rate of each post format.

<img width="669" height="470" alt="image" src="https://github.com/user-attachments/assets/ee0d7fb3-49ce-4e4c-ad65-5bcdf6959d19" />


## Findings

The average engagement rates are:

- **Video:** 4.55%
- **Carousel:** 3.84%
- **Image:** 3.36%

Video posts have the highest average engagement rate, followed by Carousel and Image posts.

The ANOVA result also confirms that the difference between post formats is statistically significant.

---

# Evidence-Based Content Strategy

Based on the analysis, the client should:

1. **Prioritize Video content** because it achieved the highest average engagement rate.
2. Use **Carousel posts** as a secondary format for informative or multi-step content.
3. Continue using **Image posts**, but use them selectively for simple visual announcements and branding content.
4. Monitor engagement performance continuously and test different topics, captions, and creative styles within each format.
5. Use future campaign data to validate whether the observed advantage of Video remains consistent over time.

## Final Conclusion

The analysis shows that **post format has a significant effect on engagement**.

Among the three formats, **Video posts generate the highest average engagement rate (4.554%)**. Therefore, the recommended strategy is to make Video the primary content format while using Carousel and Image posts as supporting formats.

---

## Technologies Used

- Python
- Pandas
- NumPy
- SciPy
- Matplotlib
- Seaborn
- Google Colab

---
