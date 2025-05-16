# Problem 1

# 🌊 Interference Patterns on a Water Surface – Wave Modeling

## 🔷 Step 1: Choosing a Regular Polygon

We begin by choosing a **regular polygon** as the geometric base for placing wave sources. In this case, we select a:

- **Square**: A 4-sided regular polygon.

Let the side length be normalized, and the center of the square be located at the origin $(0,0)$. Then, the vertices (wave sources) are placed symmetrically around the origin:

### 🔹 Vertex Coordinates (Wave Sources)

Let the distance from the center to each vertex be $R$. Then the coordinates are:

- $(x_1,y_1) = (R,R)$
- $(x_2,y_2) = (-R,R)$
- $(x_3,y_3) = (-R,-R)$
- $(x_4,y_4) = (R,-R)$

These correspond to the corners of a square centered at the origin.

---

## 📐 Step 2: Define Wave Parameters

We define the physical properties of each wave emitted from the sources:

- **Amplitude**: $A$
- **Wavelength**: $\lambda$
- **Frequency**: $f$
- **Angular Frequency**:  
$$
\omega = 2\pi f
$$
- **Wave Number**:  
$$
k = \frac{2\pi}{\lambda}
$$
- **Initial Phase**: $\phi$  
  (Assume same phase for all sources for coherence)

---

## 🧮 Step 3: Mathematical Model – Single Source

The displacement of the water surface at point $(x,y)$ and time $t$ from a single point source located at $(x_0,y_0)$ is given by:

$$
\eta(x,y,t) = \frac{A}{\sqrt{r}} \cdot \cos\left(kr - \omega t + \phi\right)
$$

where

- $r = \sqrt{(x - x_0)^2 + (y - y_0)^2}$ is the distance from the source to the point $(x,y)$,
- $A$ is the amplitude,
- $k$ is the wave number,
- $\omega$ is the angular frequency,
- $\phi$ is the initial phase.

---

## 📊 Step 4: Superposition from Multiple Sources

Since the waves from all sources are **coherent and identical** (same $A$, $k$, $f$, and $\phi$), the **total surface displacement** at any point $(x,y)$ and time $t$ is:

$$
\eta_{\text{sum}}(x,y,t) = \sum_{i=1}^{N} \eta_i(x,y,t)
$$

For a square, $N=4$, so:

$$
\eta_{\text{sum}}(x,y,t) = \sum_{i=1}^{4} \frac{A}{\sqrt{r_i}} \cdot \cos\left(k r_i - \omega t + \phi\right)
$$

where $r_i = \sqrt{(x - x_i)^2 + (y - y_i)^2}$ for each source $i$.

---

