# Mathematical Modelling of Electrochemical Treatment for Choroidal Melanoma

### A Finite-Element Multiphysics Study Using COMSOL Multiphysics

> **Bachelor's Research Project | Mathematical Modelling | Computational Mathematics | Electrochemical Treatment**

---

## 🔬 Project Overview

This project develops a **two-dimensional mathematical and computational model of electrochemical treatment (EChT) for choroidal melanoma** using **COMSOL Multiphysics**.

The model couples **electric-current distribution, electrochemical reactions, ionic transport, and pH evolution** within a computational representation of the tumor environment. The **Finite Element Method (FEM)** with an unstructured triangular mesh is used to obtain numerical solutions of the governing equations.

The study provides a computational framework for investigating how treatment conditions influence the resulting electrochemical environment, with particular emphasis on **pH variation and ionic transport around the tumor region**.

---

## 🧬 Clinical Problem

### Choroidal Melanoma

Choroidal melanoma is a malignant tumor arising from melanocytes within the **choroid**, the vascular layer located at the back of the eye.

Treatment requires effective tumor control while minimizing damage to surrounding ocular structures. Existing approaches include **plaque brachytherapy, proton beam therapy, laser-based treatments, and surgery**, each presenting different clinical and treatment-related challenges depending on tumor characteristics.

This project investigates **electrochemical treatment as a computationally studied minimally invasive alternative**, focusing on the underlying physical and chemical processes rather than proposing a replacement for established clinical therapies.

---

## ⚡ Electrochemical Treatment (EChT)

Electrochemical treatment applies a **low direct electric current through electrodes positioned around or within the treatment region**. The resulting electrochemical reactions alter the local chemical environment and can generate substantial changes in **ionic concentrations and pH**.

These treatment-induced electrochemical changes provide the physical basis for investigating localized tissue damage and tumor response.

### Computationally relevant processes

```text
Applied Electric Current
          ↓
Electrochemical Reactions
          ↓
Ion Generation & Transport
          ↓
Changes in H⁺ Concentration
          ↓
Spatial and Temporal pH Variation
          ↓
Electrochemical Treatment Environment
```

---

## 🎯 Research Motivation

The motivation of this work is to establish a **mathematical and computational framework for studying the electrochemical processes associated with EChT of choroidal melanoma**.

Rather than replacing established clinical treatments, the model aims to provide **quantitative insight into the relationship between applied treatment conditions and the resulting electrochemical response**.

The main contribution is an **eye-specific multiphysics finite-element model** that couples:

* Electric-current flow
* Electrochemical reactions
* Ionic transport
* Hydrogen-ion concentration
* pH evolution

This framework can support future investigation of **treatment parameters, electrochemical response, and computationally informed treatment strategies**.

---

## 🧮 Mathematical Framework

The model is formulated using coupled partial differential equations and electrochemical transport theory.

### Governing components

| Component                 | Mathematical description      |
| ------------------------- | ----------------------------- |
| Electric potential        | Current continuity equation   |
| Ionic transport           | Nernst–Planck equation        |
| Electrochemical reactions | Electrode reaction kinetics   |
| Numerical solution        | Finite Element Method         |
| pH calculation            | $\mathrm{pH}=-\log_{10}[H^+]$ |

The computational model uses the **Tertiary Current Distribution** interface in COMSOL Multiphysics to investigate the coupled electrical and electrochemical behavior of the treatment domain.

---

## 💻 Computational Methodology

The computational workflow consists of:

```text
Geometry Definition
        ↓
Electrode Configuration
        ↓
Material & Electrochemical Properties
        ↓
Governing Equations
        ↓
Boundary & Initial Conditions
        ↓
Unstructured Triangular Mesh
        ↓
Finite Element Discretization
        ↓
Time-Dependent Simulation
        ↓
Post-Processing & Visualization
```

### Numerical Approach

