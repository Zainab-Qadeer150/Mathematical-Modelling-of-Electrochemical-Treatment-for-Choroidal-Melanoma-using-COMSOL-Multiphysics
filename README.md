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

Choroidal melanoma is a malignant tumor arising from melanocytes within the **choroid**, the vascular layer located at the back of the eye [1].

Effective treatment requires tumor control while minimizing damage to surrounding ocular structures. Established approaches include **plaque brachytherapy, proton beam therapy, laser-based treatments, and surgery**, with treatment-related challenges depending on tumor characteristics and clinical conditions.

This project investigates **electrochemical treatment as a computationally studied minimally invasive approach**, focusing on the underlying electrochemical and transport processes [3].

---

## Electrochemical Treatment (EChT)

Electrochemical treatment applies a **low direct electric current through electrodes** positioned around or within the treatment region[3]. The resulting electrochemical reactions alter the local chemical environment and produce changes in **ionic concentrations and pH**.

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

The motivation of this work is to establish a **mathematical and computational framework for studying the electrochemical processes associated with EChT of choroidal melanoma** [2].

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

The governing equations are implemented in **COMSOL Multiphysics** using the **Finite Element Method (FEM)** to investigate the spatial and temporal evolution of the electrochemical environment [5].

### Charge Conservation

Electric charge conservation is expressed as:

$$
\nabla \cdot \mathbf{J} = 0
$$

where $\mathbf{J}$ is the current-density vector.

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
### Species Conservation

The transport and evolution of each ionic species are governed by the species conservation equation:

```math
\frac{\partial c_i}{\partial t}
+
\nabla \cdot \mathbf{N}_i
=
R_i
```

where:

- $c_i$ = concentration of species $i$
- $\mathbf{N}_i$ = molar flux of species $i$
- $R_i$ = reaction or source term

This equation describes the change in ionic-species concentration due to transport and electrochemical reactions.

---

### Nernst–Planck Equation

The transport of ionic species is described using the Nernst–Planck equation, which accounts for diffusion and electric-field-driven migration [7].

```math
\mathbf{N}_i
=
-D_i\nabla c_i
-z_i u_i F c_i\nabla\phi
```

where:

- $D_i$ = diffusion coefficient
- $z_i$ = ionic charge number
- $u_i$ = ionic mobility
- $F$ = Faraday constant
- $\phi$ = electric potential

The Nernst–Planck formulation describes the transport of charged species under the combined effects of **diffusion and electric-field-driven migration**.

### Fick's Law of Diffusion

The diffusive component of species transport is described by Fick's law:

```math
\mathbf{N}_{i,\mathrm{diff}}
=
-D_i\nabla c_i
```

The negative sign indicates that diffusion occurs from regions of higher concentration toward regions of lower concentration.

In this model, diffusion contributes to the redistribution of electrochemically generated species and influences the spatial development of concentration and pH gradients.

---

### Butler–Volmer Electrode Kinetics

Electrochemical reactions at the electrode–electrolyte interfaces are described using Butler–Volmer electrode kinetics:

```math
i
=
i_0
\left[
\exp\left(\frac{\alpha_a F\eta}{RT}\right)
-
\exp\left(-\frac{\alpha_c F\eta}{RT}\right)
\right]
```

where:

* $i$ = electrode current density
* $i_0$ = exchange current density
* $\eta$ = overpotential
* $\alpha_a$ = anodic charge-transfer coefficient
* $\alpha_c$ = cathodic charge-transfer coefficient
* $F$ = Faraday constant
* $R$ = universal gas constant
* $T$ = absolute temperature

This formulation describes the rate of electrochemical reactions occurring at the electrode–electrolyte interfaces.

---

### Faraday's Law

Faraday's law relates the electrical charge transferred during an electrochemical reaction to the amount of chemical species produced or consumed:

```math
n
=
\frac{It}{zF}
```

where:

* $n$ = amount of substance produced or consumed
* $I$ = electric current
* $t$ = treatment time
* $z$ = number of electrons transferred
* $F$ = Faraday constant

This relationship provides a quantitative connection between the applied electrical treatment and electrochemical species generation.

---

### pH Calculation

The local pH is calculated from the hydrogen-ion concentration:

```math
\mathrm{pH}
=
-\log_{10}[H^+]
```

where $[H^+]$ represents the hydrogen-ion concentration.

Changes in hydrogen-ion concentration lead to local variations in pH during electrochemical treatment [6]. Therefore, the pH distribution provides an important quantitative measure of the treatment-induced acidic or alkaline environment.

---

