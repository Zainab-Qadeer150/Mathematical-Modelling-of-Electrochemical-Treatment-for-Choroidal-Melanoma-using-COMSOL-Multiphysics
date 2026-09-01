# Mathematical Modelling of Electrochemical Treatment for Choroidal Melanoma

### A Finite-Element Multiphysics Study Using COMSOL Multiphysics

> **Bachelor's Research Project | Mathematical Modelling | Computational Mathematics | Electrochemical Treatment**

---

## Project Overview

This project develops a **two-dimensional mathematical and computational model of electrochemical treatment (EChT) for choroidal melanoma** using **COMSOL Multiphysics**.

The model couples **electric-current distribution, electrochemical reactions, ionic transport, and pH evolution** within a computational representation of the tumor environment. The **Finite Element Method (FEM)** with an unstructured triangular mesh is used to obtain numerical solutions of the governing equations.

The study provides a computational framework for investigating how treatment conditions influence the resulting electrochemical environment, with particular emphasis on **pH variation and ionic transport around the tumor region**.

---

### Clinical Problem

### Choroidal Melanoma

Choroidal melanoma is a malignant tumor arising from melanocytes within the **choroid**, the vascular layer located at the back of the eye.

Effective treatment requires tumor control while minimizing damage to surrounding ocular structures. Established approaches include **plaque brachytherapy, proton beam therapy, laser-based treatments, and surgery**, with treatment-related challenges depending on tumor characteristics and clinical conditions.

This project investigates **electrochemical treatment as a computationally studied minimally invasive approach**, focusing on the underlying electrochemical and transport processes.

---

## Electrochemical Treatment (EChT)

Electrochemical treatment applies a **low direct electric current through electrodes** positioned around or within the treatment region. The resulting electrochemical reactions alter the local chemical environment and produce changes in **ionic concentrations and pH**.

These treatment-induced electrochemical changes provide the physical basis for investigating localized effects within the tumor region while studying the surrounding electrochemical environment computationally.

### Computationally Relevant Process

```text
Applied Electric Current
          ↓
Electrochemical Reactions
          ↓
Ion Generation & Transport
          ↓
Changes in H⁺ Concentration
          ↓
Spatial & Temporal pH Variation
          ↓
Electrochemical Treatment Environment
```

---

## Research Motivation

The motivation of this work is to establish a **mathematical and computational framework for studying the electrochemical processes associated with EChT of choroidal melanoma**.

Rather than replacing established clinical treatments, this study aims to provide **quantitative insight into the relationship between applied treatment conditions and the resulting electrochemical response**.

The main contribution is the development of an **eye-specific multiphysics finite-element model** that couples:

* Electric-current flow
* Electrochemical reactions
* Ionic transport
* Hydrogen-ion concentration
* pH evolution

Such modelling can provide a foundation for investigating **treatment parameters, electrochemical response, and computationally informed treatment strategies**.

---

## Research Objectives

The main objectives of this project are to:

1. Develop a mathematical model for electrochemical treatment of choroidal melanoma.
2. Formulate the governing electrochemical transport equations.
3. Model electric potential and current-density distributions.
4. Simulate ionic transport within the computational domain.
5. Model electrode reactions using electrochemical kinetics.
6. Investigate the evolution of hydrogen-ion concentration and pH.
7. Develop a finite-element-based multiphysics model using COMSOL Multiphysics.
8. Analyze the spatial and temporal distribution of treatment-related electrochemical effects.
9. Investigate the resulting electrochemical environment around the tumor region.
---

##  Mathematical Modelling

The electrochemical treatment model is formulated as a coupled mathematical framework describing the interaction between **electric-field distribution, ionic transport, diffusion, electrode reactions, and hydrogen-ion concentration**.

The governing equations are implemented in **COMSOL Multiphysics** using the **Finite Element Method (FEM)** to investigate the spatial and temporal evolution of the electrochemical environment.

### Charge Conservation

Electric charge conservation is expressed as:

$$
\nabla \cdot \mathbf{J} = 0
$$

where $\(\mathbf{J}\)$ is the current-density vector.

This equation governs the conservation of electric charge within the computational domain and determines the resulting current distribution.

---

### Ohm's Law

The relationship between current density and electric field is given by:

$$
\mathbf{J} = \sigma \mathbf{E}
$$

where:

* $\(\mathbf{J}\)$ = current density
* $\(\sigma\)$ = electrical conductivity
* $\(\mathbf{E}\)$ = electric field

The electric field is related to the electric potential by:

$$
\mathbf{E} = -\nabla \phi
$$

where $\(\phi\)$ represents the electric potential.

---

### Nernst–Planck Equation

Transport of ionic species is described by the Nernst–Planck formulation, which accounts for **diffusion and electric-field-driven migration**:

$$
\frac{\partial c_i}{\partial t}+\nabla\cdot\mathbf{N}_i=R_i
$$

where $\(c_i\)$ is the concentration of species $\(i\)$, $\(\mathbf{N}_i\)$ is its flux, and $\(R_i\)$ represents the corresponding reaction or source term.

The ionic flux can be expressed as:

$$
\mathbf{N}_i
=
-D_i\nabla c_i
-z_i u_i F c_i\nabla\phi
+c_i\mathbf{v}
$$
where $\(D_i\)$ is the diffusion coefficient, $\(z_i\)$ is the ionic charge number, $\(u_i\)$ is ionic mobility, $\(F\)$ is the Faraday constant, $\(\phi\)$ is electric potential, and $\(\mathbf{v}\)$ is fluid velocity where applicable.

---

###  Fick's Law of Diffusion

The diffusive component of species transport is described by Fick's law:

$$
\mathbf{N}_{i,\mathrm{diff}}=-D_i\nabla c_i
$$

The negative sign indicates that diffusion occurs from regions of higher concentration toward regions of lower concentration.

Diffusion contributes to the redistribution of electrochemically generated species and influences the resulting concentration and pH gradients.

---

### Butler–Volmer Electrode Kinetics

Electrochemical reactions at the electrode–electrolyte interfaces are described using Butler–Volmer kinetics:

$$
i
=
i_0
\left[
\exp\left(\frac{\alpha_a F\eta}{RT}\right)-
\exp\left(-\frac{\alpha_c F\eta}{RT}\right)
\right]
$$

where:

* $\(i\)$ = electrode current density
* $\(i_0\)$ = exchange current density
* $\(\eta\)$ = overpotential
* $\(\alpha_a,\alpha_c\)$= anodic and cathodic charge-transfer coefficients
* $\(F\)$ = Faraday constant
* $\(R\)$ = universal gas constant
* $\(T\)$ = absolute temperature

This formulation describes the rate of electrochemical reactions occurring at the electrode interfaces.

---

### Faraday's Law

Faraday's law relates the electrical charge transferred to the amount of chemical species produced or consumed:

$$
n=\frac{It}{zF}
$$

where:

* $\(n\)$ = amount of substance
* $\(I\)$ = electric current
* $\(t\)$ = treatment time
* $\(z\)$ = number of electrons transferred
* $\(F\)$ = Faraday constant

This provides a quantitative connection between the applied electrical treatment and electrochemical species generation.

---

###  pH Calculation

The local pH is calculated from the hydrogen-ion concentration:

$$
\mathrm{pH}=-\log_{10}[H^+]
$$

where $\([H^+]\)$ represents the hydrogen-ion concentration.

The resulting pH distribution provides a quantitative measure of the treatment-induced acidic or alkaline environment.

---


