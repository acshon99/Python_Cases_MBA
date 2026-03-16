# GitHub Portfolio: Predictive Analytics Storytelling

**ISOM 835 — Predictive Analytics | Sawyer Business School**

**Student Name: [Shonette Crossdale]**

# Online Shopper Purchasing Intention Prediction 
Leveraging web session data to predict online shipper revenue conversion and optimize e-commerce strategies.

# Business Problem: 
The client aims to understand the factors that are influencing online purchasing decisions and improve the conversion rate of website visitors into paying customers. Specifically, the goal is to identify sessions likely to result in revenue to enable proactive interventions and optimize marketing efforts, while minimizing lost sales opportunities. 

# The Data: 
The dataset comprises of `12,330` online shopping sessions, each are characterized by `18` attributes. It was sourced from the `UCI Machine Learning Repository (Online Shoppers Purchasing Intention Dataset)`. Features include metrics like `Administrative`,`Informational`, and `ProductRelated` page views and durations, `BounceRates`, `ExitRates`, `PageValues`, and categorical features such as `Month`, `OperatingSystems`, `Browser`, `Region`, `TrafficType`, `VisitorType`, and `Weekend`.

The target variable, `Revenue`, is a boolean indicating whether a session resulted in a purchase. A critical data quality issue is the high class imbalance, with only `15.47%` of sessions resulting in revenue.

# Key Discoveries: 
- There is a high imbalance in the target variable, with only 15.47% of sessions resulting in a purchase, which is a significant factor to consider for model training. 

- There is a visitor type impact, where `NewVisitors` show a higher proportion of revenue conversion `(24.91%)` compared to `ReturningVisitors` at `(13.93%)`, which could suggest different engagement strategies that might be needed. 

- There are peak purchasing months, such as November at 25.35% revenue, and October at 20.95% revenue stand out, while months like February display significantly low revenue at 1.63%, indicating seasonal patterns. 

- The sessions that lead to revenue consistently exhibit significantly higher `PageValues`, which highlights the importance of engaging users with valuable content. 

# Chart:
The chart that captures the main findings is the chart that displays the proportion of revenue by `VisitorType`. The bar chart illustrates the proportion of sessions that result in revenue across different visitor types. It shows that `NewVisitors` have a higher conversion rate than `ReturningVisitors`, which is a key insight for tailoring visitor-specific strategies. 

# Prediction Outcome:
My analysis involved training and comparing Gaussian Naive Bayes, decision tree, and logistic regression models. The GNB model emerged as the most suitable for this business problem, primarily due to its ability to minimize `False Negatives (154 missed sales)`. While other models have displayed higher overall accuracy or fewer False Positives, avoiding missed sales is deemed the most critical business priority. 

# Recommendations:

1. Prioritize `NewVisitor` conversion and high-value page engagement by focusing on optimizing the journey for new visitors and highlighting products or content with high `PageValues` to capitalize on their higher conversion propensity.

2. Optimize seasonal marketing efforts by strategically intensifying marketing during high-revenue months like November and October, while exploring novel engagement tactics for low-revenue months such as February. 

3. Deploy and refine predictive analytics for proactive interactions by integrating the GNB model to identify high-potential sessions in real-time, enabling proactive interactions like live chat or personalized offers to discover potentially lost sales. 

# Tools and Techniques: #
- # Programming Language: 
    Python
- # Data Maniputlation & Analysis: 
    Pandas
- # Machine Learning:
    scikit-learning (for `train_test_split`),
    GaussianNB,
    Decision Tree Classifier,
    Logistic Regression,
    Accuracy score,
    Confusion matric,
- # Data Visualization:
    matplotlib,
    seaborn
- # Data Source:
    ucimlrepo library for fetching the UCI dataset.
