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