# 🧠 Fuzzy Logic Expert System: Academic Performance Evaluator

<div align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/scikit--fuzzy-FF8C00?style=for-the-badge&logo=python&logoColor=white" alt="scikit-fuzzy" />
  <img src="https://img.shields.io/badge/AI-Expert_Systems-00599C?style=for-the-badge" alt="Expert Systems" />
  <img src="https://img.shields.io/badge/Logic-Mamdani_Inference-8B0000?style=for-the-badge" alt="Mamdani" />
</div>

## 📌 Executive Summary
This repository showcases the development of an **Expert System** using **Fuzzy Logic** to evaluate student academic performance. 

While modern Machine Learning portfolios often focus exclusively on data-driven predictive modeling, this project highlights proficiency in **Rule-Based AI**. Traditional academic evaluation relies on rigid, boolean scoring systems (e.g., exactly 59 is "Average", but 60 is "Good"). This system applies fuzzy set theory to model the uncertainty and approximate reasoning of human grading, creating a flexible, robust, and mathematically fair assessment algorithm that reduces grading bias.

---

## ⚙️ AI Architecture & Methodology

The system is built on a **Mamdani Fuzzy Inference System (FIS)**, transforming subjective grading heuristics into a computable mathematical model.

### 1. Fuzzification (Input Layer)
Crisp numerical data is converted into linguistic variables using **Trapezoidal Membership Functions** (`trapmf`). 
* **Input Parameters:** `Attendance` (%), `Internal_Marks` (0-100), `External_Marks` (0-100).
* **Linguistic Categories:** `Poor`, `Average`, `Good`, `Very Good`, `Excellent`.

### 2. Fuzzy Knowledge Base (Rules Engine)
The core of the expert system is a robust matrix of **43 "If-Then" inference rules** that map every possible combination of student inputs to a fair outcome.
* *Example Rule:* `IF (Attendance is Poor) AND (External_Marks is Good) AND (Internal_Marks is Very Good) THEN (Performance is Good)`

### 3. Defuzzification (Output Layer)
The fuzzy outputs are aggregated using the **Maximum of Minimum (Max-Min)** method, computing the centroid to return a single, crisp `Performance` score.

---

## 📊 Statistical Validation & Results
To prove the algorithm's viability, the fuzzy logic evaluator was tested against a historical dataset of **54 students**.
* **T-Test Validation:** A statistical T-test confirmed there is **no significant difference** between conventional rigid grading methods and the fuzzy logic system. 
* **Conclusion:** The model accurately mirrors human grading expectations while successfully capturing nuances and edge-cases that traditional threshold grading overlooks.

---

## 🚀 How to Run the Project

**1. Clone the repository**
```bash
git clone [https://github.com/aansikkaw/fuzzy-logic-evaluation.git](https://github.com/aansikkaw/fuzzy-logic-evaluation.git)
cd fuzzy-logic-evaluation
