# Expectation Decider

**Probability analysis to understand which students are likely to pass a competitive mathematics exam.**

> Project PR-1: Mathematics and Advanced Statistics

---

## 1. About the Project

An educational institute wants an "Expectation Decider" model that tells how likely a student is to pass a competitive maths exam.
In this project, I act as a junior data analyst. I use data of **200 students** and apply probability topics to find patterns.

## 2. Dataset

File: `student_data.csv` (200 rows). The data is **AI-generated (synthetic)**. It was made with Python so that every task can be solved. The code is in `generate_dataset.py`.

| Column | Meaning |
|---|---|
| student_id | Unique ID of the student |
| study_hours | Hours studied per week |
| attendance | Attendance in lectures (%) |
| group_discussion | Took part in group discussion (Yes / No) |
| previous_test_score | Marks out of 100 in the last internal test |
| final_exam_pass | Result of the competitive exam (Pass / Fail) |

## 3. Topics Covered

| # | Task | What I did |
|---|---|---|
| 1 | Understanding the basics | Defined probability, key terms, and gave 3 events from the data |
| 2 | Types of events | Calculated one empirical and one theoretical probability |
| 3 | Random variable | X = number of passes out of 3 students. Made the distribution table, mean and variance |
| 4 | Venn diagram | Study > 10 hours and attendance > 80%, with the overlap |
| 5 | Contingency table | Joint, marginal and conditional probability |
| 6 | Relationships | Explained conditional probability. Tested independence with a chi-square test |
| 7 | Bayes theorem | Found P(Pass given high attendance) |

## 4. Key Results

| Item | Result |
|---|---|
| Overall chance of passing, P(Pass) | 91 / 200 = **0.455** |
| Empirical P(Pass) vs theoretical P(Group discussion = Yes) | 0.455 and 0.50 (observed 0.52) |
| Mean of X (passes out of 3) | **1.365** |
| Variance of X | **0.7439** |
| Students with study > 10 hrs AND attendance > 80% | **50** |
| Joint P(Group discussion AND Pass) | 60 / 200 = **0.30** |
| Conditional P(Pass given Group discussion) | 60 / 104 = **0.577** |
| Group discussion and Pass | **Dependent** (chi-square p-value = 0.0005), not mutually exclusive |
| Bayes: P(Pass given high attendance) | **0.778 (77.8%)** |

### Final Conclusion
1. **Previous test score** has the strongest link with passing.
2. **Group discussion** is next. Pass chance is 57.7% with it and 32.3% without it.
3. **Study hours** and **attendance** also help, but their effect is smaller.
4. Dependence does not prove cause. The data is synthetic, so the results show the method, not real student behaviour.

## 5. Repository Structure

```
Expectation-Decider/
|-- README.md                        <- this file
|-- Expectation_Decider.ipynb        <- practical work (code + markdown + outputs)
|-- Expectation_Decider_Report.pdf   <- theory, formulas and step-by-step calculations
|-- student_data.csv                 <- dataset (200 students)
|-- generate_dataset.py              <- code used to create the dataset
|-- figures/                         <- charts saved by the notebook
```

## 6. How to Run

```bash
pip install pandas numpy matplotlib matplotlib-venn scipy jupyter
jupyter notebook Expectation_Decider.ipynb
```
Keep `student_data.csv` in the same folder as the notebook.

## 7. Video Explanation

Face + screen video (5 to 10 minutes):

**Video link:** `PASTE YOUR GOOGLE DRIVE / YOUTUBE (UNLISTED) LINK HERE`

File name format: `PR1_YourName_GRID.mp4`

## 8. Tools Used
Python, pandas, NumPy, Matplotlib, matplotlib-venn, SciPy, Jupyter Notebook.

---
**Author:** `YOUR NAME` | **GRID:** `YOUR GRID`
