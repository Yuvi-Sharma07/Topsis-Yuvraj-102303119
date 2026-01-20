# TOPSIS Implementation using Python

## Project Overview
This project implements the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method using Python.
TOPSIS is a multi-criteria decision-making (MCDM) technique used to rank alternatives based on their relative closeness
to an ideal best solution and distance from an ideal worst solution.

The implementation is done using Python in a Google Colab notebook and the complete solution is uploaded to GitHub
as required for academic submission.

---

## Objectives
- To implement the TOPSIS algorithm using Python
- To rank multiple alternatives based on multiple criteria
- To visualize the ranking results using a graph
- To document the complete methodology and results clearly

---

## Input Description
The input data is provided in CSV format with the following structure:

- **First column**: Names of alternatives (non-numeric)
- **Remaining columns**: Criteria values (numeric only)

Example:
| Alternative | C1 | C2 | C3 | C4 | C5 |
|------------|----|----|----|----|----|
| A1 | 250 | 16 | 12 | 5 | 1 |
| A2 | 200 | 20 | 8 | 4 | 2 |

Additional inputs:
- **Weights**: A list of numerical values separated by commas (e.g., 1,2,3,4,5)
- **Impacts**: A list of '+' or '-' values separated by commas (e.g., +,+,+,-,+)

---

## Validation Rules Implemented
The following validations are applied in the implementation:

- Input file must contain at least three columns
- All criteria columns (2nd column onwards) must contain numeric values
- Number of weights must be equal to number of criteria
- Number of impacts must be equal to number of criteria
- Impacts must be either '+' (benefit) or '-' (cost)
- Weights and impacts must be comma-separated

---

## Methodology
The TOPSIS algorithm is implemented using the following steps:

1. **Reading Input Data**
   - Read CSV file using Pandas
   - Separate alternative names and criteria values

2. **Normalization of Decision Matrix**
   - Each criterion value is normalized using vector normalization:
     r_ij = x_ij / sqrt(sum(x_ij²))

3. **Weight Assignment**
   - Normalized values are multiplied by normalized weights

4. **Determination of Ideal Best and Ideal Worst**
   - Ideal Best: Maximum value for benefit criteria and minimum for cost criteria
   - Ideal Worst: Minimum value for benefit criteria and maximum for cost criteria

5. **Distance Calculation**
   - Euclidean distance of each alternative from ideal best and ideal worst

6. **TOPSIS Score Calculation**
   - Score = Distance from Ideal Worst / (Distance from Ideal Best + Distance from Ideal Worst)

7. **Ranking**
   - Alternatives are ranked in descending order of TOPSIS score

---

## Output Description (Result Table)
The output result contains the following additional columns:

- **Topsis Score**: Indicates closeness of an alternative to the ideal solution
- **Rank**: Rank of alternatives based on TOPSIS score

Higher TOPSIS score indicates a better alternative.

---

## Result Visualization (Graph)
A bar graph is generated using Matplotlib to visualize the TOPSIS scores of all alternatives.
This helps in easy comparison and interpretation of results.

- X-axis: Alternatives
- Y-axis: TOPSIS Scores

---

## Tools & Technologies Used
- Python 3
- Google Colab
- Pandas
- NumPy
- Matplotlib
- GitHub

---

## How to Run the Project
1. Open the Google Colab notebook provided in the repository
2. Upload the input CSV file
3. Provide weights and impacts in the specified format
4. Run all cells sequentially
5. View the result table and result graph
6. Download the output CSV file

---

## Assumptions
- Input CSV file is properly formatted
- Criteria values are numeric and non-null
- Weights provided are positive numbers
- Internet connection is available for Google Colab

---

## Conclusion
The TOPSIS method provides an effective approach for multi-criteria decision making.
This implementation successfully ranks alternatives by considering both beneficial and non-beneficial criteria.
The inclusion of result visualization further enhances interpretability of the decision-making process.

---

## Author
**Yuvraj Sharma**  
Roll No: **102303119**

---

## GitHub Repository
This repository contains:
- Google Colab notebook (.ipynb)
- Sample input CSV file
- Detailed README documentation
