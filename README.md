# MBT-5 Curvature Stabilisation Tests  
### Demonstrating Geometric Shock Suppression Using the Motion–TimeSpace (MTS / MBT-5) Framework

This repository contains a collection of numerical experiments validating a core feature of the MBT-5 geometric framework:  
**curvature-driven stabilisation of nonlinear dynamical fields.**

The code demonstrates how the MBT-5 curvature term (Γ) suppresses shock formation, prevents singularities, and drives unstable systems toward smooth, physically realistic attractors — even when classical PDEs blow up.

---

## 🔍 What This Code Shows

Standard nonlinear advection systems such as the inviscid Burgers equation:

\[
u_t + u\,u_x = 0
\]

are known to form **shocks**, leading to:

- infinite gradients  
- numerical blow-ups  
- oscillations  
- loss of physical meaning  

In contrast, the MBT-5 curvature term introduces a geometric resistance proportional to the local gradient:

\[
\Gamma\text{-term} \;\Rightarrow\; \text{curvature-driven damping}
\]

This produces:

- **shock suppression**  
- **finite gradients**  
- **global field stability**  
- **smooth attractor behaviour**  
- **energy dissipation into a stable plateau**

The stabilisation is **not viscosity**, **not artificial diffusion**, and **not a limiter**.  
It is a geometric damping term unique to the Motion–TimeSpace framework.

---

## 🧪 Experiments Included

The notebook scripts and Python files reproduce several standard instability tests:

### **1. Random-Field Collapse**
Pure random noise is evolved under:
- baseline nonlinear advection (unstable)
- MBT-5 curvature dynamics (stable)

The MBT-5 field collapses noise into a smooth attractor.

### **2. Double Shock Collision**
Two opposing shock fronts collide.

- Baseline solution blows up.
- MBT-5 stabilises the collision and produces a bounded, monotonic profile.

### **3. Step Discontinuity (Shock Formation Test)**
A sharp step (1 → 0 or 0 → 1) evolves forward in time.

- Classical PDE forms a vertical shock.
- MBT-5 smooths the gradient and prevents singularity.

### **4. Energy Stability Test**
We track the total energy:

\[
E(t) = \int u^2\,dx
\]

- Baseline Burgers grows unbounded.
- MBT-5 energy decays into a stable fixed point.

---

## 🌐 Why This Matters

These experiments confirm a central principle of the MBT-5 / MTS theory:

### **Curvature persistence (Γ) acts as a universal geometric stabiliser.**

Where traditional PDEs collapse, blow up, or require artificial fixes,  
the MBT-5 curvature mechanism:

- smooths shocks  
- eliminates singularities  
- regularises nonlinear flows  
- maintains conservation without instability  
- behaves consistently across different initial conditions  

This mirrors the broader claims of MTS in:

- orbital mechanics  
- cosmological curvature  
- field stability  
- information-geometry regularisation  

The exact same stabilising behaviour emerges here in the simplest possible setting.

---

## 📂 What’s in the Repository

```

/mbt5_random_noise_test.py
/mbt5_double_shock_collision.py
/mbt5_step_shock_stability.py
/mbt5_energy_test.py
/common_derivatives.py
/README.md

````

Each script is fully self-contained and can be run directly in any Python environment with NumPy and Matplotlib.

---

## ⚠️ Important Note

These experiments validate the **mathematical stability** of the MBT-5 curvature term.  
They **do not** expose or encode any application of MBT-5 outside PDE/field analysis  
(e.g., they do not reveal financial logic, prediction systems, or applied algorithms).

This repo is strictly a **physics / math demonstration**, not an applied tool.

---

## 🚀 Running the Tests

```bash
python mbt5_random_noise_test.py
python mbt5_double_shock_collision.py
python mbt5_step_shock_stability.py
python mbt5_energy_test.py
````

---

## 🏁 Summary

This repository provides a clean, reproducible validation of the MBT-5 curvature term as a **geometric shock-regularisation mechanism**.
It confirms the theory’s prediction that Γ prevents singularities and stabilises nonlinear fields — a key piece of the broader Motion–TimeSpace framework.

```

---

