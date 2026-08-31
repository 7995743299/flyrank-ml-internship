# Machine Learning Content Refresh Prediction

## Overview

This project was developed during the FlyRank Machine Learning Internship.

The project uses observable content and performance signals to identify potentially declining pages. It compares a simple hand-written ranking rule with a readable Decision Tree model and evaluates the model using precision.

The project also demonstrates an important machine learning concept: data leakage, and why features that contain the target outcome must not be used.

## Who It Is For

This project is useful for SEO and content teams who want to identify pages that may need review or content refresh.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook
- GitHub

## Architecture

Data
↓
Data Preparation
↓
Feature Selection
↓
Hand-Written Baseline
↓
Decision Tree Model
↓
Validation
↓
Precision Evaluation
↓
Results

## Evaluation

The project compares a hand-written ranking rule with a depth-2 Decision Tree using Precision@20 and Precision@50.

A separate 80/20 train/test experiment was also performed. The Decision Tree achieved a test precision of 0.633 (63.3%) on the test split.

## Design Decision

I used a shallow Decision Tree because its decision rules can be printed and understood directly. This makes the model easier to interpret and inspect for potential problems.

## Data Leakage

The project demonstrates leakage using `trend_pct`. The target label is derived from the trend information, so using this feature allows the model to see the answer indirectly.

This demonstrates why features must represent information that would have been available before the outcome.

## Limitations

- The starter comparison includes an in-sample evaluation for teaching purposes.
- The dataset and experimental setup limit how broadly the results can be generalized.
- A shallow Decision Tree may not capture all available patterns.
- Precision can vary depending on the selected features and validation strategy.

## AI Transparency

I used AI as a development partner for coding assistance, debugging, documentation, and understanding the machine learning workflow. I reviewed the implementation, experiments, and results myself.

## Author

**Joshna Sindhuja Pitta**

FlyRank Machine Learning Internship
