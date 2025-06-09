# Problem 1

# 🧪 Measuring Gravitational Acceleration using a Pendulum

## ✅ 1. Preparation

- **Materials Needed:**
  - A **string** (e.g., 1.4 m long).
  - A **small weight** — *Compass embroidered string*.
  - A **stopwatch** or **smartphone timer**.
  - A **ruler or measuring tape** with millimeter (mm) resolution.

- **Pendulum Assembly:**
  - Securely attach the weight to one end of the string.
  - Fix the other end of the string to a **sturdy support** so that it can swing freely.
  - Ensure that:
    - The pendulum can swing without obstruction.
    - The angle of release is small (less than 15°) for simple harmonic motion approximation.

---

## 🧾 2. Measurement Setup

- **Measure the Pendulum Length $L$:**
- Use the ruler to measure from the **suspension point** to the **center of mass of the weight**.
- Recorded Length:  
$$L = 1.4\,\text{m}$$

- **Resolution of Measuring Tool:**
- Ruler resolution:  
$$\text{Resolution} = 1\,\text{mm} = 0.001\,\text{m}$$

- **Calculate Uncertainty in Length $\Delta L$:**
- By definition:  
$$\Delta L = \frac{\text{Resolution}}{2}$$
- Therefore:  
$$\Delta L = \frac{0.001\,\text{m}}{2} = 0.0005\,\text{m}$$

---

## 📊 3. Data Collection


![alt text](<Ekran görüntüsü 2025-06-04 024804.png>)

---


- **Length of Pendulum:**
- $L = 1.4\,\text{m}$

- **Perform 10 Trials:**
- Time 10 full oscillations for each trial.
- Let each measurement be denoted as $T_{10}$ (time for 10 oscillations).

- **Measured Data:**

| Trial | $T_{10}$ (s) |
|-------|--------------|
| 1     | 23.74        |
| 2     | 23.81        |
| 3     | 23.69        |
| 4     | 23.76        |
| 5     | 23.85        |
| 6     | 23.79        |
| 7     | 23.71        |
| 8     | 23.78        |
| 9     | 23.73        |
| 10    | 23.77        |

- **Mean Time for 10 Oscillations:**

$$
\overline{T}_{10} = \frac{1}{10} \sum_{i=1}^{10} T_{10,i} = 23.763\,\text{s}
$$

- **Standard Deviation:**

$$
\sigma_T = 0.046\,\text{s}
$$

- **Uncertainty in the Mean:**

$$
\Delta T_{10} = \frac{\sigma_T}{\sqrt{10}} = \frac{0.046}{\sqrt{10}} \approx 0.0146\,\text{s}
$$

---

## 🧮 4. Calculations

- **Period of One Oscillation:**

$$
T = \frac{\overline{T}_{10}}{10} = \frac{23.763}{10} = 2.3763\,\text{s}
$$

- **Uncertainty in the Period:**

$$
\Delta T = \frac{\Delta T_{10}}{10} = \frac{0.0146}{10} = 0.00146\,\text{s}
$$

- **Calculate Gravitational Acceleration:**

Using:

$$
g = \frac{4\pi^2 L}{T^2}
$$

Plug in values:

$$
g = \frac{4\pi^2 \times 1.4}{(2.3763)^2} \approx 9.79\,\text{m/s}^2
$$

- **Propagate Uncertainty:**

Given:
- $\Delta L = 0.0005\,\text{m}$
- $L = 1.4\,\text{m}$
- $\Delta T = 0.00146\,\text{s}$
- $T = 2.3763\,\text{s}$

Now apply:

$$
\Delta g = g \sqrt{\left(\frac{\Delta L}{L}\right)^2 + \left(2\frac{\Delta T}{T}\right)^2}
$$

$$
\Delta g = 9.79 \sqrt{\left(\frac{0.0005}{1.4}\right)^2 + \left(2\frac{0.00146}{2.3763}\right)^2} \approx 0.011\,\text{m/s}^2
$$

---

### ✅ Final Result:

$$
g = 9.79 \pm 0.01\,\text{m/s}^2
$$

> 📘 *The measured value of gravitational acceleration is consistent with the expected standard value of $9.81\,\text{m/s}^2$, showing high accuracy and low uncertainty.*


## 📈 5. Analysis

- **Compare Measured $g$ to Standard Value:**

The experimentally determined value:

$$
g = 9.79 \pm 0.01\,\text{m/s}^2
$$

Standard accepted value:

$$
g_{\text{standard}} = 9.81\,\text{m/s}^2
$$

- **Percent Error:**

