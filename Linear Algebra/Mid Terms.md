# Mid Terms

# Linear Algebra — Complete Guide (From Zero)

---

## PART 1: MATRICES — INTRODUCTION

A **matrix** is a rectangular grid of numbers enclosed in brackets.

```
        [ 2   3 ]
A   =   [ 1   4 ]
```

This is a **2×2 matrix** — 2 rows, 2 columns. Order = rows × columns.

Elements are written as aᵢⱼ (row i, column j):

```
        [ a11   a12   a13 ]
A   =   [ a21   a22   a23 ]
```

---

### Types of Matrices

**Row matrix** — only 1 row:

```
[ 1   1   6 ]
```

**Column matrix** — only 1 column:

```
[ 1 ]
[ 4 ]
[ 2 ]
```

**Rectangular matrix** — rows ≠ columns:

```
[ 1   1 ]
[ 3   7 ]
[ 7  -7 ]
```

(3 rows, 2 columns → 3×2)

**Square matrix** — rows = columns:

```
[ 1   1   1 ]
[ 9   9   0 ]
[ 6   6   1 ]
```

(3×3 — the "main diagonal" is 1, 9, 1)

**Diagonal matrix** — square, everything zero EXCEPT the main diagonal:

```
[ 1   0   0 ]
[ 0   2   0 ]
[ 0   0   1 ]
```

**Identity matrix (I)** — diagonal matrix with all 1s on the diagonal:

```
[ 1   0   0 ]
[ 0   1   0 ]
[ 0   0   1 ]
```

**Null/Zero matrix (0)** — every element is 0:

```
[ 0   0   0 ]
[ 0   0   0 ]
[ 0   0   0 ]
```

**Upper triangular** — everything BELOW the diagonal is 0:

```
[ 1   8   9 ]
[ 0   1   6 ]
[ 0   0   3 ]
```

**Lower triangular** — everything ABOVE the diagonal is 0:

```
[ 1   0   0 ]
[ 2   1   0 ]
[ 5   2   3 ]
```

**Scalar matrix** — diagonal matrix where ALL diagonal elements are the SAME number:

```
[ 6   0   0 ]
[ 0   6   0 ]
[ 0   0   6 ]
```

---

## PART 2: MATRIX OPERATIONS

### Addition / Subtraction

Only works if **both matrices are the same size**. Add/subtract element by element.

```
    [ 2   3 ]       [ 5  -1 ]       [ 2+5   3+(-1) ]       [ 7   2 ]
A = [ 1   4 ],  B = [ 2   3 ]  →  A+B = [ 1+2   4+3   ]  =  [ 3   7 ]
```

```
                              [ 2-5   3-(-1) ]       [ -3   4 ]
                    A-B  =    [ 1-2   4-3    ]   =   [ -1   1 ]
```

**Rules:** A+B = B+A (commutative), A+(B+C) = (A+B)+C (associative)

### Scalar Multiplication

Multiply every element by the scalar k.

```
        [ 3  -1 ]                    [ 12  -4 ]
k=4, A =[ 2   1 ]   →   4A   =       [  8   4 ]
        [ 2  -3 ]                    [  8 -12 ]
        [ 4   1 ]                    [ 16   4 ]
```

### Matrix Multiplication

**Rule:** columns of A must equal rows of B. Result size = (rows of A) × (columns of B).

Method: **row of A × column of B**, multiply matching positions, then add.

```
    [ 1   2 ]       [ 2   0 ]
A = [ 3   4 ],  B = [ 1   3 ]

AB = [ (1×2)+(2×1)   (1×0)+(2×3) ]   =   [ 4    6 ]
     [ (3×2)+(4×1)   (3×0)+(4×3) ]       [ 10  12 ]

BA = [ (2×1)+(0×3)   (2×2)+(0×4) ]   =   [ 2    4 ]
     [ (1×1)+(3×3)   (1×2)+(3×4) ]       [ 10  14 ]
```

**AB ≠ BA** — matrix multiplication is NOT commutative. This is a guaranteed exam point.

**Also remember:**

- If AB = 0, it does NOT mean A = 0 or B = 0
- If AB = AC, it does NOT mean B = C
- IA = AI = A (identity matrix acts like "1")

### Transpose (Aᵀ)

Flip rows and columns.

```
        [ 2   4   7 ]                     [ 2   5 ]
A   =   [ 5   3   1 ]     →      Aᵀ   =   [ 4   3 ]
                                           [ 7   1 ]
```

