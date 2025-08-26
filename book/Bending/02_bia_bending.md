## Biaxial Bending 
In deriving the Flexure Formula for Symmetric Bending, a number of major assumptions about the beam geometry and loading were made. These assumptions greatly simplified the derivation of the formula; however, they also limit the general applicability of the resulting formula. We will systematically relax some of these assumptions in order to obtain more generalized formulas for bending of beams.

We will start by relaxing the constraint on the orientation of the internal bending moment. Previously, we considered only a bending moment that acted orthogonal to an axis of symmetry of the cross section. In this way, bending deformation was confined to the plane defined by this axis of symmetry and the axis of the beam itself (the $z$-axis). We will now consider the case of the internal moment being oriented by an angle $\theta$ with respect to the axis of symmetry as illustrated in {numref}`Fig:Morient`.
```{figure} ../figures/Biaxial_Bending.svg
---
width: 80%
name: Fig:Morient
---
Orientation of a moment, $M$, in the $xy$-plane.
```
Take a moment and think about how you would expect the beam to deform under this new internal loading. 
- Where would you expect the neutral axis to be located? 
- Where do you expect the maximum bending stresses to occur? 

Write down your thoughts so that you can critically reflect on them and align your intuition with the resulting theory. Please do not skip this step as it is vital for developing your own engineer intuition.

### Analyzing Biaxial Bending Using Superposition
This loading state of an arbitrary internal bending moment acting within a symmetric beam cross section is typically referred to as *biaxial bending* as it can be viewed as superposition of two symmetric bending problems.  
```{figure} ../figures/Biaxial_Bending_decomp.svg
---
width: 90%
name: Fig:BiaxBendSup
---
Decomposition of an arbitrary bending moment into a biaxial moment state.
```
Here the moment, $M$, is decomposed into components $M\cos\theta$ and $M\sin\theta$ that can be treated with the symmetric bending equation. Applying the symmetric bending equation for each moment component, we obtain:
```{math}
---
name: eq:BiaxialBend
---
{\sigma _z} = \frac{{{M_x}y}}{{{I_{xx}}}} + \frac{{{M_y}x}}{{{I_{yy}}}}
```
where $M_x$ and $M_y$ are the $x$- and $y$-components of an arbitrary moment $M$, $x$ and $y$ are the distances from the $y$ and $x$ axes respectively, and $I_{xx}$ and $I_{yy}$ are the moments of inertia about the $x$ and $y$ axes respectively. For the above illustrated case, $ {M_x} = M\cos \theta $ as this component produces a positive normal stress in the positive $y$-direction and ${M_y} =  - M\sin \theta $ as this component produces a negative normal stress in the positive $x$-direction.

When analyzing a biaxial bending problem, one must take care when identifying the location of the neutral axis. It may be tempting to think that it will be aligned with moment $M$ as it is with the symmetric bending components, but this is generally not the case. Recognizing that the normal stress at the neutral axis is zero, we can prove this by setting eqn. {eq}`eq:BiaxialBend` equal to zero:
$${\sigma _z} = \frac{{{M_x}y}}{{{I_{xx}}}} + \frac{{{M_y}x}}{{{I_{yy}}}} = 0$$

and then rearranging it define the linear relationship between the $x$ and the $y$ coordinate of the neutral axis:
```{math}
---
name: eq:BiaBendNA
---
\frac{y}{x} =  - \frac{{{M_y}{I_{xx}}}}{{{M_x}{I_{yy}}}} = \tan\alpha 
```