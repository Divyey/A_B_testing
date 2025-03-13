# A/B Testing for Website Higher Engagement/Conversion Optimization

## Overview
This project analyzes A/B testing data to compare the performance of two versions of a webpage: the control (old page-light theme) and the treatment (new page-dark theme). The goal is to determine which version improves user conversion rates.

![image](https://github.com/user-attachments/assets/8f43cf72-11e4-46ec-b85b-c6122fcca058)

## Approach: 
 Conducted an A/B test to measure the impact of dark mode on user conversion rates, analyzing 286K+ sessions.
1. Data Cleaning & Preparation: Removed 3,894 duplicate user sessions to ensure data integrity.
2. Sampling Strategy: Used statistical power analysis to determine an optimal sample size of 4,720 users per group (9,440 total).
3. A/B Testing: Conducted a proportion z-test to compare conversion rates between control (light mode) and treatment (dark mode).
4. Statistical Significance: Set α = 5% and test power = 80% to detect a meaningful 2% effect size.

## Getting Started

### Prerequisites
- Python 3.x
- Required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `statsmodels`

### Installation
To install the necessary libraries, run:

    pip install -r requirements.txt


### Usage
1. Clone this repository:

    git clone https://github.com/Divyey/AB_Testing.git
   
    cd AB_Testing

3. Place your dataset (`ab_data.csv`) in the `data/` folder.
4. Run the script:
   
    python AB_Testing.ipynb

## Data Description
The dataset includes:
- `user_id`: Unique identifier for each user.
- `timestamp`: Time of interaction.
- `group`: Indicates whether the user was shown the control or treatment version.
- `landing_page`: Specifies which page the user interacted with.
- `converted`: Binary value indicating whether the user converted (1) or not (0).

![image](https://github.com/user-attachments/assets/9d975ff7-50ec-40a2-a07a-e04b2ef383b9)

## Findings & Results:
1. The control group (light mode) had a conversion rate of 11.10%.
2. The treatment group (dark mode) had a conversion rate of 12.5%, showing an increase.
3. The calculated p-value (0.0352) indicated moderate evidence against the null hypothesis, leading to its rejection.

## Results and Analysis
The script calculates conversion rates for both groups, performs statistical tests, and visualizes results to help interpret findings.
The A/B test on 286K+ user sessions showed that the dark mode version increased conversion rates from 11.10% to 12.5%, with a statistically significant p-value of 0.0352. The project recommended dark mode as an effective UX enhancement, while continuing to monitor performance over time.
