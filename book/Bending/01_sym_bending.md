## Symmetrical Bending 
The first case of bending we will examine is known as Symmetrical Bending (or sometimes just Simple Bending). It is characterized by bending where a moment $M$ acting within a given plane will only cause bending deformation within that plane. The conditions necessary for this to occur are that *a*) the cross-section of the beam contains at least one plane of symmetry (see {numref}`Fig:SymSec`) and *b*) the internal bending moment is aligned with or perpendicular to the cross-sectional plane of symmetry. 

```{figure} ../figures/Symmetric_bending_sections_horz.svg
---
width: 80%
name: Fig:SymSec
---
Examples of symmetric beam cross-sections.
```
In this type of bending, it is customary to align the coordinate system of the beam such that the bending moment is aligned with the $x$-axis and bending occurs within the $yz$-plane. In many engineering applications, it is also common to orient the coordinate system with the $y$-axis pointing downwards such that distributed gravitational loads are positive (upper-left orientation in the figure below). However, it should be noted that this is simply a common convention, and the other three orientations of the coordinate system shown in the same figure are equivalent as they represent alternative views of the same beam and loading.

```{figure} ../figures/Symmetric_bending.svg
---
width: 80%
name: Fig:CoordPerspective
---
Various 2D views of a cantilever beam with positive external loading. Note that all views of the beam shown are equivalent. See {numref}`Fig:SymSec` for cross-sections that would make this a symmetric bending case.
```

::::::{tip}
It is easy to confuse the plane in which a moment acts with the direction of a moment. A moment, like a plane, is defined by the direction of the normal vector to that plane (using the right hand rule). So moment $M_x$ acts within the $yz$-plane.
::::::

In order to analyze what happens to a beam in pure bending, we will first start by understanding the nature of its deformation. Based on this understanding, we will then derive formulas to describe the internal stress state and deformation of a beam under pure bending.  

### Deformation due to Bending
Consider the flexible foam beam with a square cross-section illustrated in {numref}`Fig:SymBendDef`. A rectangular grid has been drawn on the beam to help visualize the deformation that occurs. What do you notice about this deformation?

```{figure} ../figures/Bending_deformation_foam_beam.png
---
width: 80%
name: Fig:SymBendDef
---
Visualization of the deformation of a symmetric beam subjected to pure bending.
```
Referring to horizontal lines along the length of the beam in its undeformed state as fibres, several observations can be made.
- Fibres in the upper half of the beam are in compression (ie: $\overline {A'B'}  < \overline {AB} $).
- Fibres in the lower half of the beam are in tension (ie: $\overline {C'D'}  > \overline {CD} $).
- Transverse planes of the beam do not warp or skew due to the moment loading, but remain straight.
- The deformed transverse planes (ie: $\overline {A'C'} $ and $\overline {B'D'} $) will intersect at the centre of curvature of the deformation.

Taking the above observations into account, we can sketch the deformation of the beam as shown below. Here we have introduced another set of points $P$ and $Q$ which define a fibre along the beam that does not change in length as a result of the deformation. We will call this line the {bdg-primary}`neutral plane` of the beam. Although we do not know precisely where it is located at the moment, we can postulate its existence from the fact that on side of the beam is compressed while the other side of the beam elongates. 

::::::{important}
**Neutral plane vs. neutral axis**. Both these terms are used throughout this chapter, but what is the difference between them? If you consider a 3-dimensional beam in bending, the "fibre" along the beam that does not deform is actually a 2-dimensional plane. Thus, we refer to it as the neutral plane. When looking at a 2-dimensional cross-section of a beam, the only portion of the neutral plane visible is the intersection between the neutral plane and the cross-sectional plane which we refer to as the neutral axis.
::::::

As we can see, the material within the beam is either being elongated or compressed, we can deduce from our understanding of the types of strains (ie: shear vs. normal strain) that bending results in internal normal strains. This normal strain by definition is zero at the neutral plane and will vary linearly with distance y from the neutral plane according to the relationship:

```{math}
---
name: eq:BendCurv
---
\epsilon_z = \frac{y}{R}
```