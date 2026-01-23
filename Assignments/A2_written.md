# CEE6501 — Written Assignment, Week 2

**Assigned:** 01/23/2026 (Week 2)

**Due:** 02/02/2026

**Canvas Submission Link:** <https://gatech.instructure.com/courses/517856/assignments/2320534>

## Logistics

### 📄 Assignment Format

This is a **written assignment**, not a coding assignment.

- Complete the assignment **by hand or typed up**
- You may write:
  - in a markdown file
  - on paper
  - on a tablet
  - using a stylus or digital note-taking app
- After completing the assignment, **scan or export your work** and upload it to Canvas

You may use **any format you prefer**, but your submission \*_must be neat and legible_

### 📤 Submission Instructions

- Upload **one file** to Canvas
- Accepted formats: **PDF, PNG, or JPG**
- Make sure all pages are clearly visible and in the correct order

### ✅ Checklist Before Submitting

- [ ] Assignment completed by hand
- [ ] Writing is neat and legible
- [ ] Title block provided on each page
- [ ] All questions answered
- [ ] File uploaded successfully to Canvas

### 🤝 Collaboration / AI tools

You may discuss concepts with classmates and you may use AI tools to help you learn, but **your submitted work must be
written by you and you must understand it**. If you used outside help, add a short note in the final reflection cell.

---

### Question 1 — From Equations to Matrix Form (10 Points)

Consider the following system of four equations in four unknowns:

$$
\begin{aligned}
2x_1 - x_2 + 0x_3 + 3x_4 &= 7 \\
-4x_1 + 5x_2 + x_3 - 2x_4 &= -6 \\
x_1 + 2x_2 + 4x_3 + 0x_4 &= 10 \\
0x_1 - 3x_2 + 2x_3 + x_4 &= 1
\end{aligned}
$$

1. Write the system in matrix form $\mathbf{A}\mathbf{x}=\mathbf{b}$.
2. Clearly identify $\mathbf{A}$, $\mathbf{x}$, and $\mathbf{b}$.
3. State the dimensions of $\mathbf{A}$, $\mathbf{x}$, and $\mathbf{b}$.

---

### Question 2 — 2D Linear Transformations (10 Points)

Let the vector

$$
\mathbf{x}=
\begin{bmatrix}
1\\
2
\end{bmatrix}
$$

Consider the following three transformation matrices:

$$
\mathbf{T}_1=
\begin{bmatrix}
2 & 0\\
0 & 1
\end{bmatrix}
\qquad
\mathbf{T}_2=
\begin{bmatrix}
0 & -3\\
3 & 0
\end{bmatrix}
\qquad
\mathbf{T}_3=
\begin{bmatrix}
1 & 1\\
0 & 1
\end{bmatrix}
$$

1. Compute $\mathbf{y}_k=\mathbf{T}_k\mathbf{x}$ for $k=1,2,3$.
2. On a single set of axes, sketch the original vector $\mathbf{x}$ and the three transformed vectors
   $\mathbf{y}_1,\mathbf{y}_2,\mathbf{y}_3$.

---

### Question 3 — Matrix Multiplication (10 Points)

Let

$$
\mathbf{A}=
\begin{bmatrix}
1 & -2 \\
0 & 3 \\
4 & 1 \\
-1 & 2
\end{bmatrix}
\qquad
\mathbf{B}=
\begin{bmatrix}
2 & 0 & -1 & 3 & 1 \\
-2 & 4 & 5 & 0 & -3
\end{bmatrix}
$$

1. State the dimensions of $\mathbf{A}$, $\mathbf{B}$, and $\mathbf{A}\mathbf{B}$.
2. Compute the product $\mathbf{C}=\mathbf{A}\mathbf{B}$.
3. Show your work clearly for **two entries** of $\mathbf{C}$:
   - $c_{11}$
   - $c_{34}$

---

### Question 4 — Block Matrix Multiplication (10 Points)

Consider the matrices

$$
\mathbf{K}\in\mathbb{R}^{6\times 6}
\qquad
\mathbf{X}\in\mathbb{R}^{6\times 3}
$$

Matrix $\mathbf{K}$ is partitioned into four blocks:

- $\mathbf{K}_{11}\in\mathbb{R}^{4\times 4}$
- $\mathbf{K}_{12}\in\mathbb{R}^{4\times 2}$
- $\mathbf{K}_{21}\in\mathbb{R}^{2\times 4}$
- $\mathbf{K}_{22}\in\mathbb{R}^{2\times 2}$

