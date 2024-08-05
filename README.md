# JMP---Ilvl-reliance-on-DPS-

1. Objective of the Study

The study aims to analyze data from the game World of Warcraft, focusing on performance logs from the latest raid “Icecrown Citadel”. The primary goal is to identify which features have the most significant explanatory power for a specific variable, allowing for better future predictions.

2. Data Collection

	•	Source: Data is sourced from Warcraftlogs.com.
	•	Data Details: 40 logs from four different bosses: “Lord Marrowgar Heroic”, “Deathbringer Saurfang Heroic”, “Rotface”, and “Festergut Heroic”.
	•	Data Format: Each log contains 25-28 rows, with a total dataset of 1099 rows and 6 columns.
	•	Features: Parse %, Amount, Ilvl, Ilvl %, Active, and DPS.

3. Data Exploration

	•	Missing Values: Identified in Parse %, Ilvl, and Ilvl % (6.7% missing).
	•	Outliers: Found in Parse % and Ilvl %.
	•	Correlation: High correlation between DPS and Amount (94%), and between Active and DPS (78%).

4. Data Preparation

	•	Outlier Treatment: 238 outliers in the ‘Active’ feature were treated and converted to missing values.
	•	Missing Values: Addressed using JMP’s algorithm.

5. Model Short-listing

	•	Boostrap Forest Analysis: Initial analysis with 100 trees showed potential overfitting with high RSquare values (0.956 for training and 0.890 for validation).
	•	Model Screening: Identified multiple models with high RSquare values, confirming overfitting.
	•	Lasso Analysis: Highlighted the significance of the Imputed_DPS feature, indicating it as a major factor in overfitting.

6. Model Fine-tuning

	•	Neural Boosted Model: Tuned by adding layers and nodes, improving RSquare from 88.8% to 89.1%.
	•	Hyperparameter Adjustments: Tested various combinations to improve model performance.
	•	Validation: Models showed better performance with a smaller training and validation set, indicating overfitting.

7. Final Analysis and Conclusion

	•	Fit Stepwise Model: Evaluated combinations of features, confirming Imputed_DPS as a significant feature with high predictive power.
	•	Business Objective: Successfully identified key features that explain the primary variable, with Imputed_DPS being the most influential.
	•	Model Performance: Models performed well, validating initial expectations and demonstrating strong explanatory power for the primary variable.

Conclusion

The study effectively identified and analyzed key features affecting performance in World of Warcraft raids. Despite overfitting concerns, the models provided valuable insights, with Imputed_DPS emerging as a critical feature for accurate predictions.
