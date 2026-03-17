## 5. Relative Velocity (River Crossing Problem)

### **Problem Statement**
A river flows east at $2 \text{ m/s}$. A boat with a speed of $5 \text{ m/s}$ in still water wants to travel directly north. 
* **River Width:** $200 \text{ meters}$
* **Target:** Directly North (Zero eastward drift).

### **Step-by-Step Solution**

#### **1. Determining the Heading Angle ($\theta$)**
To cancel the river's eastward push, the boat must aim westward at an angle $\theta$. The eastward component of the boat's velocity must equal the river's speed.
$$\sin(\theta) = \frac{v_{river}}{v_{boat}} = \frac{2}{5} = 0.4$$
$$\theta = \arcsin(0.4) \approx \mathbf{23.58^\circ \text{ (West of North)}}$$

#### **2. Calculating Net Velocity ($v_{net}$)**
Using the Pythagorean theorem, we find the resultant velocity that actually moves the boat across the river:
$$v_{net} = \sqrt{v_{boat}^2 - v_{river}^2}$$
$$v_{net} = \sqrt{5^2 - 2^2} = \sqrt{21}$$
$$v_{net} \approx \mathbf{4.58 \text{ m/s}}$$

#### **3. Calculating Time of Flight ($t$)**
The time taken to cross the $200\text{m}$ width is:
$$t = \frac{\text{Distance}}{\text{Velocity}_{north}}$$
$$t = \frac{200}{4.58} \approx \mathbf{43.67 \text{ seconds}}$$

---
**Defense Note:** "I treated the boat's speed as the hypotenuse of a right triangle. By aiming into the current at $23.6^\circ$, the boat cancels the drift, leaving a net northward speed of $\sqrt{21} \text{ m/s}$."
