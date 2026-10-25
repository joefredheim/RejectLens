# RejectLens

**A simple reject analysis in digital radiography using Python**

Final project for IT6119 (Health AI), NTNU, 2026.

## What is this?

In radiography, some images have to be rejected and taken again, for example because of positioning errors or patient motion. Each repeat means extra radiation for the patient and extra time for the department. Reject analysis is a common quality-assurance task.

This project shows how Python can be used to:

1. Create a synthetic (made-up) reject log of 1,000 X-ray exposures
2. Calculate the overall reject rate
3. Make charts of reject rate by exam type, reject reasons and patient mobility
4. Train a simple decision tree that estimates which exposures have a higher risk of being rejected
5. Evaluate the model with sensitivity and specificity

## Data

**All data is synthetic.** No real patients, staff or hospital data are used. The data is generated inside the notebook with a fixed random seed, so the results are the same every time.

| Column | Meaning |
|---|---|
| `exam` | Type of examination |
| `mobility` | Walking, wheelchair or bed |
| `shift` | Day, evening or night |
| `rejected` | 1 = rejected, 0 = accepted |
| `reason` | Reject reason (empty if accepted) |

## How to run

1. Open [Google Colab](https://colab.research.google.com)
2. Click **File → Upload notebook** and choose `RejectLens.ipynb`
3. Click **Runtime → Run all**

No installation is needed.

## Files

| File | Content |
|---|---|
| `RejectLens.ipynb` | The notebook with all code and explanations |
| `synthetic_reject_log.csv` | The synthetic dataset created by the notebook |
| `figures/` | Charts used in the report |

## Limitations

The model learns from made-up data, so it can only find patterns that were built into the data. This project demonstrates a method and is not a tool for clinical use.
