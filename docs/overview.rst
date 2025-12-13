Overview
========

Problem Statement
-----------------

Drosophila melanogaster wings provide a classic model for linking developmental
and genetic pathways to subtle, yet reproducible, changes in morphology.
Perturbations of signalling pathways such as EGFR, Notch and Dpp typically lead
to low-amplitude shifts in vein position, wing proportions and overall geometry
rather than gross malformations.

These pathway-specific shape signatures can be quantified using landmark-based
morphometrics or image-based methods, and form the basis for comparing genotype
effects. In this project, we build on a public bright-field wing image dataset
that provides high-resolution images for multiple mutant genotypes and both
sexes.

Purpose of the Software
-----------------------

The goal of this software is to recognise these phenotypic signatures directly
from raw wing images and predict both **genotype** and **sex**. The tool:

* performs all preprocessing automatically,
* combines deep convolutional image features with handcrafted geometric
  descriptors of wing outline and venation, and
* outputs class probabilities for both tasks.

Through a simple graphical interface, users can upload a cropped wing image and
obtain predicted mutant genotype and sex. This enables scalable and reproducible
phenotyping in settings where subtle differences between mutants are difficult
to score by eye.

Dataset
-------

We use the public high-resolution Drosophila wing imaging dataset (40× Olympus
subset; GigaDB accession ID 100141). Each image contains metadata encoding
genotype, sex and wing side. The high magnification ensures sufficient resolution
to quantify vein topology and intervein geometry, which are essential for
phenotyping signalling-pathway mutants.
