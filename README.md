# pyflash
Flash Separation Calculations with Python

In this work, with some practical examples, we present an approach to using these resources based on the SCORM learning paths as a tool for curation and reinforcement of content sharing. By learning path, we refer to a sequence of modules or activities the learner must complete in a particular order. The content is structured to guide students from basic concepts to more advanced topics or through a customizable learning experience based on their performance. The advantage of this approach is that it not only considers problem-solving methods but also relates them to theoretical concepts, the use of numerical methods and Python libraries, and the presentation of results in graphical form or in the form of summations that also allow interaction with the student to study specific cases. In this case, determining physical properties in equilibrium has been chosen as an example to illustrate the proposed methodology.

## Introduction

Flash separations are fundamental processes in chemical engineering, widely used to separate multicomponent mixtures into vapor and liquid phases. These processes are essential to many industrial chemical processes like petrochemical, pharmaceutical, and food processing. Teaching flash separation calculations involves understanding both theoretical and practical aspects to equip students with the necessary skills for real-world applications \[1, 2\].

The theoretical foundation of flash separation is the phase equilibrium thermodynamics. Key concepts include Raoult's Law, Dalton's Law, and concepts of fugacity and activity coefficient, phase diagrams, and types of flash separations. These principles help predict the components' behavior in a mixture under different temperature and pressure conditions. Understanding these concepts is crucial for accurately calculating phase compositions and quantities. Flash separation relies on the sudden pressure release, causing the liquid mixture to undergo phase separation into vapor and liquid phases. The process reaches equilibrium between the vapor and liquid phases, allowing for the separation of components based on their volatility.

Solving flash separation problems involves the use of numerical methods. Calculating pure components' boiling points, dew, and bubble points and techniques like the Rachford-Rice equation use iterative solving methods like Newton-Raphson to determine the equilibrium compositions. These methods require a solid grasp of mathematical principles and computational skills, making them an integral part of the chemical engineering curriculum. For instance, the Rachford-Rice equation gives the solution for the vapor-liquid equilibrium (VLE) by iterating on the vapor fraction until the material balance is satisfied. Additionally, the Newton-Raphson method is applied to solve non-linear equations that arise in flash calculations, enhancing the accuracy and efficiency of the solutions \[3\].

The ideal tool to fuse these theoretical and numerical aspects into the teaching of flash separation calculations ensures that students develop a comprehensive understanding of the process is the methodology of problem-based learning. This knowledge enhances their problem-solving abilities and prepares them for the challenges they will face in their professional careers. Educators can provide a robust learning experience that bridges the gap between theory and practice by integrating practical examples and computational tools \[4, 5, 6\].

## Phase Equilibrium for Flash Separations

**Flash separation partially vaporizes a liquid mixture by reducing its pressure or increasing its temperature. This process creates two phases: a vapor phase and a liquid phase, each with different compositions. The key to understanding flash separations lies in phase equilibrium, which describes how the mixture's components distribute between the vapor and liquid phases. Here are some essential points about phase equilibrium in flash separations that students need to consult before using the notebooks. Links to these fundamental concepts should appear in a markdown file \[**12**\]. Alternatively, form a part of the markdown cells content of the corresponding Jupyter Notebooks.**

**Gibbs Phase Rule: This rule helps determine the degrees of freedom in a system at equilibrium. For a system with (C) components and (P) phases, the degrees of freedom (F) are given by (F = C - P + 2). This rule is essential for understanding how many variables control a flash separation process \[**13**\].**

**Material and Energy Balances: To perform flash calculations, material balances (accounting for the mass of each component) and energy balances (considering the heat effects) are combined with phase equilibrium relationships. These balances ensure the conservation of total mass and energy during the separation processes \[**14**\].**

**Equilibrium Relations: The equilibrium between the vapor and liquid phases is described by the equality of chemical potentials or fugacity of each component in both phases, expressed in terms of equilibrium constants or activity coefficients, depending on the system \[**15**\].**

