# Mathematics IIB: Long Answer Questions (LAQs)
## Practice Set: Circles & Indefinite Integrals (Telangana Intermediate Board)

---

### I. Circles

#### **Question 1**
**Find the equation of a circle passing through the points $(1, 2), (3, -4),$ and $(5, -6)$.**

**Solution:**
Let the required circle equation be:
$$x^2 + y^2 + 2gx + 2fy + c = 0$$

1. Substituting $(1, 2)$: $1 + 4 + 2g + 4f + c = 0 \implies 2g + 4f + c = -5$ — (1)
2. Substituting $(3, -4)$: $9 + 16 + 6g - 8f + c = 0 \implies 6g - 8f + c = -25$ — (2)
3. Substituting $(5, -6)$: $25 + 36 + 10g - 12f + c = 0 \implies 10g - 12f + c = -61$ — (3)

**Solving the equations:**
- Subtract (1) from (2): $4g - 12f = -20 \implies g - 3f = -5$ — (4)
- Subtract (2) from (3): $4g - 4f = -36 \implies g - f = -9$ — (5)
- Subtract (4) from (5): $2f = -4 \implies f = -2$

**Substituting back:**
- In (5): $g - (-2) = -9 \implies g = -11$
- In (1): $2(-11) + 4(-2) + c = -5 \implies -22 - 8 + c = -5 \implies c = 25$

**Final Equation:**
$$x^2 + y^2 - 22x - 4y + 25 = 0$$

---

#### **Question 2**
**Show that the circles $S \equiv x^2 + y^2 - 6x - 2y + 1 = 0$ and $S' \equiv x^2 + y^2 + 2x - 8y + 13 = 0$ touch each other. Find the point of contact and the equation of common tangent.**

**Solution:**
- **Circle 1 ($S$):** Center $C_1(3, 1)$, Radius $r_1 = \sqrt{3^2 + 1^2 - 1} = 3$
- **Circle 2 ($S'$):** Center $C_2(-1, 4)$, Radius $r_2 = \sqrt{(-1)^2 + 4^2 - 13} = 2$

**Distance between centers:**
$$d = C_1C_2 = \sqrt{(3 - (-1))^2 + (1 - 4)^2} = \sqrt{4^2 + (-3)^2} = 5$$

Since $d = r_1 + r_2$ ($5 = 3 + 2$), the circles **touch each other externally**.

**Point of Contact ($P$):**
Divides $C_1C_2$ in the ratio $r_1 : r_2 = 3 : 2$ internally.
$$P = \left( \frac{3(-1) + 2(3)}{3+2}, \frac{3(4) + 2(1)}{3+2} \right) = \left( \frac{3}{5}, \frac{14}{5} \right)$$

**Equation of Common Tangent:**
$$S - S' = 0$$
$$(x^2 + y^2 - 6x - 2y + 1) - (x^2 + y^2 + 2x - 8y + 13) = 0$$
$$-8x + 6y - 12 = 0 \implies 4x - 3y + 6 = 0$$

---

### II. Indefinite Integrals

#### **Question 3**
**Evaluate $\int \frac{2x+5}{\sqrt{x^2+3x+1}} dx$**

**Solution:**
Let $2x + 5 = A \frac{d}{dx}(x^2+3x+1) + B$
$$2x + 5 = A(2x + 3) + B$$

Equating coefficients:
- $2A = 2 \implies A = 1$
- $3A + B = 5 \implies 3(1) + B = 5 \implies B = 2$

The integral split:
$$I = \int \frac{2x+3}{\sqrt{x^2+3x+1}} dx + 2 \int \frac{1}{\sqrt{x^2+3x+1}} dx$$

**Solving Parts:**
1. $\int \frac{f'(x)}{\sqrt{f(x)}} dx = 2\sqrt{f(x)} \implies I_1 = 2\sqrt{x^2+3x+1}$
2. For $I_2$, complete the square: $x^2 + 3x + 1 = (x + \frac{3}{2})^2 - \frac{5}{4}$
$$I_2 = 2 \int \frac{1}{\sqrt{(x+\frac{3}{2})^2 - (\frac{\sqrt{5}}{2})^2}} dx = 2 \log |(x + \frac{3}{2}) + \sqrt{x^2+3x+1}| + C$$

**Final Result:**
$$2\sqrt{x^2+3x+1} + 2 \log |(x + \frac{3}{2}) + \sqrt{x^2+3x+1}| + C$$

---

#### **Question 4**
**Obtain the reduction formula for $I_n = \int \sin^n x dx$ and hence find $\int \sin^4 x dx$.**

**Solution:**
Write $I_n = \int \sin^{n-1} x \cdot \sin x dx$

Using **Integration by Parts** ($u = \sin^{n-1} x$, $dv = \sin x dx$):
- $I_n = \sin^{n-1} x (-\cos x) - \int (n-1) \sin^{n-2} x \cos x (-\cos x) dx$
- $I_n = -\sin^{n-1} x \cos x + (n-1) \int \sin^{n-2} x (\cos^2 x) dx$
- $I_n = -\sin^{n-1} x \cos x + (n-1) \int \sin^{n-2} x (1 - \sin^2 x) dx$
- $I_n = -\sin^{n-1} x \cos x + (n-1)I_{n-2} - (n-1)I_n$

Rearranging for $I_n$:
$$I_n = \frac{-\sin^{n-1} x \cos x}{n} + \frac{n-1}{n} I_{n-2}$$

**Evaluating $I_4$:**
- $I_4 = \frac{-\sin^3 x \cos x}{4} + \frac{3}{4} I_2$
- $I_2 = \frac{-\sin x \cos x}{2} + \frac{1}{2} I_0$ (where $I_0 = \int 1 dx = x$)

**Substituting back:**
$$I_4 = -\frac{\sin^3 x \cos x}{4} - \frac{3\sin x \cos x}{8} + \frac{3x}{8} + C$$
