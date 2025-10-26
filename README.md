🧠 Shell.ai Hackathon 2025 – Fuel Blend Properties Prediction
🚀 Overview

This project is built for the Shell.ai Hackathon for Sustainable and Affordable Energy 2025.
The goal is to predict 10 final blend properties of fuels using their composition and component properties, helping design sustainable fuel blends efficiently.

📊 Dataset
train.csv – 55 input features + 10 target blend properties
test.csv – 55 input features (no targets)
sample_submission.csv – required output format

Input features include:
5 blend composition columns
50 component property columns

⚙️ Methodology
A Random Forest Regressor is used for multi-output prediction.
Steps:

Load and clean data (drop ID column if present)

Train Random Forest model

Evaluate using Mean Absolute Percentage Error (MAPE)

Generate predictions and save as submission.csv

🧾 Submission Format

Output file must have:

500 rows × 10 columns

Columns: BlendProperty1 … BlendProperty10

Only floating-point values

	​

	​

