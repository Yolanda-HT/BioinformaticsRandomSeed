**[Back to main page](https://yolanda-ht.github.io/BioinformaticsRandomSeed/)**

# Causal Discovery from Heterogeneous/Nonstationary Data

## Intro
1. Tranditional approached for causal network inference:
  - Constraint-based approaches: recover some information of the underlying causal structure based on conditional independence relationships of the variables (Spirtes et al., 1993)
  - Functional causal models: infer the causal structure by exploiting the fact that under certain conditions, the independence between the noise and the hypothetical cause only holds for the correct causal direction but not for the wrong direction (Shimizu et al., 2006; Hoyer et al., 2009; Zhang and Hyv¨arinen, 2009a,b).

2. Challenge of causal network
  - Distribution shift: may occur across data sets, which may be obtained under different interventions or with different data collection conditions, or over time, as featured by nonstationary data.  It is believed that one of the basic properties of neural connections is their time-dependence (Havlicek et al., 2011).

3. Proposed solution:
Constraint-based causal Discovery from heterogeneous/NOnstationary Data (CD-NOD): assume that mechanisms or parameters, associated with the causal model, may change across data sets or over time (we allow mechanisms to change in such a way that some causal links in the structure may vanish or appear in some domains or over some time periods)
  - Problem 1: identify variables with changing local mechanisms and reliably recover the skeleton of the causal structure over observed variables
  - Problem 2: Take advantage of the information carried by distribution shifts for the purpose of identifying causal directions
  - Problem 3: Extract from data a low-dimensional and potentially interpretable representation of changes, the so-called “driving force” of changing causal mechanisms

4. Solution details
4.1 Phase I: Changing Causal Module Detection and Causal Skeleton Estimation
  4.1.1 Assumptions
  - Confounders, if any, can be written as functions of the domain index or smooth functions of time 2. It follows that in each domain or at each time, the values of these confounders are fixed.
  - The joint distribution ... is Markov and faithful to the augmented graph Gaug. In addition, there is no selection bias; i.e., the observed data are perfect random samples from the populations implied by the causal model.
  4.1.2  Detection of Changing Modules and Recovery of Causal Skeleton

4.2 Phase II: CD-NOD Phase II: Distribution Shifts Benefit Causal Direction Determination
  4.2.1 Causal Direction Identification by Generalization of Invariance
  4.2.2 Causal Direction Identification by Independently Changing Modules

4.3 Phase III: Nonstationary Driving Force Estimation

  
