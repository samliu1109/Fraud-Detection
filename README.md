# Fraud-Detection

Executive Summary 
Problem: 
Discovering fraud in the business is very important for all companies. Fraud can decrease the confidence of your investors, partners, and customers in your organization. If the losses from fraud are so great, they might threaten your business’s existence. Moreover, the consequences of significant failures can impose financial, reputational, loyalty, and other brand-related costs that will persist for a very long time. Therefore, managing the risk of fraud is very important to gain a significant competitive advantage over those that don’t. This analysis aims to find potential fraud, waste, and abuse in the payment stream.

Key Findings:  
1.	Email domain is the fourth important variable in the model. It shows that the more common email addresses that show high frequency in the fraud, the more likely the transactions with these email addresses are fraud.
2.	The billing postal code is the tenth important variable in the model. It indicates that if the transactions come from the postal code that frequently appears, they are less likely fraud.
3.	The first 6 digits of the credit card, which determines the card type and issuing bank, is also an influential variable in the model. Some card types and issuing banks frequently appear in the fraud, indicating the more likely fraud in the transactions.
4.	The larger the USD value of the transaction, the more probability the transaction might be a fraud. However, if the adjustment USD $ value to the transaction is high, the transaction will be less likely to be a fraud.

Model Performance Summary & Interpretation 
1.	Comparing the three models in the analysis, the random forest shows the highest area under the curve, roughly 98%, which means only a 2% misclassification rate. 
2.	The random forest has the lowest misclassification rate among the three models, indicating the best model to fit the data. In addition, the lowest mean of log loss shows a little error rate.
3.	Looking at the precision rate, how many are fraud in all the transactions labeled as fraud. The random forest has the highest precision rate to label the correct fraud transaction.
4.	Looking at the recall rate, they are actually fraud; how many have been identified. Though the logistic model has the highest recall rate, its AUC and precision rate are not better than random forest. The random forest has the second-highest recall rate to identify the many actual fraud transactions.
5.	When controlling the false positive rate to 6%, the threshold should change to 0.083, the false positive rate will be 6%, and the true positive rate is 92%, which means the model can distinguish 92% of fraud transactions. In the meantime, the precision rate decreases to roughly 49%, indicating a 50% probability to identify fraud transactions correctly.

Recommendations  
1.	To mitigate the false positive rate to 6%, identify any transactions as fraud with over 8.3 probability of fraud. Instead of the cost of identifying an average transaction as a fraud, the loss of missing to identify fraud is more detrimental. Therefore, the plan is to set a high standard to clarify any possible transactions as fraud and prevent them from contributing a huge loss.
2.	For the email domains of the transactors that has counted as high frequency used in fraud transactions, tracking them to prevent a fraud transaction in advance.  
3.	For the billing postal codes that show little in the transactions, those postal codes are high-risk transactions to implement fraud.  
4.	The digits of the credit card that show the most common card types and issuing banks that happen in a fraud transaction should track them in advance to prevent a fraud transaction.
5.	Paying attention to the anomaly large value transactions, these transactions have a high probability of implementing fraud.
