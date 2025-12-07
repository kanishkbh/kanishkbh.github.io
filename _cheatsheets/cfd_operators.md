---
title: 'CFD: Vector Calculus Operators and Basics'
date: 2025-12-07
permalink: /cheatsheets/cfd-operators/
tags:
  - cfd
  - calculus
  - quick-reference
---

![Divergence visualization](/images/divergence.svg)
*Vector field divergence: spreading of vectors from a point.* Image source: [Khan Academy](https://www.khanacademy.org/math/multivariable-calculus/multivariable-derivatives/divergence-and-curl-articles/a/divergence)

# Divergence

$$\text{div} F$$, or,  $$\nabla . F $$

1D: $$\frac{\partial F}{\partial x}$$

3D: $$\frac{\partial F_1}{\partial x} + \frac{\partial F_2}{\partial y} +  \frac{\partial F_3}{\partial z}$$

F is scalar (e.g. Pressure) → div(F) is not defined. 

**Physical interpretation:**   
The divergence tells us **to what extent the field is spreading the property** out, ”diverging”, i.e., the divergence of velocity is the rate of expansion of the fluid volume per unit volume. An **incompressible** liquid is **divergence free** ($$ \nabla . V = 0 $$). Whenever you here "divergence free flow", it basically means incompressible flow. Beyond the physical interpretation of divergence, this condition is also derived when the continuity equation (conservation of mass) is applied on incompressible flows.   
Whereas, a gas is compressible and the divergence is non-vanishing.

**Application:** Incompressible fluid in a closed system → conservation of mass → divergence of velocity is zero
    
  $$\nabla.\vec{u} = 0$$, or, 
  $$\frac{\partial u}{\partial x} + ... = 0$$
    

# Curl

$$\nabla \times F = \text{curl} F $$


**Physical Interpretation**:   
The curl tells us how the vector field ”swirls” around. Curl is a vector; the magnitude tells us how much it curls, and the direction tells us the axis around which it curls. A vector field F is called **irrotational** if ∇×F = 0.

# Laplacian

Scalar F → Laplacian is scalar 

Vector F → Laplacian is vector or matrix

$$\Delta F = \nabla.(\nabla F) = \text{div(grad} F)$$

scalar $$f$$ + 1D Domain: $$\Delta f = \frac{\partial^2 f}{\partial x^2}$$

scalar $$f$$ + 3D Domain: $$\Delta f = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2}$$

vector $$F$$ + 3D Domain: $$\Delta \mathbf{F} = \begin{pmatrix}
\Delta F_1 \\
\Delta F_2 \\
\Delta F_3
\end{pmatrix} = 
 \begin{pmatrix}
\frac{\partial^2 F_1}{\partial x^2} + \frac{\partial^2 F_1}{\partial y^2} + \frac{\partial^2 F_1}{\partial z^2} \\
\frac{\partial^2 F_2}{\partial x^2} + \frac{\partial^2 F_2}{\partial y^2} + \frac{\partial^2 F_2}{\partial z^2} \\
\frac{\partial^2 F_3}{\partial x^2} + \frac{\partial^2 F_3}{\partial y^2} + \frac{\partial^2 F_3}{\partial z^2}
\end{pmatrix}$$ 

**Application**
  - Fluids (NS equation): viscosity term, a.k.a, diffusion term: $$\nu \Delta \vec{u}$$
  - Heat Diffusion Equation: $$\frac{\partial u}{\partial t} = \alpha \Delta u$$
  - Poisson Equation: $$\Delta u = f$$

## Fun Facts

**Laplacian of a scalar quantity in a vector field:** 

observe that this is the sum of the diagonal elements of the Hessian (i.e. the trace of the Hessian)

$$H(f) = \begin{pmatrix}
\frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial x \partial y} & \frac{\partial^2 f}{\partial x \partial z} \\
\frac{\partial^2 f}{\partial y \partial x} & \frac{\partial^2 f}{\partial y^2} & \frac{\partial^2 f}{\partial y \partial z} \\
\frac{\partial^2 f}{\partial z \partial x} & \frac{\partial^2 f}{\partial z \partial y} & \frac{\partial^2 f}{\partial z^2}
\end{pmatrix}$$

$$\Delta f = \text{tr}(H(f))$$

**Invariance to a *change of basis:***

The invariance of the trace to a change of basis means that the Laplacian can be defined in different coordinate spaces, but it would give the same value at some point (*x*, *y*) in the Cartesian coordinate space, and at the same point (*r*, *θ*) in the polar coordinate space. 

# Lagrangian vs. Eulerian Perspective

### Lagrangian

- “Control Mass”
- Follow a fixed particle over time (particles moves through the volume)
- Moving reference frame $$\vec{X}$$
- Material derivative / Total derivative $$\frac{Du}{Dt}$$

### Eulerian

- “Control Volume”
- Follow a fixed volume over time (particles enter and exit the volume)
- Fixed reference frame $$\vec{x}$$
- Partial derivative $$\frac {\partial u}{\partial t}$$

They are linked by writing the moving reference frame as a function of the fixed reference frame and time, i.e.,

$$\vec{X}(\vec{x}, t)$$

# References

- [https://math.jhu.edu/~lindblad/211/l8.pdf](https://math.jhu.edu/~lindblad/211/l8.pdf)
- [https://machinelearningmastery.com/a-gentle-introduction-to-the-laplacian/](https://machinelearningmastery.com/a-gentle-introduction-to-the-laplacian/)