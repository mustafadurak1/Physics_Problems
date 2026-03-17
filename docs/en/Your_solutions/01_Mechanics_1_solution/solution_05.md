# Mechanics I: Study Notes & Problem Solutions
**Student:** Mustafa Duhan Durak  
**Topic:** Kinematics, Dynamics, and Vector Calculus

---

## 1. Projectile Motion
**Problem:** $v_0 = 100 \text{ m/s}$ at $\theta = 37^\circ$. (Assume $g = 9.8 \text{ m/s}^2$)

### Differential Equations
* **Horizontal ($x$):** $\frac{d^2x}{dt^2} = 0$
* **Vertical ($y$):** $\frac{d^2y}{dt^2} = -9.8$

### Results
* **Time of Flight ($t_f$):** $\frac{2v_0 \sin\theta}{g} \approx \mathbf{12.24 \text{ s}}$
* **Max Height ($H$):** $\frac{(v_0 \sin\theta)^2}{2g} \approx \mathbf{183.67 \text{ m}}$
* **Range ($R$):** $\frac{v_0^2 \sin(2\theta)}{g} \approx \mathbf{980.88 \text{ m}}$

---

## 2. Range Optimization
To find the maximum range $R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$:
1. Differentiate with respect to $\theta$: $\frac{dR}{d\theta} = \frac{v_0^2}{g} [2\cos(2\theta)]$.
2. Set to zero: $\cos(2\theta) = 0 \implies 2\theta = 90^\circ$.
3. **Conclusion:** Maximum range is achieved at $\mathbf{\theta = 45^\circ}$.

---

## 3. Path Intersection: Alice vs. Bob
* **Alice:** $A(t) = (2+t, 8-3t)$
* **Bob:** $B(t) = (2t-1, 2t+2)$

**Analysis:**
Setting $x_A = x_B \implies 2+t = 2t-1 \implies t = 3 \text{ s}$.  
At $t=3$: $y_A = -1$ and $y_B = 8$.  
**Result:** Since $y_A \neq y_B$, there is **no collision**.

---

## 4. Vector Calculus
Given position $\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$:
* **Velocity:** $\vec{v}(t) = \frac{d\vec{r}}{dt} = \mathbf{6t\hat{i} + (5 - 16t)\hat{j}}$
* **Acceleration:** $\vec{a}(t) = \frac{d\vec{v}}{dt} = \mathbf{6\hat{i} - 16\hat{j}}$

---

## 5. Relative Velocity (River Crossing)
* **Heading Angle:** $\sin\theta = \frac{2}{5} \implies \theta = \arcsin(0.4) \approx \mathbf{23.58^\circ}$ (West of North).
* **Crossing Velocity:** $v_{net} = \sqrt{5^2 - 2^2} = \sqrt{21} \approx \mathbf{4.58 \text{ m/s}}$.
* **Time to Cross:** $t = \frac{200}{4.58} \approx \mathbf{43.67 \text{ s}}$.

---

## 6. Variable Velocity
$v(t) = t^2 + 2t - 5$ with $x(0)=4$.
* **Position:** $x(t) = \int v(t)dt = \frac{t^3}{3} + t^2 - 5t + 4$. At $t=3$, **$x = 7$**.
* **Acceleration:** $a(t) = \frac{dv}{dt} = 2t + 2$. At $t=3$, **$a = 8 \text{ m/s}^2$**.

---

## 7. Trajectory Elimination
Given $x = 2t^2$ and $y = 3t^3$:
1. $t = \sqrt{x/2}$.
2. Substitute into $y$: $y = 3(x/2)^{3/2} \implies \mathbf{27x^3 = 4y^2}$.
3. **Acceleration:** $\vec{a}(t) = (4, 18t)$. (Not constant as it depends on $t$).

---

## 8. Circular Motion
$\omega = \frac{2\pi}{86400} \text{ rad/s}$, $R = 6,378,000 \text{ m}$.
* **Centripetal Acceleration:** $a_c = \omega^2 R \approx \mathbf{0.034 \text{ m/s}^2}$.

---

## 9. Momentum Comparison ($p = mv$)
* **Fly:** $0.002 \text{ kg} \cdot 10 \text{ m/s} = 0.02 \text{ kg}\cdot\text{m/s}$.
* **Tennis Ball:** $0.060 \text{ kg} \cdot 1 \text{ m/s} = 0.06 \text{ kg}\cdot\text{m/s}$.
**Result:** The **tennis ball** has greater momentum.

---

## 10. Kinematics (3D Helix)
$\vec{r}(t) = (a \cos\omega t, b \sin\omega t, bt)$
* **Trajectory:** An **Elliptical Helix**.
* **Path Length:** $s = \int_0^{t_0} \sqrt{(a\omega\sin\omega t)^2 + (b\omega\cos\omega t)^2 + b^2} \, dt$.
