# COMSOL Multiphysics Model

This section presents the computational implementation of the mathematical model using **COMSOL Multiphysics** [4]. The model was developed to investigate the coupled electrical and electrochemical processes associated with electrochemical treatment of choroidal melanoma.

---

## Model Overview

A **two-dimensional finite-element multiphysics model** was developed to simulate the electrochemical treatment environment around the tumor.

The model combines:

* Electric potential and current-density distribution
* Ionic transport
* Electrode reactions
* Hydrogen-ion concentration
* pH evolution

The coupled formulation enables investigation of the **spatial and temporal evolution of the electrochemical environment** under prescribed treatment conditions.

---

## Computational Geometry

The computational domain represents the relevant ocular environment, including the **tumor region, surrounding tissue/electrolyte regions, and electrodes**.

The choroidal melanoma is represented as a localized tumor domain in the posterior region of the modeled eye. The electrode configuration is incorporated into the geometry to represent the applied electrochemical treatment.

https://github.com/Zainab-Qadeer150/Mathematical-Modelling-of-Electrochemical-Treatment-for-Choroidal-Melanoma-using-COMSOL-Multiphysics/blob/main/Figures/Computational%20Geometry.png?utm_source=chatgpt.com

**Figure 1.** Two-dimensional computational geometry showing the modeled ocular environment, tumor region, and electrode configuration.

---

## Physics Interfaces

The model couples electrical and species-transport processes using two principal physics interfaces.

### Electric Currents (ec)

The **Electric Currents (ec)** interface is used to calculate:

* Electric potential
* Electric field
* Current density

These quantities describe the electrical response of the computational domain under the applied treatment conditions.

### Transport of Diluted Species (tds)

The **Transport of Diluted Species (tds)** interface is used to model ionic species transport through:

* Diffusion
* Electromigration
* Species generation and consumption

The resulting concentration fields are used to investigate the treatment-induced changes in the local chemical environment.

---

## Multiphysics Coupling

The electrical and species-transport processes are coupled through the interaction between the electric field and charged species.

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

The applied electrical conditions generate an electric field that influences the migration of charged species. Together with diffusion and electrochemical reactions, this produces spatial and temporal changes in ionic concentrations and consequently in the local pH.

---

## Electrode Configuration

The electrodes provide the electrical input required to initiate the electrochemical treatment process.

Their **position, geometry, and applied electrical conditions** influence the resulting electric potential, current-density distribution, and local electrochemical environment.

Electrochemical boundary conditions were applied at the electrode–electrolyte interfaces to represent the prescribed treatment configuration.

---

## Initial and Boundary Conditions

Initial conditions were specified to represent the electrochemical state of the computational domain before treatment.

The initial concentrations of the modeled ionic species were prescribed, and the corresponding hydrogen-ion concentration was used to define the initial pH.

Boundary conditions were applied to the electrode interfaces and external boundaries to define the electrical and species-transport behavior of the model.

The model includes:

* Prescribed electrical conditions at the electrodes
* Electrochemical reaction conditions at electrode interfaces
* Species flux conditions
* No-flux conditions at appropriate external boundaries
* Initial species concentrations

These conditions provide the physical constraints required for solving the coupled electrochemical model.

---

## Mesh and Discretization

The computational domain was discretized using an **unstructured triangular finite-element mesh**.

Local mesh refinement was applied near the **tumor and electrode regions**, where stronger spatial variations in electric potential, current density, and species concentration are expected.

https://github.com/Zainab-Qadeer150/Mathematical-Modelling-of-Electrochemical-Treatment-for-Choroidal-Melanoma-using-COMSOL-Multiphysics/blob/main/Figures/mesh.png

**Figure 2.** Unstructured triangular finite-element mesh used to discretize the computational domain.

The refined mesh provides improved spatial resolution in regions where significant electrochemical gradients are expected.

---

## Study and Solver

A **time-dependent study** was performed to investigate the evolution of the electrochemical environment during treatment.

| Parameter          | Setting               |
| ------------------ | --------------------- |
| Study type         | Time-dependent        |
| Initial time       | 0 s                   |
| Final time         | 1200 s                |
| Treatment duration | 1200 s                |
| Time stepping      | Automatic             |
| Numerical method   | Finite Element Method |

The numerical solver calculates the coupled electrochemical variables at successive time points, enabling analysis of the temporal evolution of ionic concentrations and pH throughout the treatment period.

---

## Model Outputs

The principal simulation outputs include:

| Quantity               | Purpose                                                          |
| ---------------------- | ---------------------------------------------------------------- |
| **Electric Potential** | Analyze the spatial electrical-potential distribution            |
| **Electric Field**     | Examine the electrical field generated within the domain         |
| **Current Density**    | Investigate the spatial distribution of electrical current       |
| **Ion Concentration**  | Analyze ionic transport within the computational domain          |
| **H⁺ Concentration**   | Evaluate treatment-induced changes in hydrogen-ion concentration |
| **pH Distribution**    | Characterize the resulting acidic and alkaline regions           |
| **Temporal Evolution** | Investigate changes throughout the treatment period              |

These outputs provide the basis for evaluating the **spatial and temporal electrochemical response** generated during the simulated treatment.

---

## Summary

The COMSOL Multiphysics model provides a **finite-element computational framework** for investigating the coupled electrical, electrochemical, and ionic transport processes associated with electrochemical treatment of choroidal melanoma.

The model integrates the **computational geometry, electrode configuration, coupled physics, boundary conditions, finite-element mesh, and time-dependent simulation** to investigate the resulting electrochemical environment around the tumor.

The simulation outputs are subsequently used to analyze the **spatial distribution and temporal evolution of pH and related electrochemical quantities** during treatment.
