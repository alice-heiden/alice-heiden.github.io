---
title: "Multimaterial Pliers"
excerpt: "A self-designed set of 6-inch needlenose pliers printed using PLA (handles) and TPU-95A (flexible center)."
header:
  image: /assets/img/pliers-resistor.gif
  teaser: /assets/img/mm-pliers2.JPG
gallery:
  - image_path: assets/img/mm-pliers.JPG
   
---

# Description: 

### Multimaterial Print-in-Place 

Print-in-place designs are becoming increasingly popular in the prototyping realm as they allow you to create a fully functional prototype in just one go. This includes things like fitting together multiple parts, adding flexibility to a prototype, and all-in-one mechanisms. These applications can be seen in several industries as well as in the normal hobbyist. With things like hinges, snap fits, and joints being able to be printed in this fashion, the limits are seemingly endless. This has been used in instances of robotic fingers, snap-fit joints, spring-loaded boxes, and scissor lifts. This type of printing adds a sense of ease to prototyping as it reduces the stress of tolerances and allows you to get a sense of a parts mechanics fairly quickly.

Successful print-in-place printing depends significantly on the choice of materials. Materials that offer a balance between rigidity and flexibility are ideal for such applications. Thermoplastic elastomers (TPE) and thermoplastic polyurethane (TPU) are commonly used due to their rubber-like flexibility, making them suitable for creating flexible joints and hinges. Conversely, materials like polylactic acid (PLA) and acrylonitrile butadiene styrene (ABS) provide the necessary rigidity for structural components. Combining these materials allows for the fabrication of complex assemblies with both flexible and rigid parts, enhancing the functionality of print-in-place designs.​


### Project & My Design 

This project focused on utilizing multimaterial printing to create a ready-to-use part. We were tasked with creating a set of pliers that could consistently pick up resistors. Due to some lab restrictions, my pliers were designed as separate pieces to be assembled with no tools.

### About the iterative process 

With my project, I began with a base design that replicated needlenose pliers and a square center portion with a grid design intended to allow for shearing. I printed three options of grid density (20%, 25%, and 30%). From this, I determined that the jaws needed more surface area and the 25% density grid provided the best usability. Once this was determined, I was able to add a design to the handles and play around with some other aesthetic features.


### Plier Specs 

* Overall Length: 155 mm
* Jaw Length: 50 mm (Flat Section 7.5mm)
* Jaw Capacity: 11 mm (neutral), X mm (flexed open)
* Handle Length: 71 mm


### Print Settings
 
* **Handles & Jaws**: 
  * Vertical Shells: 3 perimeters, 0 wall thickness
  * Horizontal Shells: 3 top and bottom layers
  * Infill: Rectilinear, 25% Density
* **Flexible Center**: 
  * Vertical Shells: 2 perimeters, 0 wall thickness
  * Horizontal Shells: 0 top and bottom layers
  * Infill: Grid, 25% Density
  * By having no horizontal shell layers, I was able to use the infill pattern to create flexibility. This meant that I could easily adjust the density and shape of the infill without having to tediously edit the CAD model, which allowed for a much faster iterative prototyping process.


# CAD Model:

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4769e6a965613a860?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# Supplemental Images:
{% include gallery %}
