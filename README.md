# Does Negativity Drive Engagement? -- Evidence from Donald Trump’s Social Media Posts

## Overview
This project investigates how sentiment influences engagement in political social media content. Specifically, we analyze whether negative sentiment leads to higher engagement in posts by Donald Trump, and whether this relationship changed after 2021.
Using a combination of sentiment analysis, feature engineering, and regression modeling, we compare:

- Pre-2021 Twitter posts
- Post-2021 social media posts

Our findings show that negative sentiment is strongly associated with higher engagement, and that this relationship shifted significantly after 2021.

## Research Questions
1. Does sentiment polarity predict engagement (likes & retweets)?
2. Did the relationship between sentiment and engagement change after 2021?

## Dataset
We combine two datasets:
- Twitter data (pre-2021)
- Post-2021 social media data

Each observation includes:
- `Post text`
- `Favorites (likes)`
- `Retweets`
- `Timestamp`
- `Retweet indicator`

To ensure comparability across platforms, engagement metrics were standardized using z-scores

## Data Cleaning & Feature Engineering
We used a lexicon-based approach (AFINN) to compute sentiment scores.
Improvements:
- Baseline accuracy: 63.5%
- Extended lexicon accuracy: 65%
- Improved negative sentiment detection by ~5%

Common Negative Words
Examples: `"fake”`, `“bad”`, `“crime”`, `“crooked”`, `“illegal”`, `“radical”`

## Exploratory Data Analysis
<img width="874" height="540" alt="fig5" src="https://github.com/user-attachments/assets/6f64a84b-d652-4b08-b19a-e58e30fe8236" />
<img width="873" height="537" alt="fig4" src="https://github.com/user-attachments/assets/b913ee8d-2a7e-4e8f-9804-ebcb21fdf9a5" />
<img width="873" height="541" alt="fig3" src="https://github.com/user-attachments/assets/bbe31f8a-d6c8-41ff-89b4-792707ba3b2f" />

Key Insights:
- Most posts are neutral or mildly emotional.
- Negative posts receive higher engagement.
- Neutral & positive posts show lower, similar engagement.
- Boxplots show higher median engagement for negative sentiment.

## Modeling Approach
We fit multivariable linear regression models:
<img width="1260" height="65" alt="Screenshot 2026-03-31 at 17 35 04" src="https://github.com/user-attachments/assets/21dd4c98-ac22-4f54-ba8e-fa1f5282573a" />
- 𝑌𝑖: relative engagement (favorites or retweets)
- 𝑋𝑖: control variables (length, capitalization, etc.)

Models:
- Model 1: Sentiment → Engagement
- Model 2: Sentiment × Period interaction
​
## Results
- Negative sentiment significantly increases engagement.
- Sentiment is a strong predictor of both likes and retweets.
- Stylistic features (e.g., exclamation marks, emphasis) also matter.

## Limitations
- Lexicon-based sentiment may miss sarcasm and context-specific meaning.
- High engagement may reflect controversy, not agreement.





