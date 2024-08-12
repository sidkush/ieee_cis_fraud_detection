# IEEE-CIS Fraud Detection

## Business Problem Statement
Fraud detection is a critical challenge faced by various industries, including e-commerce and banking services. With the rise of online transactions, there has been a corresponding increase in fraudulent activities. This project aims to develop a fraud detection system using the IEEE-CIS Fraud Detection dataset provided by VESTA corporation. The goal is to accurately classify transactions as fraudulent or genuine while minimizing false positives and enhancing the customer experience.

## Methodology
The methodology employed in this project involves several key steps:

1. **Data Preprocessing**: The dataset underwent memory optimization by casting appropriate data types. Null values were handled using an iterative imputer, and outliers were treated using Power Transformation (Yeo-Johnson method) to improve data distribution and normalize the data.

2. **Dimensionality Reduction**: Principal Component Analysis (PCA) was applied to reduce the feature dimensions to 72, explaining 95% of the data variance.

      ![image](https://github.com/user-attachments/assets/77d4f94d-51dc-49d7-b17c-80408633a871)


3. **Imbalance Treatment**: The dataset exhibited a class imbalance, with 96.5% non-fraudulent transactions and 3.5% fraudulent transactions. The Synthetic Minority Oversampling Technique (SMOTE) was employed to address this imbalance by oversampling the minority class.

      ![image](https://github.com/user-attachments/assets/cba90861-ab93-49f7-95cc-d0a1af4e82b4)


5. **Model Selection and Evaluation**: Various machine learning models were explored, including Logistic Regression, Random Forest Classifier, Balanced Random Forest Classifier, CatBoost Algorithm, and Gaussian NB. The models were evaluated using the Area Under the Curve (AUC) score.

      ![image](https://github.com/user-attachments/assets/c78afbd9-d76a-405b-9d1a-5dadad441a06)

      ![image](https://github.com/user-attachments/assets/99cf0f23-a525-4272-8f62-25a5be19646a)


7. **Ensemble Methods**: Ensemble methods were employed to improve model performance and reduce overfitting. A hyperoptimized Balanced Random Forest Classifier was used, which automatically rectifies imbalance concerns through resampling and reshuffling techniques.

      ![image](https://github.com/user-attachments/assets/6997183b-fe45-4634-a722-ecdafa2b6f25)

      ![image](https://github.com/user-attachments/assets/c121cb05-ac4d-4f65-919a-78af92eef8c2)


10. **Advanced Models**: The CatBoost algorithm was hyperoptimized, specifying parameters such as 1000 iterations, a depth of 16, a learning rate of 0.73, and an evaluation metric of 'F1'. The Balanced Random Forest was further enhanced by incorporating the AdaBoost algorithm with a learning rate of 0.73 and 50 estimators.

      ![image](https://github.com/user-attachments/assets/6198b40f-b2dd-49c6-8164-71823d3fe682)


## Key Findings from EDA
During the exploratory data analysis (EDA), several key findings were observed:

- Fraudulent transactions were more prevalent on Sundays compared to other days of the week.
- Fraudulent transactions decreased consistently during the afternoon hours across all days.
- Non-fraudulent transactions had a transaction amount cap below $10,000, while fraudulent transactions reached up to $5,000.
- The average amount of fraudulent transactions was higher than the average amount of non-fraudulent transactions.
- Fraudulent transactions were more associated with products categorized as W or C, settled through debit cards or credit cards (Visa or MasterCard).
- Charge cards like American Express and Discover had minimal to no instances of fraudulent transactions.
- Protonmail.com and mail.com were identified as prominent email domains associated with fraudulent transactions.
- Fraudulent transactions were more concentrated on mobile platforms, while legitimate transactions were more commonly performed on desktops.
- Identification fields (id12 to id38) had a substantial prevalence of null values, exceeding 70%.

## Model Selection and Performance
Several machine learning models were explored in this project. The Balanced Random Forest Classifier incorporated with AdaBoost achieved the best performance with an AUC score of 0.94. It significantly reduced the false negatives, which was a major concern.

The CatBoost algorithm also demonstrated promising results, achieving an AUC score of 0.95 while maintaining a nearly identical F1 score as the Balanced Random Forest Classifier.

The choice of ensemble methods and advanced models played a crucial role in improving the fraud detection system's performance. The Balanced Random Forest Classifier effectively addressed the class imbalance issue, while the AdaBoost algorithm enhanced its capabilities by expediting convergence.

## Conclusion
In conclusion, this research project successfully developed a fraud detection system using the IEEE-CIS Fraud Detection dataset. By employing various machine learning techniques, including data preprocessing, dimensionality reduction, imbalance treatment, and ensemble methods, the project achieved remarkable results in accurately classifying fraudulent transactions.

The Balanced Random Forest Classifier incorporated with AdaBoost emerged as the optimal model, achieving an AUC score of 0.94 and significantly reducing false negatives. The findings from the exploratory data analysis provided valuable insights into the patterns and characteristics of fraudulent transactions, aiding in the development of effective fraud detection strategies.

This project demonstrates the potential of machine learning in combating fraudulent activities and contributes to the broader field of fraud detection. The developed system can be further enhanced and adapted to real-world scenarios, helping financial institutions and businesses safeguard their operations and protect their customers from fraudulent transactions.