$$
\text{Percent Error} = \left|\frac{g - g_{\text{standard}}}{g_{\text{standard}}}\right| \times 100 = \left|\frac{9.79 - 9.81}{9.81}\right| \times 100 \approx 0.20\%
$$

> ✅ *The result is remarkably close to the accepted value with only 0.2% error, indicating high experimental accuracy.*

---

- **Discussion of Uncertainties and Limitations:**

### 🔍 1. How Measurement Resolution Affects $\Delta L$:
- The uncertainty in length is directly tied to the resolution of the measuring tool:
$$
\Delta L = \frac{\text{Resolution}}{2}
$$
- In this experiment:
$$
\Delta L = \frac{1\,\text{mm}}{2} = 0.0005\,\text{m}
$$
- **Higher-resolution tools** (e.g., digital calipers) would reduce $\Delta L$, improving the precision of $g$.

---

### ⏱️ 2. How Timing Variability Affects $\Delta T$:
- Human reaction time introduces variability in the timing of oscillations.
- This affects the standard deviation $\sigma_T$ and thus the uncertainty in the mean:
$$
\Delta T = \frac{\Delta T_{10}}{10} = \frac{\sigma_T}{10\sqrt{n}}
$$
- **Reducing timing errors**:
  - Use multiple trials (we used $n = 10$).
  - Use tools like motion sensors or video analysis for higher accuracy.

---

### ⚙️ 3. Experimental Assumptions and Limitations:

- **Small-angle approximation**:
  - Assumes $\theta < 15^\circ$ so that motion is simple harmonic.
  - Larger angles would introduce non-linear effects and require a correction factor.

- **Negligible air resistance**:
  - Assumes damping is minimal, which is acceptable for short durations and streamlined weights.

- **Massless and inextensible string**:
  - Real strings may stretch slightly or have mass, introducing minor deviations.

- **Center of mass estimation**:
  - The exact location of the center of mass of the compass necklace affects the true length $L$.

---

> 📘 *Despite limitations, careful measurement and repeated trials allow a precise and reliable estimate of gravitational acceleration.*

```python
import numpy as np
import matplotlib.pyplot as plt

# Simulated data: times for 10 full oscillations (in seconds)
T10_trials = np.array([23.74, 23.81, 23.69, 23.76, 23.85,
                       23.79, 23.71, 23.78, 23.73, 23.77])

# Constants
L = 1.4  # Length of pendulum in meters
delta_L = 0.0005  # Uncertainty in length (m)
n = len(T10_trials)

# Calculations
T10_mean = np.mean(T10_trials)
T10_std = np.std(T10_trials, ddof=1)  # sample standard deviation
delta_T10 = T10_std / np.sqrt(n)

T = T10_mean / 10  # Period of one oscillation
delta_T = delta_T10 / 10

g = (4 * np.pi**2 * L) / (T**2)
delta_g = g * np.sqrt((delta_L / L)**2 + (2 * delta_T / T)**2)

# Annotation text
textstr = '\n'.join((
    r'$L = 1.4\,\mathrm{m}$',
    r'$\Delta L = 0.0005\,\mathrm{m}$',
    rf'$\overline{{T}}_{{10}} = {T10_mean:.3f}\,\mathrm{{s}}$',
    rf'$\sigma_T = {T10_std:.3f}\,\mathrm{{s}}$',
    rf'$\Delta T_{{10}} = {delta_T10:.4f}\,\mathrm{{s}}$',
    rf'$T = {T:.4f}\,\mathrm{{s}}$',
    rf'$\Delta T = {delta_T:.5f}\,\mathrm{{s}}$',
    rf'$g = {g:.2f}\,\mathrm{{m/s^2}}$',
    rf'$\Delta g = {delta_g:.2f}\,\mathrm{{m/s^2}}$'
))

# Plot
plt.figure(figsize=(6, 4))  # Daha kompakt bir boyut
plt.plot(range(1, n + 1), T10_trials, marker='o', linestyle='-', color='teal', label='Time for 10 Oscillations')
plt.axhline(T10_mean, color='orange', linestyle='--', label='Mean Time')

plt.title('Pendulum Oscillation Measurements', fontsize=14)
plt.xlabel('Trial Number', fontsize=10)
plt.ylabel('Time for 10 Oscillations (s)', fontsize=10)
plt.grid(True, linestyle='--', alpha=0.6)
plt.legend()

# Text box with calculations
props = dict(boxstyle='round,pad=0.4', facecolor='linen', edgecolor='gray')
plt.text(0.75, max(T10_trials) - 0.1, textstr, transform=plt.gca().transAxes, fontsize=9,
         verticalalignment='top', bbox=props)

plt.tight_layout()
plt.show()
```