(2×3 becomes 3×2)

**Properties:**

- (A+B)ᵀ = Aᵀ+Bᵀ
- (AB)ᵀ = BᵀAᵀ ← order REVERSES
- (kA)ᵀ = kAᵀ
- (Aᵀ)ᵀ = A

### Symmetric & Skew-Symmetric

**Symmetric:** Aᵀ = A (mirror image across the diagonal)

```
    [ 20   120   200 ]
A = [120    10   150 ]     ← A = Aᵀ (check: a12=120=a21, a13=200=a31, a23=150=a32)
    [200   150    30 ]
```

**Skew-symmetric:** Aᵀ = −A (diagonal must be all zeros)

```
    [ 0    1   -3 ]
B = [-1    0   -2 ]        ← Aᵀ = -A (check: a12=1, a21=-1 → negatives of each other)
    [ 3    2    0 ]
```

---

## PART 3: DETERMINANTS

Only defined for **square matrices**. Written det(A) or |A|.

### 2×2 Determinant

```
    [ 4   3 ]
A = [ 2   5 ]     →     |A| = (4×5) - (3×2) = 20 - 6 = 14
```

Formula: |A| = a₁₁a₂₂ − a₁₂a₂₁

### 3×3 Determinant (expansion along Row 1)

```
    [ 1   2   3 ]
A = [ 0   4   5 ]
    [ 1   0   6 ]
```

Formula:

```
|A| = a11(a22·a33 - a23·a32) - a12(a21·a33 - a23·a31) + a13(a21·a32 - a22·a31)
```

Substituting:

```
|A| = 1(4×6 - 5×0) - 2(0×6 - 5×1) + 3(0×0 - 4×1)
    = 1(24) - 2(-5) + 3(-4)
    = 24 + 10 - 12 = 22
```

### Key Properties (memorize — direct MCQs)

- Two identical rows/columns → det = 0
- det(2A) for an n×n matrix = 2ⁿ × det(A)
- det(Aᵀ) = det(A)
- If one row is a multiple of another → det = 0
- Swapping two rows flips the sign of the determinant

---

## PART 4: MINORS, COFACTORS & ADJOINT

### Minors

Delete the row and column of an element → the determinant of what's left is the **minor** Mᵢⱼ.

```
    [ 2   3   1 ]
A = [ 4   5   7 ]
    [ 6   8   9 ]
```

To find M₁₁ (minor of a₁₁=2): delete row 1, column 1 →

```
        [ 5   7 ]
        [ 8   9 ]    →    M11 = (5×9)-(8×7) = 45-56 = -11
```

### Cofactors

```
Cᵢⱼ = (-1)^(i+j) × Mᵢⱼ
```

Sign pattern (checkerboard):

```
[ +  -  + ]
[ -  +  - ]
[ +  -  + ]
```

So C₁₁ = (−1)²×M₁₁ = +M₁₁ = −11

### Adjoint — Full Worked Example

```
    [ 1   2   3 ]
A = [ 4   5   6 ]
    [ 7   8   9 ]
```

**Step 1 — find all 9 cofactors:**

```
C11 = 5×9-6×8 = -3        C12 = -(4×9-6×7) = 6       C13 = 4×8-5×7 = -3
C21 = -(2×9-3×8) = 6      C22 = 1×9-3×7 = -6          C23 = -(1×8-2×7) = 3
C31 = 2×6-3×5 = -3        C32 = -(1×6-3×4) = 6        C33 = 1×5-2×4 = -3
```

**Step 2 — build the cofactor matrix:**

```
    [ -3    6   -3 ]
C = [  6   -6    3 ]
    [ -3    6   -3 ]
```

**Step 3 — transpose it → this is the adjoint:**

```
             [ -3    6   -3 ]
adj(A)   =   [  6   -6    6 ]
             [ -3    3   -3 ]
```

**Key identity:** A · adj(A) = adj(A) · A = |A| · I  ← this is WHY adjoint gives you the inverse.

**2×2 Shortcut** (fast method — use this whenever the matrix is 2×2):

```
        [ a   b ]                    [  d   -b ]
A   =   [ c   d ]     →   adj(A) =   [ -c    a ]
```

Just swap the main diagonal, and flip the sign of the other two.

---

## PART 5: INVERSE OF A MATRIX

```
A⁻¹ = adj(A) / |A|
```

**Condition:** Inverse exists ONLY if |A| ≠ 0.