and matrix $\mathbf{X}$ is partitioned compatibly as:

- $\mathbf{X}_1\in\mathbb{R}^{4\times 3}$
- $\mathbf{X}_2\in\mathbb{R}^{2\times 3}$

1. Sketch out the partitioning on the matrices (you dont need to write out all the entries). Write the **partitioned
   forms** of $\mathbf{K}$ and $\mathbf{X}$ using block notation,

2. Write the block multiplication expression for

   $$
   \mathbf{Y}=\mathbf{K}\mathbf{X}
   $$

   in terms of the submatrices.

3. For each product appearing in your expression, state its dimensions. For example:

   $$
   \mathbf{K}_{12}\mathbf{X}_2:\quad (4\times 2)(2\times 3)=(4\times 3)
   $$

4. State the final dimension of $\mathbf{Y}$.

You do **not** need to perform any numerical multiplication — the goal is to correctly set up the block multiplication
and verify dimensional consistency.

---

### Question 5 — Gauss–Jordan (10 Points)

Let

$$
\mathbf{A}=
\begin{bmatrix}
2 & 1 & 0 & 1 \\
1 & 3 & 1 & 0 \\
0 & 2 & 4 & 1 \\
1 & 0 & 1 & 2
\end{bmatrix}
\qquad
\mathbf{b}=
\begin{bmatrix}
1\\2\\3\\4
\end{bmatrix}
$$

1. Form the augmented matrix $[\mathbf{A}\,|\,\mathbf{I}]$.
2. Perform Gauss–Jordan elimination **only through the first two pivots** (i.e., make the first two pivot columns match
   $\mathbf{I}$).
3. Clearly show your row operations and the partially reduced matrix.

---

### Question 6 — LU Decomposition (10 Points)

Using the same matrix $\mathbf{A}$ from Question 5:

1. Perform Gaussian elimination (no pivoting, i.e., swapping rows) to produce $\mathbf{U}$.
2. Record the elimination multipliers to construct $\mathbf{L}$ (unit diagonal).
3. Verify your result by computing (by hand) the product $\mathbf{L}\mathbf{U}$ and checking that it equals
   $\mathbf{A}$.

---

### Question 7 — Cholesky Factorization (20 Points)

Let the symmetric positive definite matrix

$$
\mathbf{K}=
\begin{bmatrix}
4 & 1 & 0 & 0 \\
1 & 3 & 1 & 0 \\
0 & 1 & 2 & 1 \\
0 & 0 & 1 & 2
\end{bmatrix}
$$

1. Compute the Cholesky factorization $\mathbf{K}=\mathbf{L}\mathbf{L}^T$.
2. Solve $\mathbf{K}\mathbf{x}=\mathbf{b}$ for each right-hand side:

$$
\mathbf{b}_{1}=
\begin{bmatrix}
1\\0\\0\\0
\end{bmatrix}
\qquad
\mathbf{b}_{2}=
\begin{bmatrix}
0\\1\\0\\0
\end{bmatrix}
\qquad
\mathbf{b}_{3}=
\begin{bmatrix}
1\\1\\1\\1
\end{bmatrix}
$$

For each solve, show:

- forward substitution $\mathbf{L}\hat{\mathbf{b}}=\mathbf{b}$
- back substitution $\mathbf{L}^T\mathbf{x}=\hat{\mathbf{b}}$

---

### Question 8 — Point Jacobi Iterations (20 Points)

Using the SPD system from Question 7 and $\mathbf{b}_{1}$:

1. Write the Point Jacobi update formula for the 4 unknowns.
2. Perform **two Jacobi iterations** starting from
   $$
   \mathbf{x}^{(0)}
   =
   \begin{bmatrix}
   0\\
   0\\
   0\\
   0
   \end{bmatrix}
   $$
3. Perform **two Jacobi iterations** starting from
   $$
   \mathbf{x}^{(0)}
   =
   \frac{1}{2}\mathbf{x}^\ast
   =
   \frac{1}{2}
   \begin{bmatrix}
   x_1^\ast\\
   x_2^\ast\\
   x_3^\ast\\
   x_4^\ast
   \end{bmatrix}
   $$
   where $\mathbf{x}^\ast$ is your solution from Question 7 for $\mathbf{b}_{1}$.
4. For each starting guess, report the residual norm
   $$
   \|\mathbf{K}\mathbf{x}^{(m)}-\mathbf{b}^{(1)}\|_2
   $$
   after each iteration ($m=1$ and $m=2$) (you may approximate to 2–3 decimals).
