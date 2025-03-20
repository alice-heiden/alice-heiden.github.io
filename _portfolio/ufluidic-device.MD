---
title: "Microfluidic Device: Pinch Flow Fractionation (PFF)"
excerpt: "A self-designed ufluidic device that is designed to separate molecules of 125-150 um and 425-500um in solution."
header:
  image: /assets/img/ufluidic-cad.png
  teaser: /assets/img/syringe-pump.png 
gallery:
  - image_path: assets/img/pump-cad.png
  - image_path: assets/img/pump-wiring.png
  - image_path: assets/img/syringe-pump.png
   
---

# Introduction

Microfluidic devices are miniature platforms designed to control and manipulate small volumes of fluids, typically in the microliter or nanoliter range, using channels with dimensions on the order of micrometers. The small scale of these devices allows for precise control over fluid flow, which enables high-throughput screening, rapid analysis, and integration of various assays, all within a compact, cost-effective system. This is extremely useful when it comes to biomedical engineering as they have increased the innovation and efficiency throughout the fields of diagnostics, lab-on-a-chip technology, and drug delivery systems.

One such innovation within this category is pinch flow fractionation (PFF), a technique that has gained attention for its ability to separate particles based on size, shape, and deformability. The working principle of PFF relies on controlling fluid flow through microchannels with precise pinch points that create localized pressure differences. These pressure gradients cause particles in the fluid to move along specific pathways, separating them according to their physical properties. By using the principles of fluid dynamics and precise microchannel design, PFF enhances the ability to sort and manipulate small particles with great accuracy, addressing challenges in particle analysis that were once difficult to overcome with traditional methods.

The combination of these innovations has led to researchers being able to detect and monitor cancer metastasis through blood samples. Previously, the size overlap between white blood cells and circulating tumor cells (CTCs) caused issues when attempting to separate them out, but PFF allows researchers to take advantage of the deformed nature of these cells to separate and sort them while maintaining viability for testing and enrichment. [3]  


# Instructions

### CAD Model

The CAD model for my device was created in Fusion360 (Autodesk). The device was designed to be 25 x 75 mm to fit into a standard micropscope slide. There was also a 3 mm clearance on all sides to allow for the device to bond to the slide and minimize leaking. 2 inlet and 3 outlet barbs were modeled in the CAD model as well. The CAD design created a negative model of which material would be poured in to cast the actual device.

### Print & Cure Mold

The model was printed on a Form 3 SLA printer using black resin (Formlabs). The CAD design was exported into an STL file, which was then sliced and converted into g-code using PreForm software (Formlabs). The Form 3 printer offers a minimum layer resolution of 25 μm along the z-axis and 80 μm along the x- and y-axes, ensuring high precision in the printing process. [2] The print was washed for 5 minutes in the FormWash, then 5 minutes in stationary isopropyl alcohol, IPA (Formlabs). The mold them dried for 30 minutes, at an angle that ensured no IPA would pool in the print, and was then UV cured for 60 seconds at room temperature before removing the supports.

### Parylene Device

The cured prints were transferred to a Labcoter PDS 2010 parylene deposition machine (Specialty Coating Systems), where they were coated with parylene-C following the manufacturer’s guidelines. A total of 2 grams of parylene-C was used to coat all prints, with all other parameters automated by the Labcoter. [3]

### Cast the PDMS

The prints were then placed in a plastic petri dish, and a mixture of polydimethyl siloxane (PDMS, Sylgard 184; Ellsworth Adhesive Company) elastomer and curing agent was prepared at a 10:1 weight ratio and poured onto the prints. This mixture was degassed for 30 minutes in a vacuum chamber and cured in an oven at 80 °C for 3 hours before demolding. [3]

### Plasma Bond Glass Slide

After demolding, the PDMS devices were bonded to glass coverslips using a PlasmaFlo PDC-FMG plasma cleaner (Harrick Plasma) and sterilized in an autoclave before use. [3]

# Discussion

While this model is not directly applicable to medicine due to its large molecule size, it could be useful in drug or polymer sorting in the future. Additionally, this model could be scaled down appropriately to fit the specs required to separate molecules found in blood.

From the two inlet barbs is two paths, 0.75 mm in width. This minimizes the stacking of molecules as it is 1.5 times the diameter of the largest possible molecule that this device was designed to sort. The two paths then meet at the pinched segment, which is 0.60 mm wide (1.2 times the maximum particle width) and 1.25 mm long (slighly larger than 2x the largest particle diameter). [1] 

From the pinched segment, the fluid flows into the wide segment, which is 19 mm wide. Based on the width of the pinched and broad sections, the theroetical position of each particle's flow was calculated. Since the molecules go from a large to small to large cross-sectional area, they are effectively pushed against the wall and then follow their centerline along the wall. The outlet channels were 5.25 mm wide, which was decided based on determining the midpoint between the particle positions. 

All of the outlets were intended to have the same length of about 19 mm, which was determined based on the shortest path from the beginning of the outlet channel to the furthest outlet barb. All other paths were made more torutuous to approximate this length in order to ernsure similar resistances across all channels. All outlet channels tapered to a width of 0.75 mm over the length of 5.00 mm.

* Based on the results of testing, could you implement any future changes to improve sorting?


## Supplemental Images
{% include gallery %}

## References
1. Maenaka, H., Yamada, M., Yasuda, M., & Seki, M. (2008). Continuous and size-dependent sorting of emulsion droplets using hydrodynamics in pinched microchannels. Langmuir, 24(8), 4405-4410.
2. O'Grady, B. J., Geuy, M. D., Kim, H., Balotin, K. M., Allchin, E. R., Florian, D. C., ... & Lippmann, E. S. (2021). Rapid prototyping of cell culture microdevices using parylene-coated 3D prints. Lab on a chip, 21(24), 4814-4822.
3. Pødenphant, M., Ashley, N., Koprowska, K., Mir, K. U., Zalkovskij, M., Bilenberg, B., … & Marie, R. (2015). Separation of cancer cells from white blood cells by pinched flow fractionation. Lab on a Chip, 15(24), 4598-4606. https://doi.org/10.1039/c5lc01014d
