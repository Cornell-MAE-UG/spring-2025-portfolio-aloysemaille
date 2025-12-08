---
layout: project
title: Torque Wrench Design
description: Mechanics of Engineering Materials Final Project
technologies: [ANSYS, FEM Analysis, MATLAB, CAD, Fusion, Rendering, Stress/Strain Analysis, Strain Gauge, Beam Theory Analysis, Fracture Toughness, Service Life, Fatigue]
image: /assets/images/MM16.png
---

<div>
<p>This is the final project of MAE 3270: Mechanics of Engineering Material.</p>
</div>

<img src="{{ site.baseurl }}/assets/images/MM6.png" style="width:300px; border-radius:10px;" />


<div>
<p>This design is simple but yet needs careful analysis in order to meet the users needs and have a reasonable service life. The baseline design is made of M42 Steel, while the updated torque wrench design uses AerMet 100 high alloy steel, successfully meeting all engineering requirements while maintaining manufacturability and cost effectiveness. </p>
</div>

<img src="{{ site.baseurl }}/assets/images/MM5.png" style="width:300px; border-radius:10px;" />
<img src="{{ site.baseurl }}/assets/images/MM7.png" style="width:300px; border-radius:10px;" />
<img src="{{ site.baseurl }}/assets/images/MM8.png" style="width:300px; border-radius:10px;" />

<div>
<p>Through FEM anlysis on ANSYS, we can check for the total deformation, stresses, strains and mesh deformation under an applied load on the design. Those results can be compared and are found to be relatively similar to hand calculation results. The diffrence found in maximum stress and deformation are due to partial clamping condition in the FEM analysis, which differ from the fully clamped conditions assumed for beam theory and hand calculation analysis.</p>
</div>

<img src="{{ site.baseurl }}/assets/images/MM1.png" style="width:300px; border-radius:15px;" />
<img src="{{ site.baseurl }}/assets/images/MM2.png" style="width:300px; border-radius:10px;" />
<img src="{{ site.baseurl }}/assets/images/MM12.png" style="width:300px; border-radius:15px;" />

<div>
<p>The improved design is made from AerMet 100 high alloy steel. This material has a significantly higher fracture toughness and fatigue strength than M42 Steel, for similar Young's modulus and tensile strength. Those properties allows us to achieve better factor of safety, and allow us to meet the 1 mV/V output minimum requirement. 

The dimension of the design are also thinner than the baseline, but still allow the use of a small full bridge strain gauge.

Through FEM simulation and mesh refinement, the critical high stress and strain areas can be identified and the design adapted to minimize the maximums, while deformation analysis helps predict the behavior of the tool.
</p>
</div>


<img src="{{ site.baseurl }}/assets/images/MM3.png" style="width:300px; border-radius:10px;" />
<img src="{{ site.baseurl }}/assets/images/MM14.png" style="width:300px; border-radius:10px;" />
<img src="{{ site.baseurl }}/assets/images/MM13.png" style="width:300px; border-radius:10px;" />
<img src="{{ site.baseurl }}/assets/images/MM4.png" style="width:300px; border-radius:10px;" />


<div>
<p>To improve user experience and the aesthetics of the design, a grip design can be added to the handle, and the handle is defined as a 4 inches elongation of the arm. 

Its material can be changed to be a high stiffness rubber such as EPDM (Ethylene Propylene Diene Monomer) or Neoprene. This material is meant to provide more grip comfort. The design could have the handle part entirely made out of rubber or have a center of steel alloy like the arm then wrapped with a layer of rubber. 

In addition to those changes, fillets have been added to the edges of the arm and the handle. Those fillets serve both aesthetic and safety purposes, as the rounded shape is not only more pleasing to the eye but also a
great way to prevent injuries or pain from holding the tool.</p> 
</div>

<img src="{{ site.baseurl }}/assets/images/MM15.png" style="width:300px; border-radius:10px;" /> 

<div>
<p>The code above was used for all hand calculations, both for that baseline design and for the improved design.</p> 
</div>

<div>
<p>Work conducted in collaboration with Olivia Santiago, Cornell Mechanical Engineering Student.</p> 
</div>


