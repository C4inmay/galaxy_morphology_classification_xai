# Dataset Exploration

## Objective

The objective of this notebook was to understand the Galaxy Zoo dataset, inspect the labels, and create meaningful target classes for image classification.

---

## Dataset Information

- Source: Kaggle - Galaxy Zoo: The Galaxy Challenge
- Total Samples: 61,578
- Features:
  - GalaxyID
  - 37 probability label columns
- Missing Values: None
- Duplicate Rows: None

---

## Exploratory Data Analysis

Performed:

- Loaded the dataset using Pandas.
- Inspected dataset shape and column names.
- Checked data types.
- Verified missing values.
- Verified duplicate rows.
- Calculated descriptive statistics.
- Computed average probability for every label.
- Visualized label distribution.

---

## Label Understanding

The original dataset does not contain a single class label.

Instead, it contains:

- 11 Questions
- 37 Possible Answers

Each answer is represented as a probability generated from multiple Galaxy Zoo volunteers.

Example:

Question 1

- Smooth
- Features/Disk
- Star

Question 2

- Edge-on
- Not Edge-on

...

---

## Label Engineering

Created readable mappings for every ClassX.Y label.

Selected the most probable answer for each question.

Designed a rule-based classifier to convert multiple answers into one final galaxy class.

Final classes:

- Oval
- Elliptical
- Spiral
- Edge-on Spiral
- Disk
- Ring Galaxy
- Barred Spiral
- Irregular
- Cigar
- Merger
- Other

Rare classes (Star and Dust Lane) were merged into "Other".

---

## Output

Generated:

data/processed/galaxy_labels.csv

Columns:

- GalaxyID
- Galaxy_Class

This file will be used for model training.

---

## Next Step

- Load galaxy images.
- Match images with labels.
- Explore image dimensions.
- Visualize samples.
- Prepare the dataset for PyTorch.