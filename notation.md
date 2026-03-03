# 📘 Direct Stiffness Method — Notation Convention

To maintain consistency throughout the course, we adopt the following rules.

These need to be implemented consistently across lectures

---

## 🔹 1. General Rules

- **Vectors** → bold lowercase
- **Matrices** → bold uppercase
- **Element stiffness matrices** → lowercase $ \mathbf{k} $
- **Assembled global stiffness matrix** → uppercase $ \mathbf{K} $

---

## 🔹 2. Subscripts and Superscripts

- Subscript $ i $ → element index
- Subscript $ l $ → local coordinate system
- Subscript $ g $ → global coordinate system (element level)
- No subscript → assembled global system
- Superscript $ F $ → fixed-end force

---

## 🔹 3. Local Element Equation (Element $ i $)

$$
\mathbf{q}_i = \mathbf{k}_{l,i} \mathbf{v}_i + \mathbf{q}_i^{\,F}
$$

Where:

- $\mathbf{v}_i$ = local element DOFs
- $\mathbf{q}_{i}$ = local element end forces
- $\mathbf{k}_{l,i}$ = local element stiffness matrix
- $\mathbf{q}_i^{\,F}$ = local fixed-end force vector

---

## 🔹 4. Global Element Equation (Element $ i $)

$$
\mathbf{f}_i = \mathbf{k}_{g,i} \mathbf{u}_i + \mathbf{f}_i^{\,F}
$$

Where:

- $\mathbf{u}_i$ = element DOFs in global coordinates
- $\mathbf{f}_i$ = element nodal forces in global coordinates
- $\mathbf{k}_{g,i} = \mathbf{T}_i^T \mathbf{k}_{l,i} \mathbf{T}_i$
- $\mathbf{f}_i^{\,F} = \mathbf{T}_i^T \mathbf{q}_i^{\,F}$

---

## 🔹 5. Global Assembled System

$$
\mathbf{f} = \mathbf{K}\mathbf{u} + \mathbf{f}^{\,F}
$$

Where:

- $ \mathbf{u} $ = global displacement vector
- $ \mathbf{f} $ = global nodal force vector
- $ \mathbf{K} $ = assembled global stiffness matrix
- $ \mathbf{f}^{F} $ = assembled global fixed-end forces

---

## 🔹 6. Summary Table

| Level          | Displacements  | Forces         | Stiffness          |
| -------------- | -------------- | -------------- | ------------------ |
| Local element  | $\mathbf{v}_i$ | $\mathbf{q}_i$ | $\mathbf{k}_{l,i}$ |
| Global element | $\mathbf{u}_i$ | $\mathbf{f}_i$ | $\mathbf{k}_{g,i}$ |
| Global system  | $\mathbf{u}$   | $\mathbf{f}$   | $\mathbf{K}$       |

---

This convention:

- Avoids stacked superscripts
- Keeps vectors lowercase and matrices uppercase
- Clearly separates element-level and assembled quantities
- Scales cleanly to 2D trusses, beams, frames, and 3D systems
