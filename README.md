🧠 Shell.ai Hackathon 2025 – Fuel Blend Properties Prediction Challenge
🚀 Project Overview

This project was developed for the Shell.ai Hackathon for Sustainable and Affordable Energy 2025, focusing on Fuel Blend Properties Prediction.
The goal is to build a machine learning model that predicts the final properties of fuel blends based on their composition and component characteristics.

The challenge supports sustainable fuel innovation, helping the industry move toward net-zero emissions by enabling accurate, data-driven fuel formulation.

🎯 Objective

To predict 10 final blend properties of fuels using:

Blend composition (5 columns)

Component properties (50 columns)

Based on the provided train.csv and test.csv datasets.

The model helps:

Evaluate thousands of potential blend combinations

Identify optimal recipes meeting safety & sustainability targets

Reduce development time for new fuel formulations

📂 Dataset Description
File	Description
train.csv	Contains input features (blend compositions & component properties) and 10 target columns (BlendProperty1–BlendProperty10).
test.csv	Contains input features for unseen blends (without target columns).
sample_submission.csv	Shows the expected format for your final submission file.
🧩 Columns Breakdown

Blend Composition (5 columns) – Volume fractions of base components

Component Properties (50 columns) – Properties of each component batch (structured as ComponentX_PropertyY)

Final Blend Properties (10 columns) – Target variables (BlendProperty1–BlendProperty10)

⚙️ Approach

The notebook follows a simple and interpretable ML pipeline using Random Forest Regression from scikit-learn:

Data Loading & Inspection

Data Cleaning & Preprocessing

Dropped unnecessary columns (like ID if present)

Checked for missing values

Ensured consistent feature columns between train/test

Model Training

Used RandomForestRegressor for multi-output prediction

Tuned for stability and accuracy

Evaluation

Metric: Mean Absolute Percentage Error (MAPE)

Prediction & Submission

Generated predictions for the 500 test samples

Saved submission.csv in the correct 10-column format

🧠 Model Details
Parameter	Value
Estimator	RandomForestRegressor
n_estimators	200
random_state	42
Scoring Metric	MAPE
Output	Multi-output regression (10 blend properties)
📊 Evaluation Metric

The hackathon uses Mean Absolute Percentage Error (MAPE):

MAPE
=
1
𝑛
∑
𝑖
=
1
𝑛
∣
𝑦
𝑖
−
𝑦
^
𝑖
𝑦
𝑖
∣
×
100
MAPE=
n
1
	​

i=1
∑
n
	​

	​

y
i
	​

y
i
	​

−
y
^
	​

i
	​

	​

	​

×100
