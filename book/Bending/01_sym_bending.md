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


```{figure} ../figures/Bending_deformation_drawing3.svg
---
width: 80%
name: Fig:SymBendDefDraw
---
Fibre elongation/contraction in a beam under pure bending.
```

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

where $R$ is the radius of curvature of the neutral plane of the beam.

For completeness, the derivation of this expression is given at the end of this section. More importantly, you should focus on what this expression tells us. Looking at the above equation we see that the normal strain due to bending is linearly dependent on the distance $y$ that we defined as the transverse distance from the neutral plane. Noting that this result was derived for a positive internal bending moment (refer to the direction of $M_x$ in {numref}`Fig:SymBendDefDraw`), we can also see that a compressive normal strain is produced when $y$ is negative (above the neutral plane) and a positive normal strain when $y$ is positive (below the neutral plane). This is consistent with our earlier observations of beam deformation in {numref}`Fig:SymBendDef` and reconnects with the deformation-based sign convention for internal bending moments discussed in **Sign Convention for Internal Loads** section in the chapter on **Internal Loads**. 

Recalling that we are limiting our analysis of beams to the linear elastic material regime, we can also then state that the internal normal stresses within the beam will also vary linearly with distance from the neutral plane. Thus, we can express that:
$${\sigma _z} = E{_z} = E\frac{y}{R}$$ (eq:stresscurvature)

```{math}
---
name: eq:stresscurvature2
---
{\sigma _z} = E{_z} = E\frac{y}{R}
```

where $E$ is the Young's modulus of the beam material.

::::::{admonition} Derivation of the Strain-Curvature Relationship
:class: tudproof, dropdown
Consider a spanwise differential segment of a beam in bending, $dz$, as illustrated in Fig. !fig{SymBendDefDraw} in both its undeformed and deformed states. The neutral plane of the beam is denoted by points $P$ and $Q$ such that:
    $$\overline {PQ}  = \overline {P'Q'}  = dz$$

In the deformed state, we can define this length by the arc length swept by the radius of curvature, $R$, of the neutral plane:
    $$\overline{P^\prime Q^\prime} = dz = R \cdot d\theta$$

which can be rearranged to obtain:
    $$d\theta = \frac{dz}{R}$$

If we now look at another plane $\overline{EF}$ located an arbitrary distance $y$ from the neutral plane, we can define its length in the undeforemed state as:

    $$\overline{EF} = dz$$

and in its deformed state as:
    $$\begin{array}{*{20}{c}}
    {\overline {E'F'}  = \left( {R + y} \right)d\theta }\\
    { = dz + \frac{y}{R}dz}
    \end{array}$$

Recalling that normal strain is defined by the change in length of a segment of material divided by its original length, we can formulate an expression for the normal strain in a beam as a function of distance $y$ from the neutral plane:
    \begin{equation*}
        \begin{split}
            \epsilon_z &= \frac{\Delta L}{L}\\
            &= \frac{\overline{E^\prime F^\prime}-\overline{EF}}{\overline{EF}}\\
            &= \frac{\left( dz + \frac{y}{R}dz \right) - dz}{dz}\\
            &= \frac{y}{R}
        \end{split}
    \end{equation*}

Thus ending up with the result expressed in eqn. {eq}`eq:stresscurvature`.
::::::

### Flexure Formula
In the previous section, we defined a linear relationship between the normal normal strains in a beam and the distance from the neutral plane of a beam; however, this relationship was in terms of the curvature of the beam. It would be more useful to be able to relate the internal stresses and strains in a beam to the moment loading rather than the beam curvature. 

If we consider a beam under pure moment loading, the internal loading will simply be the bending moment, $M_x$, as illustrated in the figure below. We also observed in the previous section that bending will result in a internal normal stress state that varies linearly with the distance from the neutral plane. Realizing that the internal forces in the beam are simply resultants of the internal stress distribution, we can derive the relation between them by equating their resultants.

```{figure} ../figures/FlexureFormulaRef2.svg
---
width: 80%
name: Fig:FlexFormRef
---
Illustration of the internal normal stress distribution that has a resultant of $M_x$.
```

::::::{admonition} Normal Force Equivalency
:class: tudproof
It is logical that a normal stress distribution will have a resultant normal force. In the case of pure bending, the internal normal force is zero, so we need to ensure that resultant normal force:
    \begin{equation*}
    N_z = \int_A \sigma_z dA = 0
    \end{equation*}
    
where $dA$ is a differential area element of the cross-section and $A$ is the total area domain of the cross-section. In this case, we can observed that the normal stress varies only with the $y$-coordinate in eqn. {eq}`eq:stresscurvature`. Thus we can conveniently define our differential area element $dA$ as slices of the cross-section with a constant $y$-coordinate (areas of constant stress) as illustrated in {numref}`Fig:FlexFormRef`. Substituting the normal stress distribution from eqn. {eq}`eq:stresscurvature`, we obtain:
    \begin{equation*}
    N_z = \int_A E\frac{y}{R} dA = 0
    \end{equation*}
    
If we limit ourselves to a beam made out of a single material (constant $E$), then we can further simplify this to:
    \begin{equation*}
    N_z = \frac{E}{R} \int_A y dA = 0
    \end{equation*}
   
Looking at this expression, we can see that there is only one non-trivial solution as if $R = 0$ there is no bending, and if $E=0$, there is no bending. Thus, in order for the condition of normal force equivalency to be met, then:
    \begin{equation*}
    \int_A y dA = 0
    \end{equation*}
    
Hopefully this expression looks a little familiar to you. This integral is often referred to as the *First Moment of Area*, and denoted by the letter $Q$. We have used the First Moment of Area in the past to calculate the location of a centroid. 
    
What does this condition actually mean? If you recall that we specified that $y$ was the distance from the neutral plane, but that we actually did not know at this moment precisely where it was located. This condition actually specifies its location. In order for First Moment of Area based on this definition of $y$ to be equal to zero, **the neutral plane must pass through the centroid of the cross-section**.  
::::::