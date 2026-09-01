# COMSOL Multiphysics Model

This section presents the computational implementation of the mathematical model using **COMSOL Multiphysics**. The model was developed to investigate the coupled electrical and electrochemical processes associated with electrochemical treatment of choroidal melanoma.

---

##  Model Overview

A **two-dimensional finite-element multiphysics model** was developed to simulate the treatment environment around the tumor.

The model combines:

* Electric potential and current-density distribution
* Ionic transport
* Electrode reactions
* Hydrogen-ion concentration
* pH evolution

The coupled formulation allows the spatial and temporal behavior of the electrochemical environment to be investigated under prescribed treatment conditions.

---

## Computational Geometry

The computational domain represents the relevant ocular environment, including the **tumor region, surrounding tissue/electrolyte regions, and electrodes**.

The choroidal melanoma is represented as a localized tumor domain in the posterior region of the modeled eye. The electrode configuration is incorporated into the geometry to represent the applied electrochemical treatment.

geometry1.tif

**Figure 1.** Two-dimensional computational geometry showing the modeled ocular environment, tumor region, and electrode configuration.

---

##  Physics Interfaces

The model uses COMSOL Multiphysics to couple the electrical and species-transport processes.

### Electric Currents (ec)

The **Electric Currents (ec)** interface is used to calculate:

* Electric potential
* Electric field
* Current density

These quantities describe the electrical response of the treatment domain.

### Transport of Diluted Species (tds)

The **Transport of Diluted Species (tds)** interface is used to model ionic species transport through:

* Diffusion
* Electromigration
* Species generation and consumption

The resulting concentration fields are used to evaluate the treatment-induced chemical environment.

---

##  Multiphysics Coupling

The electrical and species-transport processes are coupled through the electric field and ionic migration.

```text
Applied Electrical Conditions
          ↓
Electric Potential & Field
          ↓
Ionic Migration
          ↓
Species Transport & Reactions
          ↓
H⁺ Concentration
          ↓
pH Distribution
```

This coupling provides a unified computational framework for analyzing the interaction between electrical forcing, electrochemical reactions, and ionic transport.

---

## 5. Electrode Configuration

Electrodes provide the electrical input required to initiate the electrochemical treatment process.

Their **position, geometry, and applied electrical conditions** influence the resulting electric potential, current-density distribution, and local electrochemical environment.

Electrochemical boundary conditions were applied at the electrode–electrolyte interfaces according to the prescribed treatment configuration.

---

## 6. Initial and Boundary Conditions

The model was initialized with prescribed species concentrations representing the initial electrochemical state of the computational domain.

Boundary conditions were applied to the electrodes and relevant domain boundaries to define the electrical and species-transport behavior.

Depending on the model formulation, these conditions include:

* Applied potential or current
* Electrode reaction conditions
* Species fluxes
* No-flux boundaries
* Initial species concentrations

These conditions define the physical constraints required for the numerical simulation.

---

## 7. Mesh

The computational domain was discretized using an **unstructured triangular mesh**.

Local refinement was applied near the **tumor and electrode regions**, where stronger spatial variations in electric potential, current density, and species concentration are expected.

![Computational Mesh](../Figures/Mesh.png)

**Figure 2.** Unstructured triangular mesh used for the finite-element discretization of the computational domain.

---

## 8. Study and Solver

A **time-dependent study** was performed to investigate the evolution of the electrochemical environment during treatment.

| Parameter          | Setting               |
| ------------------ | --------------------- |
| Study type         | Time-dependent        |
| Initial time       | 0 s                   |
| Final time         | 1200 s                |
| Treatment duration | 1200 s                |
| Time stepping      | Automatic             |
| Numerical method   | Finite Element Method |

The simulation calculates the coupled electrochemical variables at successive time points, allowing the temporal evolution of ionic concentrations and pH to be analyzed.

---

## 9. Model Outputs

The principal simulation outputs include:

| Quantity               | Purpose                                            |
| ---------------------- | -------------------------------------------------- |
| **Electric Potential** | Analyze the electrical potential distribution      |
| **Current Density**    | Examine the spatial distribution of current        |
| **Ion Concentration**  | Investigate ionic transport                        |
| **H⁺ Concentration**   | Evaluate treatment-induced hydrogen-ion changes    |
| **pH Distribution**    | Characterize the local acidic/alkaline environment |
| **Temporal Evolution** | Examine changes during treatment                   |

These outputs form the basis for the **Simulation Results and Analysis** presented in the next section of the repository.

---

## Summary

The COMSOL Multiphysics model provides a **finite-element computational framework** for studying the electrical, electrochemical, and ionic transport processes associated with electrochemical treatment of choroidal melanoma.

The model integrates the **computational geometry, electrode configuration, coupled physics, mesh, and time-dependent simulation** to investigate the resulting electrochemical environment around the tumor.

The next section presents the **simulation results and their analysis**.
