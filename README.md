<div align="center">

# 🤖 MEXE 3202 – Robotics 2  
### Mechanical Manipulator Simulation  
### Laboratory 1 (2026)  
**Group 19**

<br>

![Course](https://img.shields.io/badge/Course-Robotics_2-1f425f?style=flat-square)
![Laboratory](https://img.shields.io/badge/Laboratory-1-2ea44f?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-Robotics_Toolbox-orange?style=flat-square)

</div>

---

## 📘 Project Overview

This repository contains the **Laboratory 1** project for **MEXE 3202 – Robotics 2**, completed by **Group 19** as part of the academic course requirements.

The project focuses on modeling and simulating a mechanical manipulator using both **Python** and **MATLAB**, and validating the results across different software environments.

---

## 📖 Introduction

Robotic manipulators are fundamental components in modern automation systems, widely used in manufacturing, assembly, and precision-based applications. Their ability to perform repetitive tasks with high accuracy and efficiency makes them essential in industrial environments.

In this laboratory activity, our group focuses on implementing and simulating a mechanical manipulator using computational tools. The project emphasizes practical application of robotics concepts through software-based modeling and simulation. By executing the manipulator program in both Python and MATLAB, we analyze system behavior under different input conditions and verify the consistency of results across platforms.

This experiment strengthens our understanding of robotic system implementation, enhances programming proficiency, and develops our ability to present technical work in a structured and professional manner.

---

## 🎯 Objectives

- Formulate the kinematic model of the assigned mechanical manipulator using Denavit–Hartenberg (D–H) parameters and graphical methods  
- Develop and execute forward kinematics simulations in Python and MATLAB  
- Cross-verify simulation outputs across multiple joint variable test cases  
- Present technical findings through structured documentation and oral defense  

---

## # 🧰 Materials
- Laptop
- Python  
- MATLAB  
- Robotics Toolbox by Peter Corke  
- Visual Studio Code  
- GitHub  

---

## 📂 Repository Structure

```
MATLAB_Code/
Python_Code/
Images/
README.md
```

---

## 👥 Group Members

- Bonado, Lance Exequiel M.  
- Fornal, Ian Avenick G.  
- Caparro, Stephen Jay G.  
- Solis, John King Louies R.  

---

<div align="center">


# 📋 Team Member Responsibilities & Instructions

<details>
<summary><strong>1. Project Engineer – Bonado, Lance Exequiel M.</strong></summary>

- **Repository Setup:**  
  Create the group laboratory repository on GitHub. Ensure the repository is **private** and add the lecturer as a collaborator.  

- **Naming Convention:**  
  Title the repository exactly as:
- **Documentation:**  
Write all laboratory instructions and procedures into the repository’s `README.md`.  

- **Kinematics & Formatting:**  
- Draw the kinematic diagram with proper labels.  
- Construct the parametric table.  
- Derive the **Homogeneous Transformation Matrices** of the assigned mechanical manipulator.  
- Upload and embed the images directly in the GitHub README.  

- **Manipulator Link:**  
> **Assigned Manipulator:** [SCARA Manipulator PDF](https://github.com/MikkoDT/Robotics_MEXE_3rdYearCourse/blob/main/MexE_409_Robotics_2/Laboratory_Activities/Laboratory_1_Mechanical_Manipulators.pdf)  

- **Data Integration:**  
Post all simulations and analytical comparisons of Python and MATLAB results.

</details>

<details>
<summary><strong>2. Programmer 1 (Python) – Fornal, Ian Avenick G.</strong></summary>

- **Scripting:** Program the assigned mechanical manipulator in **Python** using the codes taught in class.  
- **Parameters:** Assign only **one set of link lengths**.  
- **Testing:** Test **5 points**, i.e., 5 different sets of joint variable values.  
- **Submission:** Upload the program to a folder in the repository created by the Project Engineer.  

</details>

<details>
<summary><strong>3. Programmer 2 (MATLAB) – Caparro, Stephen Jay G.</strong></summary>

- **Scripting:** Program the assigned mechanical manipulator in **MATLAB** using **Robotics Toolbox by Peter Corke**.  
- **Parameters:** Assign only **one set of link lengths**.  
- **Testing:** Test **5 points**, i.e., 5 different sets of joint variable values.  
- **Submission:** Upload the program to a folder in the repository created by the Project Engineer.  

</details>

<details>
<summary><strong>4. Project Leader – Solis, John King Louies R.</strong></summary>

- **Presentation Prep:** Prepare a **10-minute presentation** (strictly 10 minutes).  

- **Presentation Content:** Present the following:  
1. Kinematic diagram with labels, parametric table, and **Homogeneous Transformation Matrices**.  
2. Simulation results and comparison between Python and MATLAB.  
3. Verification of simulation correctness (based on instructor guidelines).  
4. Conclusion.  

- **Defense Coordination:** Prepare the other 3 members for a **5-minute Q&A** session.  

</details>

---

# 📝 Standard Denavit-Hartenberg (D-H) Transformation Matrix Reference
Students should use the standard D-H transformation matrix for calculations:  

```text
[ cos(θn)  -sin(θn)cos(αn)   sin(θn)sin(αn)  rn*cos(θn) ]
[ sin(θn)   cos(θn)cos(αn)  -cos(θn)sin(αn)  rn*sin(θn) ]
[   0         sin(αn)          cos(αn)          dn      ]
[   0            0                0              1      ]






