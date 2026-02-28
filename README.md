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
## General Laboratory Procedure (Summary)

- **Assign D-H frames**  
  Apply the 4 standard D-H rules sequentially from base to end-effector.

- **Build D-H parametric table**  
  Fill θ, d, a, α for each link based on frame assignments and diagram.

- **Derive transformation matrices**  
  Substitute table values into the standard D-H matrix formula.  
  Create one matrix per link (H0_1, H1_2, …).  
  Capture screenshots of the matrices (or grouped).

- **Compute overall transformation**  
  Chain multiply: H0_n = H0_1 × H1_2 × … × H(n-1)_n  
  Document the multiplication sequence.

- **Python implementation (NumPy)**  
  Input a_i lengths and joint variables (T1, T2, d3, …).  
  Convert angles to radians.  
  Build PT list [theta, alpha, a/r, d].  
  Manually code each 4×4 matrix using cos/sin.  
  Convert to np.array.  
  Print all individual matrices.  
  Chain with np.dot and print final H0_n (rounded to 3 decimals).

- **MATLAB implementation (Robotics Toolbox)**  
  Hard-code example link lengths.  
  Define each Link([θ, d, a, α, offset]).  
  Set qlim limits and sigma=1 for prismatic joints.  
  Build SerialLink.  
  Plot at home pose and use .teach.  
  Capture screenshot of visualization.

- **Verification – 5 test configurations**  
  Select 5 joint sets (zero + varied values).  
  Run both Python and MATLAB for each.  
  Capture Python output and MATLAB visualization.  
  Arrange side-by-side comparison images.

- **Documentation structure**  
  Manipulator title → diagrams → D-H table screenshot →  
  transformation matrix screenshots → MATLAB visualization →  
  Python code/output → 5 comparison pairs.

---
## 📂 Repository Structure

```
MATLAB_Code/
Python_Code/
Images/
README.md
```

## 👥 Group Members

- Bonado, Lance Exequiel M.  
- Fornal, Ian Avenick G.  
- Caparro, Stephen Jay G.  
- Solis, John King Louies R.  

---

<div align="Justify">


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

### 📋 Team Member Responsibilities & Instructions

#### 1. Project Engineer - **Bonado, Lance Exequiel M.**
* **Repository Setup:** Create the group laboratory repository on GitHub. **Ensure the repository is set to Private** and add the lecturer as a collaborator.
* **Naming Convention:**
  * Title the repository exactly as follows: 
  `Robotics2_Mechanical_Manipulator_Simulation_Section_Group#_Laboratory1_2026`
* **Documentation:** Write these laboratory instructions and procedures into the repository's `README.md` file.
* **Kinematics & Formatting:** * Draw the kinematic diagram with proper labels.
  * Construct the parametric table.
  * Derive the Homogeneous Transformation matrices of the mechanical manipulator assigned to your group.
  * Upload and post the pictures directly in the GitHub ReadMe file.
