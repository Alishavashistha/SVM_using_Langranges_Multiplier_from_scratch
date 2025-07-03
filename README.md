# 🧠 SVM from Scratch using Quadratic Programming

This project demonstrates how to implement a **Support Vector Machine (SVM)** classifier from scratch using **Quadratic Programming (QP)**. The approach directly solves the SVM dual problem using numerical optimization, instead of relying on libraries like `scikit-learn`.

---

## 📘 File Description

- `svm_qp.ipynb`:  
  A Jupyter notebook that:
  - Explains the SVM optimization objective
  - Formulates the dual QP problem
  - Solves it using a QP solver (`cvxopt`)
  - Visualizes support vectors and decision boundaries

---

## 🧮 Core Concepts Covered

- Linear SVM optimization (hard-margin or soft-margin)
- QP formulation of the SVM dual problem:
  
  \[
  \max_{\alpha} \sum_i \alpha_i - \frac{1}{2} \sum_i \sum_j \alpha_i \alpha_j y_i y_j \langle x_i, x_j \rangle
  \]

  Subject to:
  - \( \sum_i \alpha_i y_i = 0 \)
  - \( \alpha_i \geq 0 \) (and \( \alpha_i \leq C \), if soft-margin)

- Use of **cvxopt.solvers.qp** to solve the QP problem
- Finding the support vectors and decision boundary

---

## ✅ Requirements

Install required libraries using:

```bash
pip install numpy matplotlib cvxopt
