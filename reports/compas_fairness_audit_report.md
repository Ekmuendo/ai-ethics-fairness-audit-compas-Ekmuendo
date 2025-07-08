This audit focused on assessing racial bias within the COMPAS dataset using IBM’s AI Fairness 360 toolkit. The dataset is widely known for predicting recidivism risks and has raised ethical concerns regarding fairness across racial groups, specifically between Black and White defendants.

To begin, we loaded and explored the dataset, identifying key features related to race, age, and prior convictions. We defined “privileged” as White individuals and “unprivileged” as non-White individuals, following standard fairness evaluation protocols. Using AIF360’s metrics, we calculated Disparate Impact, Equal Opportunity Difference, and False Positive Rate Difference to quantify bias.

The initial Disparate Impact score was 0.84, suggesting that unprivileged individuals were less likely to receive favorable (low-risk) predictions compared to privileged ones. This metric being far from the ideal score of 1.0 indicates the presence of potential systemic bias. Meanwhile, Equal Opportunity and False Positive Rate Differences were both 0.00, showing parity in those areas — which is promising.

To mitigate the bias, we applied the Reweighing algorithm, a preprocessing technique that adjusts instance weights in the training data to reduce discrimination without changing labels or features. After reweighing, the Disparate Impact improved (closer to 1.0), demonstrating enhanced fairness across racial lines.

While we didn’t train a predictive model in this audit, the analysis shows that preprocessing can already significantly affect fairness outcomes. This process reinforces the importance of fairness-aware design, especially in high-stakes systems like criminal justice.

In conclusion, bias in datasets can deeply affect AI predictions and societal outcomes. Tools like AI Fairness 360 provide a practical foundation for identifying and mitigating such biases. Moving forward, audits like this should become a standard step in responsible AI development.