* **Software:** COMSOL Multiphysics
* **Model:** Two-dimensional computational model
* **Physics:** Tertiary Current Distribution
* **Numerical method:** Finite Element Method (FEM)
* **Mesh:** Unstructured triangular mesh
* **Transport model:** Nernst–Planck formulation
* **Outputs:** Electric potential, current density, ion transport, hydrogen-ion concentration, and pH distribution

---

## 🎯 Research Objectives

The project aims to:

1. Develop a mathematical model for electrochemical treatment of choroidal melanoma.
2. Formulate the governing electrochemical transport equations.
3. Model electric potential and current-density distributions.
4. Simulate ionic transport within the computational domain.
5. Model electrode reactions using electrochemical kinetics.
6. Investigate hydrogen-ion concentration and pH evolution.
7. Develop a finite-element multiphysics model using COMSOL Multiphysics.
8. Analyze the spatial and temporal distribution of treatment-related electrochemical effects.
9. Investigate the resulting electrochemical environment around the tumor region.

---

## 📊 Simulation Outputs

The model is used to investigate the following quantities:

**Electric Potential**
Spatial distribution of electrical potential generated by the applied treatment conditions.

**Current Density**
Distribution of electric current within the computational domain.

**Ion Transport**
Spatial and temporal movement of electrochemically relevant ionic species.

**pH Distribution**
Changes in hydrogen-ion concentration and the resulting local pH environment.

**Temporal Evolution**
Time-dependent evolution of the electrochemical environment during treatment.

---

## 🔭 Research Significance

The developed model provides a computational framework for studying the **multiphysics behavior of electrochemical treatment in an ocular tumor environment**.

By connecting treatment conditions with simulated electrical and chemical responses, the framework can provide quantitative insight for future studies involving:

* Treatment-parameter analysis
* Electrochemical response prediction
* pH evolution
* Tumor-region exposure analysis
* Numerical parameter optimization
* Computationally informed treatment strategies

> **Note:** This is a mathematical and computational study and is not intended to replace clinical treatment or provide direct clinical recommendations.

---

## 🛠️ Tools & Skills

**Software**

`COMSOL Multiphysics`

**Mathematical & Computational Methods**

`Partial Differential Equations` · `Finite Element Method` · `Numerical Simulation` · `Electrochemical Modelling` · `Transport Phenomena`

**Modelled Physics**

`Electric Currents` · `Ion Transport` · `Electrochemical Reactions` · `pH Evolution`

---

## 📁 Repository Structure

```text
📦 Mathematical-Modelling-Electrochemical-Treatment-Choroidal-Melanoma
│
├── 📄 README.md
│
├── 📁 Thesis
│   └── Bachelor_Thesis.pdf
│
├── 📁 Model
│   ├── COMSOL_Model.mph
│   └── Model_Description.md
│
├── 📁 Figures
│   ├── Geometry.png
│   ├── Mesh.png
│   ├── Electrode_Configuration.png
│   ├── Electric_Potential.png
│   ├── Current_Density.png
│   └── pH_Distribution.png
│
├── 📁 Results
│   └── Results_Summary.md
│
└── 📁 Documentation
    ├── Mathematical_Model.md
    └── Methodology.md
```

---

## 📄 Bachelor's Thesis

The complete Bachelor's thesis containing the mathematical formulation, computational methodology, simulations, and detailed analysis is available in:

**[`Thesis/Bachelor_Thesis.pdf`](Thesis/Bachelor_Thesis.pdf)**

---

## 👩‍🔬 Author

**Zainab Qadeer**
BS Mathematics
University of Engineering and Technology, Lahore, Pakistan

**Research Interests:** Mathematical Modelling · Numerical Analysis · Scientific Computing · Finite Element Methods · Computational Mathematics

---

### ⭐ Project Highlights

**Mathematical Modelling** • **Finite Element Method** • **Electrochemical Modelling** • **COMSOL Multiphysics** • **PDEs** • **Numerical Simulation**

