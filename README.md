# pyflash
Flash Separation Calculations with Python

|              Method              |                                                       Description                                                       |            Application             |  
|:--------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|:----------------------------------:|  
| Raoult's Law                     | Assumes ideal behaviour; partial pressure of each component is proportional to its mole fraction in the liquid phase.   | Ideal mixtures                     |  
| Dalton's Law                     | Total pressure is the sum of partial pressures of all components in the vapor phase.                                    | Ideal mixtures                     |  
| Henry's Law                      | Used for components at low concentrations; relates partial pressure to mole fraction in the liquid phase.               | Dilute solutions                   |  
| Activity Coefficients            | Accounts for non-ideal behaviour by introducing activity coefficients to modify Raoult's Law.                           | Non-ideal mixtures                 |  
| Fugacity Coefficients            | Corrects for non-ideal gas behaviour; used in conjunction with equations of state.                                      | Non-ideal mixtures                 |  
| Equations of State (EOS)         | Mathematical models (e.g., Van der Waals, Redlich-Kwong, Peng-Robinson) that describe the PVT behaviour of fluids.      | Both ideal and non-ideal mixtures  |  
| Excess Gibbs Free Energy Models  | Models like Wilson, NRTL, and UNIQUAC that describe non-ideal liquid mixtures by calculating excess Gibbs free energy.  | Non-ideal mixtures                 |  
| Group Contribution Methods       | Methods like UNIFAC that estimate activity coefficients based on group contributions.                                   | Non-ideal mixtures                 |  
| Vapor-Liquid                     | Equilibrium (VLE) Data Correlation	 Empirical correlations based on experimental VLE data to predict phase behaviour.   | Both ideal and non-ideal mixtures  |  
| Thermodynamic Consistency Tests  | Methods to check the consistency of experimental VLE data with thermodynamic principles.                                | Both ideal and non-ideal mixtures  |  