**Flash Calculations: These calculations determine the amounts and compositions of the vapor and liquid phases after flash separation. They involve solving a set of nonlinear equations that include the material balances, energy balance, and phase equilibrium relations.**

**Types of Flash Separations: There are different types of flash separations, such as isothermal flash (constant temperature), adiabatic flash (no heat exchange with surroundings), and partial condensation (where only part of the vapor condenses). Based on the above, notebooks should include the methods described in Table I to** **meet the teaching objectives of this learning path \[**16**\].**

**The learning path proposed for this topic in this article is structured according to a traditional scheme in the teaching of thermodynamics in chemical engineering \[**17**\]. The principal theoretical concepts explained about multi-component phase equilibrium are:**

- [**Lever Rule**](https://eng.libretexts.org/Bookshelves/Materials_Science/TLP_Library_II/12%3A_Phase_Diagrams_and_Solidification/12.7%3A_The_Lever_Rule)
- [**Raoult’s Law and VLE**](https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Supplemental_Modules_(Physical_and_Theoretical_Chemistry)/Equilibria/Physical_Equilibria/Raoults_Law_and_Ideal_Mixtures_of_Liquids)
- **Flash Separations**
- **Partial Molar Quantities**
- **Fugacities of Mixtures**
- **Chemical Potential**
- **Vapor-Liquid Equilibrium for Non-Ideal Solutions**

**All these calculations suppose a theoretical background that students should consult before proceeding to jupyter notebook work. Table I includes all methods suggested to students for search before numerical calculations. Figure 1 shows the flow diagram of the proposed learning path. In many cases, the notebooks’ code contains markdown text explaining the principal concepts associated with each item or links to the principal sources of information easily reached from students' laptops and, in the authors’ case, preferably open source and offers-based. Figure 2 shows the interactivity student-teacher diagram of this learning path.**

1. Methods included on the Phase Equilibrium for Flash Calculations Learning Path Notebooks.

| Method | Description | Application |
| --- | --- | --- |
| Raoult's Law | Assumes ideal behavior; partial pressure of each component is proportional to its mole fraction in the liquid phase. | Ideal mixtures |
| Dalton's Law | Total pressure is the sum of partial pressures of all components in the vapor phase. | Ideal mixtures |
| Henry's Law | Used for components at low concentrations; relates partial pressure to mole fraction in the liquid phase. | Dilute solutions |
| Activity Coefficients | Accounts for non-ideal behavior by introducing activity coefficients to modify Raoult's Law. | Non-ideal mixtures |
| Fugacity Coefficients | Corrects for non-ideal gas behavior; used in conjunction with equations of state. | Non-ideal mixtures |
| Equations of State (EOS) | Mathematical models (e.g., Van der Waals, Redlich-Kwong, Peng-Robinson) that describe the PVT behavior of fluids. | Both ideal and non-ideal mixtures |
| Excess Gibbs Free Energy Models | Models like Wilson, NRTL, and UNIQUAC describe non-ideal liquid mixtures by calculating excess Gibbs free energy. | Non-ideal mixtures |
| Group Contribution Methods | Methods like UNIFAC estimate activity coefficients based on group contributions. | Non-ideal mixtures |

| No. | Content |
| --- | --- |
| Ideal Case |     |
| 1   | Gamma (γ) Liquid Activity Coefficients: the activity coefficient (γ) equals 1 for an ideal solution. This means that the behavior of each component in the mixture is like that in the pure state. Therefore, no correction is needed for non-ideal behavior \[18\]. |
| 2   | Phi (φ) Fugacity Coefficient: the fugacity coefficient (φ) equals 1 for an ideal gas. This implies that the gas behaves ideally, and the fugacity (adequate pressure) equals the actual pressure \[19\]. |
| Non-Ideal Case (Activity Coefficient) \[20\] |     |
| 3   | Gamma (γ) Liquid Activity Coefficients: in non-ideal mixtures, especially those with azeotropes, the activity coefficients do not equal 1. Several models can be used to calculate these coefficients \[21\] |
| 4   | Margules Model: This model uses parameters derived from experimental data to account for deviations from ideality \[22\]. |
| 5   | Van Laar Model: This empirical model is used for binary mixtures and can be extended to multicomponent systems \[23\]. |
| 6   | Wilson Model: This model accounts for the non-ideal behavior by considering the energy of interaction between different molecules \[24-25\]. |
| 7   | NRTL (Non-Random Two-Liquid) Model: This model is useful for highly non-ideal mixtures and considers the local composition around each molecule \[26\]. |
| 8   | UNIQUAC (Universal Quasi-Chemical) Model: This model is based on the concept of local compositions and is widely used for complex mixtures \[27\]. |
| Non-Ideal Case (Phi (φ) Fugacity Coefficient from EOS) |     |
| 9   | Peng-Robinson EOS: This cubic equation of state is used to calculate the fugacity coefficient for non-ideal gases \[28, 29\] |
| 10  | Soave-Redlich-Kwong (SRK) EOS: Another cubic EOS commonly used for phase equilibrium calculations \[30\]. |
| 11  | Virial EOS: This equation uses virial coefficients to account for intermolecular forces and is helpful for gases at low to moderate pressures \[31\]. |
| 12  | In mixtures with azeotropes, the gamma/phi method is often used, where activity coefficients represent the liquid phase non-idealities (γ) and the vapor phase non-ideality by fugacity coefficients (φ) \[32\]. |

Figure 1: Flow diagrama of the Learning Path.

All these notebooks are available at a GitHub repository: <https://github.com/anxosanchez/pyflash> for free use. Authors are open to any suggestions or help with the contents or algorithms.

1. The general scheme of each notebook obeys the following sequence:
2. Introduction: an overview of the topics.
3. Learning Objectives: to clarify what students should expect to learn.
4. Theoretical Foundations about Phase Equilibria
5. Numerical Methods related to the flash calculations.
6. Related Python Libraries
7. Applications and Case Studies
8. Additional Resources like textbooks or online Resources
9. Conclusions are a summary of key points covered in the notebook.
10. References
11. Challenges: finally, we propose problems and case studies for the student to continue using the same notebook as homework support.

##### References

1. P. C. Wankat, _Separation process engineering_. Pearson Education, 2006.
2. Henley, Ernest J. and J. D. Seader. “Equilibrium-Stage Separation Operations in Chemical Engineering.” (1981).
3. Mikyška, J. (2023). Robust and efficient methods for solving the Rachford–Rice equation in flash equilibrium calculation. Fluid Phase Equilibria.
4. Eberhart, R.C. (2007). Computational Intelligence: Concepts to Implementations.
5. Sharifzadeh, D.M. (2015). Bridging the Gap : Computer-Aided Engineering for Energy Security and Environmental Protection.
6. Douglas, K.A., & Faltens, T. (2015). A Framework for Integrating Computational Simulations into Engineering Lessons.
7. Perkel, J. (2018). Why Jupyter is data scientists’ computational notebook of choice. Nature, 563, 145-146.
8. Randles, B.M., Pasquetto, I.V., Golshan, M.S., & Borgman, C.L. (2017). Using the Jupyter Notebook as a Tool for Open Science: An Empirical Study. 2017 ACM/IEEE Joint Conference on Digital Libraries (JCDL), 1-2.
9. Chandel, S., Clement, C.B., Serrato, G., & Sundaresan, N. (2022). Training and Evaluating a Jupyter Notebook Data Science Assistant. ArXiv, abs/2201.12901.
10. Lightfoot, R., & Thomas, S.L. (2024). INTEGRATING OPEN EDUCATIONAL RESOURCES IN SOFTWARE ENGINEERING AND COMPUTER SCIENCE SERVICE COURSES: IMPLEMENTATION AND STUDENT FEEDBACK. ICERI Proceedings.
11. Tüysüz, C. (2010). The Effect of the Virtual Laboratory on Students' Achievement and Attitude in Chemistry.
12. Verrett, J., Boukouvala, F., Dowling, A.W., Ulissi, Z.W., & Zavala, V.M. (2020). Computational Notebooks in Chemical Engineering Curricula. Chemical engineering education, 54, 143-150.
13. Ruelle, D. (1967). A variational formulation of equilibrium statistical mechanics and the Gibbs phase rule. Communications in Mathematical Physics, 5, 324-329.
14. Geankoplis, C.J. (2003). Transport processes and separation process principles (includes unit operations).
15. Tsanas, C. (2018). Simultaneous Chemical and Phase Equilibrium Calculations with Non-Stoichiometric Method.
16. Henley, E.J., & Seader, J.D. (1981). Equilibrium-Stage Separation Operations in Chemical Engineering.
17. Minalla, A. (2024). Competency-Based Learning for Improved Teaching and Learning the Thermodynamics Course for Chemical Engineering Students. Asean Journal of Engineering Education.
18. Seader, J.D., & Henley, E.J. (1998). Separation Process Principles.
19. Castier, M., Rasmussen, P., & Fredenslund, A. (1989). Calculation of simultaneous chemical and phase equilibria in nonideal systems. Chemical Engineering Science, 44, 237-248.
20. Fidkowski, Z.T., Malone, M.F., & Doherty, M.F. (1993). Computing azeotropes in multicomponent mixtures. Computers & Chemical Engineering, 17, 1141-1155.
21. Semenov, I., & Shishkin, M. (2024). CALCULATION OF VAPOR-LIQUID EQUILIBRIUM BASED ON THERMODYNAMIC MODELS OF ACTIVITY COEFFICIENTS. Modern Technologies and Scientific and Technological Progress.
22. G. M. Kontogeorgis and G. K. Folas, ‘Thermodynamic Models for Industrial Applications: From Classical and Advanced Mixing Rules to Association Theories’, 2010.
23. Peng, D.Y. (2010). Extending the Van Laar Model to Multicomponent Systems. The Open Thermodynamics Journal, 4, 129-140.
24. Yousefi Seyf, J., Nasrollahi, B., & Jalalinejad, A. (2024). Development of the Wilson Functional Activity Coefficient Model Using High-Quality and Critically Evaluated Phase Equilibria Data. Industrial & Engineering Chemistry Research.
25. Privat, R., Jaubert, J., & Kontogeorgis, G.M. (2023). The secret of the Wilson equation. Fluid Phase Equilibria.
26. Renon, H., & Prausnitz, J.M. (1968). LOCAL COMPOSITIONS IN THERMODYNAMIC EXCESS FUNCTIONS FOR LIQUID MIXTURES. Aiche Journal, 14, 135-144.
27. González, H.E., Abildskov, J., Gani, R., Rousseaux, P., & Bert, B.L. (2007). A method for prediction of UNIFAC group interaction parameters. Aiche Journal, 53, 1620-1632.
28. Nichita, D., & Minescu, F. (2008). Efficient Phase Equilibrium Calculation in a Reduced Flash Context. Canadian Journal of Chemical Engineering, 82, 1225-1238.
29. Nghiem, L.X., Aziz, K., & Li, Y.K. (1983). A Robust Iterative Method for Flash Calculations Using the Soave-Redlich-Kwong or the Peng-Robinson Equation of State. Society of Petroleum Engineers Journal, 23, 521-530.
30. Yakoumis, I., Kontogeorgis, G.M., Voutsas, E.C., Hendriks, E.M., & Tassios, D.P. (1998). Prediction of Phase Equilibria in Binary Aqueous Systems Containing Alkanes, Cycloalkanes, and Alkenes with the Cubic-plus-Association Equation of State. Industrial & Engineering Chemistry Research, 37, 4175-4182.
31. Kamerlingh Onnes H., Expression of state of gases and liquids using series, KNAW Proceedings, 4, 1901-1902, Amsterdam, 125-147 (1902).
32. Malanowski, S.K., & Anderko, A. (1992). Modeling Phase Equilibria: Thermodynamic Background and Practical Tools.
