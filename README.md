# TOPSIS Implementation using Python

## Introduction
This project implements the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method using Python.
TOPSIS is a multi-criteria decision-making technique used to rank alternatives based on their distance from an ideal solution.

---

## Methodology
1. Read the input CSV file containing alternatives and criteria.
2. Normalize the decision matrix.
3. Apply weights to normalized values.
4. Determine ideal best and ideal worst solutions.
5. Calculate Euclidean distance from ideal best and worst.
6. Compute TOPSIS score.
7. Rank alternatives based on TOPSIS score.

---

## Input
- CSV file
- First column: Alternative name
- Remaining columns: Numeric criteria
- Weights and impacts provided by the user

---

## Result Table
The output file contains:
- Topsis Score
- Rank

Each alternative is ranked based on its closeness to the ideal solution.

---

## Result Graph
A bar graph is generated to visualize TOPSIS scores of all alternatives for easy comparison.

---

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Google Colab

---

## How to Run
1. Open the Colab notebook.
2. Upload the CSV file.
3. Enter weights and impacts.
4. Execute all cells.

---

## Conclusion
TOPSIS helps in selecting the best alternative by considering multiple conflicting criteria.
This implementation provides both numerical and visual analysis of results.