* **Manipulator Link:** 
  > **Assigned Manipulator:** [https://github.com/MikkoDT/Robotics_MEXE_3rdYearCourse/blob/main/MexE_409_Robotics_2/Laboratory_Activities/Laboratory_1_Mechanical_Manipulators.pdf]  
 
* **Data Integration:** Post the simulations and the analytical comparisons of the Python and MATLAB findings.

#### 2. Programmer 1 (Python) - **Fornal, Ian Avenick G.**
* **Scripting:** Program the assigned mechanical manipulator in Python using the codes your lecturer taught you.
* **Parameters:** Assign only **one** set of link lengths.
* **Testing:** Test **5 test points**, meaning 5 different sets of values for joint variables.
* **Submission:** Post your program in a folder inside the repository created by your Project Engineer.

#### 3. Programmer 2 (MATLAB) - **Caparro, Stephen Jay G.**
* **Scripting:** Program the assigned mechanical manipulator in MATLAB with Robotics Toolbox by Peter Corke using the codes your lecturer taught you.
* **Parameters:** Assign only **one** set of link lengths.
* **Testing:** Test **5 test points**, meaning 5 different sets of values for joint variables.
* **Submission:** Post your program in a folder inside the repository created by your Project Engineer.

#### 4. Project Leader - **Solis, John King Louies R.**
* **Presentation Prep:** Prepare a **10-minute presentation** of the laboratory. (Strictly 10 minutes only).
* **Presentation Content:** You will present the following:
  1. The kinematic diagram with labels, parametric table, and Homogeneous Transformation matrices of the mechanical manipulator assigned to your group.
  2. The simulation and comparison of the 2 simulations.
  3. Verification of how the simulations are correct (Based on what I taught).
  4. Conclusion.
* **Defense Coordination:** For the other 3 members, prepare them for the **5-minute question and answer** portion.

* ### 📝 Standard D-H Transformation Matrix Reference
*Students: Utilize the standard Denavit-Hartenberg transformation matrix for your calculations:*
```text
[ cos(θn)  -sin(θn)cos(αn)   sin(θn)sin(αn)  rn*cos(θn) ]
[ sin(θn)   cos(θn)cos(αn)  -cos(θn)sin(αn)  rn*sin(θn) ]
[   0         sin(αn)          cos(αn)          dn      ]
[   0            0                0              1      ]
```
### Reference Grading Rubric (Total: 60 Points)

| Intended Learning Outcome (ILO) | Description | Points |
| :--- | :--- | :---: |
| **ILO1 (SO1)** | Calculate the Forward and Inverse Kinematics of 3-DOF robotic manipulators using D-H parameters and Graphical Methods. | 5 pts |
| **ILO2 (SO5)** | Analyze robotic motion by computing the Jacobian Matrix to identify singularities and velocity relationships in 3-DOF and 6-DOF manipulators. | 10 pts |
| **ILO3 (SO11)** | Utilize modern engineering tools, such as Python, MATLAB, and Arduino, to implement trajectory planning and simulate robotic control systems. | 25 pts |
| **ILO4 (SO7)** | Present effective technical reports and design documentation through laboratory manuals and a professional portfolio website hosted on GitHub. | 20 pts |

---
## Manipulator Assigned for the Group: **Selective Compliance Assembly Robot Arm (SCARA)**

<div align="center">
  <table border="0" cellspacing="20">
    <tr>
      <td align="center">
        <img 
          width="480" 
          alt="SCARA kinematic diagram" 
           src="https://github.com/user-attachments/assets/37cab900-f4af-4a59-8160-0724bd51c021"
        />
        <br>
        <em> SCARA MANIPULATOR #1 </em>
      </td>
      <td align="center">
        <img 
          width="480" 
          alt="SCARA DH parameters and configuration" 
         src="https://github.com/user-attachments/assets/9fdb154d-a1e5-4025-adb6-9ecb3f737cb4"
        />
        <br>
        <em> SCARA MANIPULATOR #2 </em>
      </td>
    </tr>
  </table>
</div>

<p align="center">
  <em>Figure 1 & 2. Assigned SCARA manipulator </em>
</p>

---
# SCARA Manipulator #1 (3-DOF)

<div align="center">
  <img 
    width="780" 
    alt="SCARA 3-DOF manipulator overview" 
    src="https://github.com/user-attachments/assets/bf96a556-15d2-4634-ba76-45fbea6dbe35"
  />
  <br><br>
  <em>Figure 1. Assigned 3-DOF SCARA manipulator (RR-P configuration)</em>
</div>

## 1. Denavit-Hartenberg (D-H) Notations

### Step 1: Assign Frames according to the 4 D-H Rules

### Step 2: D-H Parametric Table

<div align="center">
  <img 
    width="480" 
    alt="D-H parameter table for 3-DOF SCARA" 
    src="https://github.com/user-attachments/assets/d50d9685-9032-45d1-935b-8887bb679778"
  />
  <br>
  <em>Table 1. D-H parameters for the assigned SCARA #1</em>
</div>

### Step 3: Homogeneous Transformation Matrices

**Using the standard D-H transformation matrix:**

<div align="center">
  <img 
    width="520" 
    alt="Transformation matrix H0_1" 
    src="https://github.com/user-attachments/assets/92a7c4e3-e4c7-421a-a3d5-0ffd95c08c8c"
  />
  <img 
    width="520" 
    alt="Transformation matrix H1_2 and H2_3" 
    src="https://github.com/user-attachments/assets/89f9ec0f-751c-41ef-a5c0-b207387bce18"
  />
</div>

<p align="center">
  <em>Figure 2 & 3. Individual transformation matrices (left: H₀¹, right: H₁² & H₂³)</em>
</p>

## 2. MATLAB Implementation (Robotics Toolbox)

<div align="center">
  <img 
    width="900" 
    alt="MATLAB Robotics Toolbox visualization of SCARA V3" 
    src="https://github.com/user-attachments/assets/ad8665fe-bd3e-46f6-9df6-ba80258756db"
  />
  <br>
  <em>Figure 4. SCARA V3 model visualization in MATLAB</em>
</div>

### MATLAB Code

```matlab
%%
disp('SCARAV3')
syms a1 a2 a3 a4 a5

%% link lengths
a1 = 7;
a2 = 7;
a3 = 7;
a4 = 7;
a5 = 5;

%% joint variables

%% D-H Parameters [theta, d, r, alpha, offset]

%if prismatic joint: theta = theta, d = 0, offset = 1, after offset put
%the value of d 

% if revolute joint : theta = 0, offset = 0, after offset put the value of 
% theta 

H0_1 = Link([0,a1,a2,0,0,0]); % revolute joint
H0_1.qlim = [-pi/2 pi/2];

H1_2 = Link([0,a3,a4,pi,0,0]); % revolute joint
H1_2.qlim = [-pi/2 pi/2];

H2_3 = Link([0,0,0,0,1,a5]); % prismatic joint
H2_3.qlim = [0 d3];

Scara_V3 = SerialLink([H0_1 H1_2 H2_3], 'name', 'SCARA_V3');
Scara_V3.plot([0 0 0], 'workspace', [-5 18 -18 18 0 18])
Scara_V3.teach 
```
### PYTHON Code
```PYTHON
import numpy as np

# link lengths in mm
a1 = float(input("a1 = "))
a2 = float(input("a2 = "))
a3 = float(input("a3 = "))
a4 = float(input("a4 = "))
a5 = float(input("a5 = "))

# joint variables: i is mm if d, is degrees if theta
T1 = float(input("T1 = "))
T2 = float(input("T2 = "))
d3 = float(input("d3 = "))

# degree to radian
T1 = (T1 / 180) * np.pi
T2 = (T2 / 180) * np.pi

# Parametric Table (theta, alpha, r, d)
PT = [
    [(0/180)*np.pi + T1, (0/180)*np.pi,   a2, a1],
    [(0/180)*np.pi + T2, (180/180)*np.pi, a4, a3],
    [(0/180)*np.pi,      (0/180)*np.pi,   0,  a5 + d3],
]

# HTM Formula

# H0_1
i = 0
H0_1 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H1_2
i = 1
H1_2 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H2_3
i = 2
H2_3 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# Convert to numpy arrays
H0_1 = np.array(H0_1)
print("H0_1 = ")
print(H0_1)

H1_2 = np.array(H1_2)
print("H1_2 = ")
print(H1_2)

H2_3 = np.array(H2_3)
print("H2_3 = ")
print(H2_3)

# Overall Transformation
H0_2 = np.dot(H0_1, H1_2)
H0_3 = np.dot(H0_2, H2_3)

print("H0_3 = ")
print(np.around(H0_3, 3))
```
## Comparison of Python vs MATLAB Simulation Results

Each comparison shows:
- **Left**: Python simulation result  
- **Right**: MATLAB simulation result

<div align="center">

### Comparison 1
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 1" src="https://github.com/user-attachments/assets/66a42ecf-6c00-4aa3-8fcb-c3fea7caeef4" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 1" src="https://github.com/user-attachments/assets/28e7a093-c9c6-4e1b-bfda-6f926bd3310f" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

### Comparison 2
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 2" src="https://github.com/user-attachments/assets/600fba2f-9f6a-45c0-8d21-6eda175f9ce2" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 2" src="https://github.com/user-attachments/assets/dbead1f8-0528-4df8-aaa8-6fe5e82c6435" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

### Comparison 3
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 3" src="https://github.com/user-attachments/assets/b06661b1-db5c-46b6-b4fd-e15e8c4092f1" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 3" src="https://github.com/user-attachments/assets/cd5a8c62-2771-4a2c-89ec-4a42c0a6d610" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

### Comparison 4
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 4" src="https://github.com/user-attachments/assets/e3fb67c8-1d8f-4e10-b639-6ade4828827d" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 4" src="https://github.com/user-attachments/assets/940d296c-28c0-4622-926d-8969d9047577" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

### Comparison 5
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 5" src="https://github.com/user-attachments/assets/fd3a8b7d-a6e8-4917-8c01-276d9c473523" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 5" src="https://github.com/user-attachments/assets/784e72c7-05fc-43b8-9d3d-fdf0be1c17f4" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

</div>

<p align="center"><em>Figure set: Side-by-side visual comparison of forward kinematics results from Python (NumPy) and MATLAB (Robotics Toolbox) for the 5 test configurations.</em></p>

# SCARA Manipulator #2 (3-DOF)

<div align="center">
  <img 
    width="780" 
    alt="SCARA Manipulator #2 overview" 
    src="https://github.com/user-attachments/assets/1d3b4fb2-fac7-4ea9-87f9-7b84b42184d1"
  />
  <br><br>
  <em>Figure 1. Assigned 3-DOF SCARA manipulator #2 (kinematic structure)</em>
</div>

## 1. Denavit-Hartenberg (D-H) Notations

### Step 1: Assign Frames according to the 4 D-H Rules

### Step 2: D-H Parametric Table

<div align="center">
  <img 
    width="480" 
    alt="D-H parameter table for SCARA #2" 
    src="https://github.com/user-attachments/assets/8e867904-0090-4e9a-90f3-0f5f86d690fd"
  />
  <br>
  <em>Table 1. D-H parameters for SCARA Manipulator #2</em>
</div>

### Step 3: Homogeneous Transformation Matrices

**Using the standard D-H transformation matrix formula:**

<div align="center">
  <table border="0" cellspacing="15">
    <tr>
      <td align="center">
        <img width="520" alt="Transformation matrix H0_1" src="https://github.com/user-attachments/assets/4baab8bd-ddf7-444e-bcf2-e30d2b61a326" />
        <br>
      </td>
      <td align="center">
        <img width="520" alt="Transformation matrix H1_2" src="https://github.com/user-attachments/assets/d7a8c95f-43a6-4451-ba68-d544ba2c0885" />
        <br>
      </td>
    </tr>
    <tr>
      <td align="center" colspan="2">
        <img width="520" alt="Transformation matrix H2_3 and H3_4" src="https://github.com/user-attachments/assets/26baa9cd-5c34-4dc6-a8ee-f9a001ee4f6c" />
        <br>
      </td>
    </tr>
  </table>
</div>

<p align="center">
  <em>Figure 2–4. Individual homogeneous transformation matrices derived from the D-H table</em>
</p>

## 2. MATLAB Implementation (Robotics Toolbox)

<div align="center">
  <img 
    width="900" 
    alt="MATLAB visualization of SCARA V3 #2" 
    src="https://github.com/user-attachments/assets/c7c3f3d4-8019-47ed-8d07-d8a2a4c12ac8"
  />
  <br>
  <em>Figure 5. SCARA V3 model visualization in MATLAB (Manipulator #2)</em>
</div>

### MATLAB Code

```matlab
%%
disp('SCARAV3')
syms a1 a2 a3 a4 

%% link lengths
a1 = 7;
a2 = 7;
a3 = 7;
a4 = 7;
    
%% joint variable
d3 = 5;
%% D-H Parameters [theta, d, r, alpha, offset]

%if prismatic joint: theta = theta, d = 0, offset = 1, after offset put
%the value of d 

% if revolute joint : theta = 0, offset = 0, after offset put the value of 
% theta 

H0_1 = Link([0,a1,0,pi/2,0,0]); % base
H0_1.qlim = [0 0];

H1_2 = Link([0,0,0,3*pi/2,0,0]); % revolute joints
H1_2.qlim = [-pi/6 pi/2];

H2_3 = Link([0,a2,0,3*pi/2,0,3*pi/2]); % revolute joints
H2_3.qlim = [-pi/2 pi/2];

H3_4 = Link([0,0,0,0,1,a3+a4]); % prismatic joints
H3_4.qlim = [0 d3];

Scara_V3 = SerialLink([H0_1 H1_2 H2_3 H3_4], 'name', 'SCARA_V3');
Scara_V3.plot([0 0 0 0], 'workspace', [-10 20 -20 20 0 25])
Scara_V3.teach
```
### PYTHON Code
```python code
import numpy as np

# link lengths in mm
a1 = float(input("a1 = "))
a2 = float(input("a2 = "))
a3 = float(input("a3 = "))
a4 = float(input("a4 = "))

# joint variables: i is mm if d, is degrees if theta
T1 = float(input("T1 = "))
T2 = float(input("T2 = "))
d3 = float(input("d3 = "))

# degree to radian
T1 = (T1 / 180) * np.pi
T2 = (T2 / 180) * np.pi

# Parametric Table (theta, alpha, r, d)
PT = [
    [(0/180)*np.pi,       (90/180)*np.pi,  0,   a1      ],
    [(0/180)*np.pi + T1,  (270/180)*np.pi, 0,   0       ],
    [(270/180)*np.pi + T2,(270/180)*np.pi, 0,   a2      ],
    [(0/180)*np.pi,       (0/180)*np.pi,   0,   a3 + a4 + d3],
]

# HTM Formula

# H0_1
i = 0
H0_1 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H1_2
i = 1
H1_2 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H2_3
i = 2
H2_3 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H3_4
i = 3
H3_4 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# Convert to numpy arrays
H0_1 = np.array(H0_1)
print("H0_1 = ")
print(H0_1)

H1_2 = np.array(H1_2)
print("H1_2 = ")
print(H1_2)

H2_3 = np.array(H2_3)
print("H2_3 = ")
print(H2_3)

H3_4 = np.array(H3_4)
print("H3_4 = ")
print(H3_4)

# Overall Transformation
H0_2 = np.dot(H0_1, H1_2)
H0_3 = np.dot(H0_2, H2_3)
H0_4 = np.dot(H0_3, H3_4)

print("H0_4 = ")
print(np.around(H0_4, 3))
```
## Comparison of Python vs MATLAB Simulation Results

Each comparison shows:
- **Left**: Python simulation result  
- **Right**: MATLAB simulation result (Robotics Toolbox visualization)

<div align="center">

### Comparison 1
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 1" src="https://github.com/user-attachments/assets/79563dfe-4ba6-450e-aad2-4eac49c4ea30" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 1" src="https://github.com/user-attachments/assets/42e8b0c0-b997-4fb6-a4e1-eb34422688fc" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

### Comparison 2
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 2" src="https://github.com/user-attachments/assets/277e1f4f-57b9-440e-9be8-a75541c75635" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 2" src="https://github.com/user-attachments/assets/515b9c9f-2e79-4d66-9a1d-4150ca6f5e3d" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

### Comparison 3
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 3" src="https://github.com/user-attachments/assets/16eec7e9-e0ae-4270-b35f-11d528b77b53" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 3" src="https://github.com/user-attachments/assets/5819bc9e-44e2-4e71-ac24-a68fde72e3e6" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

### Comparison 4
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 4" src="https://github.com/user-attachments/assets/f7679002-85bb-4d7b-bc74-a37d495bb74e" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 4" src="https://github.com/user-attachments/assets/7104a290-01c1-4a28-9daa-74b37a46a378" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

### Comparison 5
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 5" src="https://github.com/user-attachments/assets/75fdf0df-3113-4128-ae9c-8e503323c626" />
      <br><em>Python</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 5" src="https://github.com/user-attachments/assets/2aa5e3af-cfed-4fb6-a444-1dc076f3fc43" />
      <br><em>MATLAB</em>
    </td>
  </tr>
</table>

</div>

<p align="center">
  <em>Figure set: Side-by-side visual comparison of forward kinematics results from Python (NumPy) and MATLAB (Robotics Toolbox) for the 5 test configurations.</em>
</p>

## SCARA Manipulator #1 (6-DOF) with Spherical Wrist

<div align="center">
  <img 
    width="680" 
    alt="SCARA 6-DOF manipulator overview" 
    src="https://github.com/user-attachments/assets/ad8bf2fe-20ec-4137-b4b2-a72b2c25901f"
  />
  <br><br>
  <em>Figure 1. Assigned 6-DOF SCARA manipulator (base + arm configuration)</em>
</div>

## Spherical Wrist (Added for 6-DOF)

The spherical wrist provides the final three rotational degrees of freedom (typically joints 4, 5, and 6), enabling full orientation control of the end-effector.

<div align="center">
  <img 
    width="380" 
    alt="Spherical wrist detail" 
    src="https://github.com/user-attachments/assets/11201627-30a6-43a2-8ad9-c520d82b8b1a"
  />
  <br><br>
  <em>Figure 2. Close-up of the spherical wrist mechanism (joints 4–6)</em>
</div>

## 1. Denavit-Hartenberg (D-H) Notations

### Step 1: Assign Frames according to the 4 D-H Rules

### Step 2: D-H Parametric Table

<div align="center">
  <img 
    width="480" 
    alt="D-H parameter table for 6-DOF SCARA" 
    src="https://github.com/user-attachments/assets/907129b9-7fc3-4d56-b701-6fa8c4f352b1"
  />
  <br>
  <em>Table 1. D-H parameters for the 6-DOF SCARA manipulator</em>
</div>

### Step 3: Homogeneous Transformation Matrices

**Using the standard D-H transformation matrix formula:**

<div align="center">
  <table border="0" cellspacing="15">
    <tr>
      <td align="center">
        <img width="480" alt="Transformation matrix H0_1" src="https://github.com/user-attachments/assets/3e2040ac-b42c-4c27-aa52-942f8ca7032c" />
        <br>
      </td>
      <td align="center">
        <img width="480" alt="Transformation matrix H1_2" src="https://github.com/user-attachments/assets/4b685cd3-36c1-4ca6-9cc7-38f8706aca90" />
        <br>
      </td>
    </tr>
    <tr>
      <td align="center">
        <img width="480" alt="Transformation matrix H2_3" src="https://github.com/user-attachments/assets/ce484231-6fbd-4d4a-96f0-88812431692c" />
        <br>
      </td>
      <td align="center">
        <img width="480" alt="Transformation matrix H3_4" src="https://github.com/user-attachments/assets/16f10a12-3e7b-4a98-8dd7-e79c806254a7" />
        <br>
      </td>
    </tr>
  </table>
</div>

<p align="center">
  <em>Figure 3–6. Individual homogeneous transformation matrices (H₀¹ to H₃⁴ shown; remaining matrices follow similar derivation)</em>
</p>

## 2. MATLAB Implementation (Robotics Toolbox)

<div align="center">
  <img 
    width="900" 
    alt="MATLAB visualization of 6-DOF SCARA" 
    src="https://github.com/user-attachments/assets/f61f1012-3ceb-4092-badb-d0f1a0e124b6"
  />
  <br>
  <em>Figure 7. 6-DOF SCARA model with spherical wrist in MATLAB</em>
</div>

### MATLAB Code

```matlab
%%
disp('SCARAV3')

%% link lengths
a1 = 10;
a2 = 10;
a3 = 10;
a4 = 10;
a5 = 3;
a6 = 3;
a7 = 3;
a8 = 3;

%% joint variables

T1 = 0;
T2 = 0;
d3 = 3;
T4 = 0;
T5 = 0;
T6 = 0;

%% D-H Parameters [theta, d, r, alpha, offset]

%if prismatic joint: theta = theta, d = 0, offset = 1, after offset put
%the value of d 

% if revolute joint : theta = 0, offset = 0, after offset put the value of 
% theta 

H0_1 = Link([0,a1,a2,0,0,0]); % revolute joint
H0_1.qlim = [-pi/2 pi/2];

H1_2 = Link([0,a3,a4,pi,0,0]); % revolute joint
H1_2.qlim = [-pi/2 pi/2];

H2_3 = Link([0,0,0,0,1,a5]); % prismatic joint
H2_3.qlim = [0 d3];

H3_4 = Link([0,a6,0,3*pi/2,0,0]);     % revolute: theta = q4, alpha=90°=pi/2
H3_4.qlim = [-pi/2 pi/2];

H4_5 = Link([0, 0,0,pi/2,0,0]);     % revolute: theta = q5, alpha=90°=pi/2
H4_5.qlim = [-pi/2 pi/2];

H5_6 = Link([0, a7+a8,0,0,0,0]);    % revolute: theta = q6, d = a7+a8
H5_6.qlim = [-pi/2 pi/2];

Scara_V3 = SerialLink([H0_1 H1_2 H2_3 H3_4 H4_5 H5_6], 'name', 'SCARA_V3');
Scara_V3.plot([0 0 0 0 0 0], 'workspace', [-30 30 -30 30 0 30],'scale', 0.5)
Scara_V3.teach
```
### PYTHON Code

```python
import numpy as np

# link lengths in mm
a1 = float(input("a1 = "))
a2 = float(input("a2 = "))
a3 = float(input("a3 = "))
a4 = float(input("a4 = "))
a5 = float(input("a5 = "))
a6 = float(input("a6 = "))
a7 = float(input("a7 = "))
a8 = float(input("a8 = "))

# joint variables: i is mm if d, is degrees if theta
T1 = float(input("T1 = "))
T2 = float(input("T2 = "))
d3 = float(input("d3 = "))
T4 = float(input("T4 = "))
T5 = float(input("T5 = "))
T6 = float(input("T6 = "))

# degree to radian
T1 = (T1 / 180) * np.pi
T2 = (T2 / 180) * np.pi
T4 = (T4 / 180) * np.pi
T5 = (T5 / 180) * np.pi
T6 = (T6 / 180) * np.pi

# Parametric Table (theta, alpha, r, d)
PT = [
    [(0/180)*np.pi + T1, (0/180)*np.pi,   a2, a1         ],
    [(0/180)*np.pi + T2, (180/180)*np.pi, a4, a3         ],
    [(0/180)*np.pi,      (0/180)*np.pi,   0,  a5 + d3    ],
    [(0/180)*np.pi + T4, (270/180)*np.pi, 0,  a6         ],
    [(0/180)*np.pi + T5, (90/180)*np.pi,  0,  0          ],
    [(0/180)*np.pi + T6, (0/180)*np.pi,   0,  a7 + a8    ],
]

# HTM Formula

# H0_1
i = 0
H0_1 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H1_2
i = 1
H1_2 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H2_3
i = 2
H2_3 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H3_4
i = 3
H3_4 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H4_5
i = 4
H4_5 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H5_6
i = 5
H5_6 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# Convert to numpy arrays
H0_1 = np.array(H0_1)
print("H0_1 = ")
print(H0_1)

H1_2 = np.array(H1_2)
print("H1_2 = ")
print(H1_2)

H2_3 = np.array(H2_3)
print("H2_3 = ")
print(H2_3)

H3_4 = np.array(H3_4)
print("H3_4 = ")
print(H3_4)

H4_5 = np.array(H4_5)
print("H4_5 = ")
print(H4_5)

H5_6 = np.array(H5_6)
print("H5_6 = ")
print(H5_6)

# Overall Transformation
H0_2 = np.dot(H0_1, H1_2)
H0_3 = np.dot(H0_2, H2_3)
H0_4 = np.dot(H0_3, H3_4)
H0_5 = np.dot(H0_4, H4_5)
H0_6 = np.dot(H0_5, H5_6)

print("H0_6 = ")
print(np.around(H0_6, 3))
```
## Comparison of Python vs MATLAB Simulation Results

Each comparison shows:  
- **Left**: MATLAB simulation result (Robotics Toolbox visualization)  
- **Right**: Python simulation result (NumPy forward kinematics)

<div align="center">

### Comparison 1
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="MATLAB result 1" src="https://github.com/user-attachments/assets/7b373907-894a-42b7-9028-857655d610b8" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="Python result 1" src="https://github.com/user-attachments/assets/cd39ce7c-2fb4-41fe-814b-492039fb6cf6" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

### Comparison 2
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="MATLAB result 2" src="https://github.com/user-attachments/assets/956a4b60-508d-46cc-9615-e40566334bfe" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="Python result 2" src="https://github.com/user-attachments/assets/cd63ff48-7aaf-4643-82fc-e281146ed8b1" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

### Comparison 3
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="MATLAB result 3" src="https://github.com/user-attachments/assets/0309d3ce-e300-4ce9-af8b-dc9b06d8bb00" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="Python result 3" src="https://github.com/user-attachments/assets/3b32b1ce-ff0d-493a-afa7-bceb4d65cf54" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

### Comparison 4
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="MATLAB result 4" src="https://github.com/user-attachments/assets/c7b202e5-9e49-4245-981d-2aeef19a1fb0" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="Python result 4" src="https://github.com/user-attachments/assets/13af42d0-eb0c-48e1-8a19-39871cd7ec63" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

### Comparison 5
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="MATLAB result 5" src="https://github.com/user-attachments/assets/b3054432-19c8-4368-9dce-7936bef88118" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="Python result 5" src="https://github.com/user-attachments/assets/1a46dbba-61bb-4e29-a772-1e0a15b54e4f" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

</div>

<p align="center">
  <em>Figure set: Side-by-side visual comparison of forward kinematics results from MATLAB (Robotics Toolbox) and Python (NumPy) across the 5 test configurations.</em>
</p>

## SCARA Manipulator #2 (6-DOF) with Spherical Wrist

<div align="center">
  <img 
    width="780" 
    alt="SCARA 6-DOF manipulator #2 overview" 
    src="https://github.com/user-attachments/assets/0d371403-3541-4da8-ae8b-4b02df5e5e40"
  />
  <br><br>
  <em>Figure 1. Assigned 6-DOF SCARA manipulator #2 (base + arm configuration)</em>
</div>

## Spherical Wrist (Added for 6-DOF)

The spherical wrist provides the final three rotational degrees of freedom, allowing full orientation control of the end-effector.

<div align="center">
  <img 
    width="380" 
    alt="Spherical wrist detail" 
    src="https://github.com/user-attachments/assets/db85a3ca-1467-4547-a248-90cb96d07bfc"
  />
  <br><br>
  <em>Figure 2. Close-up of the spherical wrist (joints 5–7)</em>
</div>



## 1. Denavit-Hartenberg (D-H) Notations

### Step 1: Assign Frames according to the 4 D-H Rules

### Step 2: D-H Parametric Table

<div align="center">
  <img 
    width="480" 
    alt="D-H parameter table for SCARA #2 6-DOF" 
    src="https://github.com/user-attachments/assets/a6b9c2ab-7d38-411b-9abc-b03b88d5dd40"
  />
  <br>
  <em>Table 1. D-H parameters for SCARA Manipulator #2 (6-DOF)</em>
</div>

### Step 3: Homogeneous Transformation Matrices

**Using the standard D-H transformation matrix formula:**

<div align="center">
  <table border="0" cellspacing="15">
    <tr>
      <td align="center">
        <img width="520" alt="Transformation matrix H0_1" src="https://github.com/user-attachments/assets/a3e80421-1b0c-481b-83d4-5b5550c0d4a0" />
        <br>
      </td>
      <td align="center">
        <img width="520" alt="Transformation matrix H1_2" src="https://github.com/user-attachments/assets/c6fb3f96-4f0a-485d-a9fc-39ae234ef7c4" />
        <br>
      </td>
    </tr>
    <tr>
      <td align="center">
        <img width="520" alt="Transformation matrix H2_3" src="https://github.com/user-attachments/assets/2b30f066-15c9-4fbd-a149-ad88aa1e2f52" />
        <br>
      </td>
      <td align="center">
        <img width="520" alt="Transformation matrix H3_4" src="https://github.com/user-attachments/assets/3f1febe6-d87c-479b-b08c-c30b98eb1e2d" />
        <br>
      </td>
    </tr>
  </table>
</div>

<p align="center">
  <em>Figure 3–6. Individual homogeneous transformation matrices (H₀¹ to H₃⁴ shown; remaining matrices follow similar derivation)</em>
</p>

## 2. MATLAB Implementation (Robotics Toolbox)

<div align="center">
  <img 
    width="900" 
    alt="MATLAB visualization of SCARA #2 6-DOF" 
    src="https://github.com/user-attachments/assets/ad928cf2-e0f8-462b-b4f3-27bd66d6d36d"
  />
  <br>
  <em>Figure 7. 6-DOF SCARA model with spherical wrist in MATLAB</em>
</div>

### MATLAB Code

```matlab
%%
disp('SCARAV3')

%% link lengths
a1 = 5;
a2 = 5;
a3 = 3;
a4 = 3;
a5 = 3;
a6 = 3;
a7 = 3;

%% joint variables

T1 = 0;
T2 = 0;
d3 = 3;
T4 = 0;
T5 = 0;
T6 = 0;

%% D-H Parameters [theta, d, r, alpha, offset]

%if prismatic joint: theta = theta, d = 0, offset = 1, after offset put
%the value of d 

% if revolute joint : theta = 0, offset = 0, after offset put the value of 
% theta 

H0_1 = Link([0,a1,0,pi/2,0,0]); % base
H0_1.qlim = [0 0];

H1_2 = Link([0,0,0,3*pi/2,0,0]); % revolute joints
H1_2.qlim = [-pi/6 pi/2];

H2_3 = Link([0,a2,0,3*pi/2,0,3*pi/2]); % revolute joints
H2_3.qlim = [-pi/2 pi/2];

H3_4 = Link([0,0,0,0,1,a3+a4]); % prismatic joints
H3_4.qlim = [0 3];

H4_5 = Link([0,a5,0,3*pi/2,0,0]);     % revolute joints
H4_5.qlim = [-pi/2 pi/2];

H5_6 = Link([0,0,0,pi/2,0,3*pi/2]);    % revolute joints
H5_6.qlim = [-pi/6 pi/2];

H6_7 = Link([0,a6+a7,0,0,0,0]);    % revolute joints
H6_7.qlim = [-pi/2 pi/2];

Scara_V3 = SerialLink([H0_1 H1_2 H2_3 H3_4 H4_5 H5_6 H6_7], 'name', 'SCARA_V3');
Scara_V3.plot([0 0 0 0 0 0 0], 'workspace', [-5 18 -18 18 0 18],'scale', 0.5)
Scara_V3.teach
```

### PYTHON Code 

```python
import numpy as np

# link lengths in mm
a1 = float(input("a1 = "))
a2 = float(input("a2 = "))
a3 = float(input("a3 = "))
a4 = float(input("a4 = "))
a5 = float(input("a5 = "))
a6 = float(input("a6 = "))
a7 = float(input("a7 = "))

# joint variables: i is mm if d, is degrees if theta
T1 = float(input("T1 = "))
T2 = float(input("T2 = "))
d3 = float(input("d3 = "))
T4 = float(input("T4 = "))
T5 = float(input("T5 = "))
T6 = float(input("T6 = "))

# degree to radian
T1 = (T1 / 180) * np.pi
T2 = (T2 / 180) * np.pi
T4 = (T4 / 180) * np.pi
T5 = (T5 / 180) * np.pi
T6 = (T6 / 180) * np.pi

# Parametric Table (theta, alpha, r, d)
PT = [
    [(0/180)*np.pi,       (90/180)*np.pi,  0,   a1               ],
    [(0/180)*np.pi + T1,  (270/180)*np.pi, 0,   0                ],
    [(270/180)*np.pi + T2,(270/180)*np.pi, 0,   a2               ],
    [(0/180)*np.pi,       (0/180)*np.pi,   0,   a3 + a4 + d3     ],
    [(0/180)*np.pi + T4,  (270/180)*np.pi, 0,   a5               ],
    [(270/180)*np.pi + T5,(90/180)*np.pi,  0,   0                ],
    [(0/180)*np.pi + T6,  (0/180)*np.pi,   0,   a6 + a7          ],
]

# HTM Formula

# H0_1
i = 0
H0_1 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H1_2
i = 1
H1_2 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H2_3
i = 2
H2_3 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H3_4
i = 3
H3_4 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H4_5
i = 4
H4_5 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H5_6
i = 5
H5_6 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# H6_7
i = 6
H6_7 = [
    [np.cos(PT[i][0]), -np.sin(PT[i][0])*np.cos(PT[i][1]),  np.sin(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.cos(PT[i][0])],
    [np.sin(PT[i][0]),  np.cos(PT[i][0])*np.cos(PT[i][1]), -np.cos(PT[i][0])*np.sin(PT[i][1]), PT[i][2]*np.sin(PT[i][0])],
    [0,                 np.sin(PT[i][1]),                   np.cos(PT[i][1]),                  PT[i][3]],
    [0, 0, 0, 1]
]

# Convert to numpy arrays
H0_1 = np.array(H0_1)
print("H0_1 = ")
print(H0_1)

H1_2 = np.array(H1_2)
print("H1_2 = ")
print(H1_2)

H2_3 = np.array(H2_3)
print("H2_3 = ")
print(H2_3)

H3_4 = np.array(H3_4)
print("H3_4 = ")
print(H3_4)

H4_5 = np.array(H4_5)
print("H4_5 = ")
print(H4_5)

H5_6 = np.array(H5_6)
print("H5_6 = ")
print(H5_6)

H6_7 = np.array(H6_7)
print("H6_7 = ")
print(H6_7)

# Overall Transformation
H0_2 = np.dot(H0_1, H1_2)
H0_3 = np.dot(H0_2, H2_3)
H0_4 = np.dot(H0_3, H3_4)
H0_5 = np.dot(H0_4, H4_5)
H0_6 = np.dot(H0_5, H5_6)
H0_7 = np.dot(H0_6, H6_7)

print("H0_7 = ")
print(np.around(H0_7, 3))
```
## Comparison of Python vs MATLAB Simulation Results

Each comparison shows:  
- **Left**: MATLAB simulation result (Robotics Toolbox visualization)  
- **Right**: Python simulation result (NumPy forward kinematics)

<div align="center">

### Comparison 1
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img  width="480" alt="Python result 1" src="https://github.com/user-attachments/assets/055a3650-4b57-46f8-8e3e-446828821820"/>
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 1" src="https://github.com/user-attachments/assets/19fc37e4-e1f4-4d4f-b4e3-ef961436fc85" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

### Comparison 2
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 2" src="https://github.com/user-attachments/assets/d06a7ebc-f112-4822-b4f8-082fdbcd9431" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 2" src="https://github.com/user-attachments/assets/e69d2f4b-d2de-49e3-9f8e-17cde6cd871a" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

### Comparison 3
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 3" src="https://github.com/user-attachments/assets/74f25773-c70f-4c7c-a7cd-273bc0604d29" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 3" src="https://github.com/user-attachments/assets/4880e422-6337-4a77-ba55-4f8afbcc4c95" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

### Comparison 4
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 4" src="https://github.com/user-attachments/assets/80390e83-45a7-4ee9-987c-cd2bf1afdd54" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 4" src="https://github.com/user-attachments/assets/8b2364ec-28a9-4c62-93d5-d209a745286c" />
      <br><em>Python</em>
    </td>
  </tr>
</table>

### Comparison 5
<table border="0" cellspacing="20">
  <tr>
    <td align="center">
      <img width="480" alt="Python result 5" src="https://github.com/user-attachments/assets/dbbae797-5495-4500-a8b4-d407df3260b4" />
      <br><em>MATLAB</em>
    </td>
    <td align="center">
      <img width="480" alt="MATLAB result 5" src="https://github.com/user-attachments/assets/4dbad36a-2773-4632-9181-57eb206d3693"  />
      <br><em>Python</em>
    </td>
  </tr>
</table>

</div>

<p align="center">
  <em>Figure set: Side-by-side visual comparison of forward kinematics results from MATLAB (Robotics Toolbox) and Python (NumPy) across the 5 test configurations.</em>
</p>

## Conclusion – Laboratory 1: ##
**Mechanical Manipulator Simulation 🤖**

In this laboratory activity, we successfully modeled and simulated the forward kinematics of the assigned SCARA manipulators (3-DOF and 6-DOF configurations with spherical wrist) using two different approaches:

- **Python (NumPy)**: Manual implementation of Denavit-Hartenberg transformation matrices, step-by-step matrix multiplication, and direct computation of end-effector pose. 🐍
- **MATLAB (Robotics Toolbox)**: High-level modeling using Link and SerialLink objects, with built-in visualization and interactive teach mode. 🖥️

**Key observations and results:**
- Both implementations produced consistent end-effector positions and orientations across all tested joint configurations. ✅
- The side-by-side visual comparisons (5 test points per manipulator) confirmed good agreement between Python numerical results and MATLAB graphical output. 👀
- The spherical wrist in 6-DOF variants successfully enabled full orientation control while maintaining decoupling from position. 🔄
- Manual matrix derivation and chained multiplication in Python provided deeper insight into the transformation process, while MATLAB offered faster prototyping and intuitive 3D visualization. 📊✨

This laboratory demonstrated the reliability of the standard D-H convention for serial manipulators and highlighted the complementary strengths of low-level (Python) and toolbox-based (MATLAB) approaches in robotics simulation.


**Prepared by:**  
John King Louies R. Solis (Project Leader) 👑  
Ian Avenick G. Fornal (Python Programmer) 🐍  
Stephen Jay G. Caparro (MATLAB Programmer) 🖥️  
Lance Exequiel M. Bonado (Project Engineer) ⚙️ 


Thank you to the lecturer and course staff for the guidance and assigned manipulators. 