- |A| ≠ 0 → **non-singular** (invertible)
- |A| = 0 → **singular** (NO inverse — always check this first!)

### 2×2 Worked Example

```
    [ 2   1 ]
A = [ 3   2 ]
```

|A| = (2×2)-(1×3) = 4-3 = 1

```
              [  2   -1 ]              [  2   -1 ]
A⁻¹ = 1/1 ×   [ -3    2 ]     =        [ -3    2 ]
```

**Verify:** A·A⁻¹ should equal I. Always do this check if you have time.

### 3×3 Worked Example

```
    [ 2  -1   0 ]
A = [-1   2  -1 ]
    [ 0  -1   2 ]
```

**Step 1 — determinant:**

```
det(A) = 2(2×2-(-1)×(-1)) - (-1)((-1)×2-(-1)×0) + 0
       = 2(4-1) + 1(-2)
       = 6 - 2 = 4
```

**Step 2 — cofactors → cofactor matrix:**

```
    [ 3   2   1 ]
C = [ 2   4   2 ]
    [ 1   2   3 ]
```

(this one happens to be symmetric, so adj(A) = Cᵀ = C)

**Step 3 — divide every element by |A|=4:**

```
        [ 3/4   1/2   1/4 ]
A⁻¹  =  [ 1/2    1    1/2 ]
        [ 1/4   1/2   3/4 ]
```

---

## PART 6: SOLVING LINEAR EQUATIONS — 3 METHODS

A system like:

```
2x + y = 5
x + 3y = 7
```

becomes **AX = B**:

```
    [ 2   1 ]        [ x ]         [ 5 ]
A = [ 1   3 ],   X = [ y ],   B =  [ 7 ]
```

### Method 1 — Matrix Inversion: X = A⁻¹B

```
|A| = (2×3)-(1×1) = 5

           1   [  3  -1 ]
A⁻¹  =    ---  [        ]
           5   [ -1   2 ]
```

```
              [  3  -1 ]   [ 5 ]        [ (3×5)+(-1×7) ]       [ 8 ]
X = A⁻¹B = (1/5)[        ] [   ]  = (1/5)[               ]  =  (1/5)[   ]
              [ -1   2 ]   [ 7 ]        [ (-1×5)+(2×7)  ]      [ 9 ]

           [ 1.6 ]
X   =      [ 1.8 ]     →   x = 1.6,  y = 1.8
```

**Check:** 2(1.6)+1.8 = 5 ✓, and 1.6+3(1.8) = 7 ✓

### Method 2 — Gauss Elimination

**Augmented matrix:**

```
[ 1    1  |  5 ]
[ 2   -1  |  1 ]
```

**Row operation R2 → R2 − 2R1:**

```
[ 1    1  |  5 ]
[ 0   -3  | -9 ]
```

This is Row Echelon Form (REF) — zeros below the diagonal.

**Back-substitute:** from row 2: −3y = −9 → y = 3
Substitute into row 1: x + 3 = 5 → x = 2

**The Three Possible Outcomes:**

```
Case 1: No contradiction, every variable has a pivot  →  Unique solution
Case 2: A row becomes all zeros (0 = 0)                →  Infinitely many solutions
Case 3: A contradictory row appears (0 = 5)            →  No solution
```

### Method 3 — Gauss-Jordan

Same row operations, but continue until you reach the **identity matrix** on the left (Reduced Row Echelon Form / RREF). No back-substitution needed — read the answer directly.

**Worked Example:**

```
2x + y + 2z = 10
 x + 2y +  z =  8
3x +  y -  z =  2
```

```
[ 2   1   2  | 10 ]
[ 1   2   1  |  8 ]
[ 3   1  -1  |  2 ]
```

After full row reduction (swap rows, eliminate, normalize) → final RREF:

```
[ 1   0   0  |  1 ]
[ 0   1   0  |  2 ]
[ 0   0   1  |  3 ]
```

Read directly: **x = 1, y = 2, z = 3**

**Comparison:**

```
Gaussian Elimination        |  Gauss-Jordan
Stops at REF                |  Continues to RREF
Needs back-substitution     |  No back-substitution needed
Faster to set up            |  Gives the answer directly
```

---

## PART 7: VECTORS — BASICS

A vector has both **magnitude** (length) and **direction**. Written as:

```
v = (3, 4)
```

### Magnitude

```
|v| = √(x² + y²)
|v| = √(3² + 4²) = √(9+16) = √25 = 5
```

