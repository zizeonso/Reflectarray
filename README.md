# IMPORTANT
**Main contributor: SUZIJIN ABRAR HOSSAIN**

---

# Reflectarray Phase Modelling Project

## Overview

This repository contains a Python-based theoretical and numerical model for a **planar reflectarray antenna**, developed as part of the **PHAS0052 group project**.  
The main objective of this work is to implement the **phase compensation theory of reflectarray antennas** and generate a two-dimensional **aperture phase distribution**, which serves as a quantitative foundation for subsequent **unit-cell design and full-wave simulations** (e.g. HFSS).

Unlike traditional parabolic reflectors, reflectarray antennas achieve beam collimation and steering by introducing spatially varying phase shifts across a flat surface composed of sub-wavelength elements. This project focuses on modelling those phase requirements directly from electromagnetic theory.

---

## Physical Background

For a reflectarray illuminated by a feed antenna, each element must compensate for:

1. **Spatial Phase Delay (SPD)** caused by spherical wave propagation from the feed  
2. **Progressive Phase (PP)** required to collimate or steer the reflected beam  

The total phase required at each reflectarray element is given by

\[
\psi_i = k \left( R_i - \sin\theta \left( x_i \cos\phi + y_i \sin\phi \right) \right) + \psi_0
\]

where:
- $k = 2\pi / \lambda$ is the wavenumber  
- $R_i$ is the distance from the feed to the $i$-th element  
- $(x_i, y_i)$ are the element coordinates on the aperture  
- $(\theta, \phi)$ defines the desired beam direction  
- $\psi_0$ is an arbitrary reference phase  

This formulation follows standard reflectarray antenna theory as described in the literature.

---

## What This Notebook Does

The Jupyter notebook implements the reflectarray phase model numerically and performs the following steps:

- Defines the operating frequency and electromagnetic parameters  
- Constructs a **2D reflectarray aperture grid**  
- Computes the **spatial phase delay** for each element based on feed geometry  
- Adds the **progressive phase term** for beam collimation  
- Applies phase wrapping to obtain physically meaningful phase values  
- Visualises the resulting **2D phase distribution (phase map)**  

The resulting phase map can be directly used as input for **unit-cell geometry tuning**, such as mapping reflection phase to square patch dimensions in full-wave simulations.

---

## Key Features

- Physics-based modelling derived directly from electromagnetic theory  
- Flexible geometry: feed position, array size, and beam direction are easily adjustable  
- Produces clear 2D phase maps suitable for reflectarray antenna design  
- Bridges analytical theory with **HFSS unit-cell simulations**  

---

## Project Context

This work represents the **theoretical modelling and numerical design component** of a larger reflectarray antenna project.  
It provides the essential phase distribution required for:

- Unit-cell design using variable-sized square patch elements  
- Full-wave electromagnetic simulations  
- Fabrication and experimental testing  

The emphasis is placed on clarity, reproducibility, and direct applicability to practical antenna engineering workflows.

---

## Technologies Used

- Python  
- NumPy  
- Matplotlib  
- Jupyter Notebook  

---

## Author Contribution

- Independent implementation of reflectarray phase compensation theory  
- Numerical modelling of aperture-level phase distributions  
- Generation and validation of 2D phase maps for antenna design use  

---