### Unit Vector (direction only, length 1)

```
unit vector = v / |v|

for v = (6,8): |v| = √(36+64) = √100 = 10
unit vector = (6/10, 8/10) = (0.6, 0.8)
```

### Dot Product

```
u·v = u1v1 + u2v2 + u3v3 + ...

u = (2,3,-1), v = (1,-2,4)
u·v = (2×1)+(3×-2)+(-1×4) = 2-6-4 = -8
```

### Orthogonal (Perpendicular) Check

If u·v = 0 → vectors are orthogonal.

```
u = (1,2,1), v = (2,-1,0)
u·v = (1×2)+(2×-1)+(1×0) = 2-2+0 = 0   →  Orthogonal ✓
```

### Angle Between Vectors

```
cos θ = (u·v) / (|u| × |v|)
```

### Parallel Check

u and v are parallel if u = k·v for some scalar k.

```
u = (2,-1,3), v = (4,-2,6)
Check: is v = 2u?  2×(2,-1,3) = (4,-2,6) = v   →  Yes, parallel
```

---

## PART 8: SPAN OF VECTORS

**Span{v1, v2, ...}** = every vector you can build by combining v1, v2, ... with scalar multiples and addition.

**"Does w belong to span{u,v}?"** → solve a·u + b·v = w for a, b. If a real solution exists → yes.

### Worked Example

Does w=(5,1) belong to span{(2,1),(1,1)}?

```
a(2,1) + b(1,1) = (5,1)

2a + b = 5
 a + b = 1
```

Subtract: a = 4. Then from row 2: b = 1−4 = −3.

**Check:** 2(4)+(-3) = 5 ✓

→ **Yes**, w = 4(2,1) − 3(1,1)

**Key insight:** In R², if two vectors are NOT parallel, their span = all of R² (they can build any vector). If they ARE parallel, span is just a line.

---

## PART 9: LINEAR DEPENDENCE & INDEPENDENCE

Set up: c₁v₁ + c₂v₂ + ... + cₙvₙ = **0**

- Only solution is all cᵢ = 0 → **linearly independent**
- Another solution exists (not all zero) → **linearly dependent**

### 2 Vectors — Quick Check

Dependent if and only if one is a scalar multiple of the other.

```
u = (1,2), v = (2,4)
v = 2u  →  Linearly dependent
```

### 3+ Vectors — Determinant Test

Arrange as rows of a matrix, find the determinant.

- det ≠ 0 → linearly independent
- det = 0 → linearly dependent

```
Vectors: (1,0,1), (0,1,1), (1,1,2)

    [ 1   0   1 ]
    [ 0   1   1 ]
    [ 1   1   2 ]

det = 1(1×2-1×1) - 0(0×2-1×1) + 1(0×1-1×1)
    = 1(1) - 0 + 1(-1)
    = 1 - 1 = 0

→  det = 0  →  Linearly dependent
```

---

## THE FULL CONCEPT MAP

```
Matrices (add, multiply, transpose)
        |
        v
Determinants (needed for inverse)
        |
        v
Minors --> Cofactors --> Adjoint
        |
        v
Inverse:  A⁻¹ = adj(A) / |A|
        |
        v
Solve AX = B  -- 3 methods:
   1. X = A⁻¹B          (uses everything above)
   2. Gauss Elimination  (row ops --> back-substitute)
   3. Gauss-Jordan       (row ops --> read off directly)

Vectors (separate but related topic)
        |
        v
Span (which vectors can you "build"?)
        |
        v
Linear Independence (determinant test tells you if vectors are redundant)
```

---

## EXTRA PRACTICE QUESTIONS

**Matrices/Determinants**

1. Find AB and BA for A=[[2,0],[1,3]], B=[[1,4],[2,1]]. Are they equal?
2. Evaluate det([[2,3,1],[1,0,2],[3,1,4]])
3. Find adj(A) and A⁻¹ for A=[[3,2],[1,4]]

**Linear Equations**
4. Solve using matrix inversion: 3x+2y=12, x−y=1
5. Solve using Gauss-Jordan: x+y+z=6, x−y+z=2, x+2y−z=1

**Vectors / Span / Independence**
6. Find the angle between u=(1,1,0) and v=(0,1,1)
7. Does (7,2) belong to span{(1,1),(2,1)}?
8. Check if (1,1,0), (0,1,1), (1,0,1) are linearly independent using the determinant test