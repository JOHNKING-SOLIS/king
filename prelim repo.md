#<div align="center">

# 🤖 MEXE 3202 – Robotics 2  
### Mechanical Manipulator Simulation  
### Laboratory 2 - Prelims  (2026)  
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

## 🎯 Project Objectives

1. Derive the kinematic model of the Spartan Robokit using Denavit-Hartenberg (D-H) parameters.
2. Integrate MATLAB with Arduino for robotic control.
3. Apply forward kinematics to actual robotic motion.
4. Perform a pick-and-place task.
5. Document the full system (hardware + software + analysis).

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

# 🦾 KINEMATICS ANALYSIS

## 🔹 Kinematic Diagram

Insert the labeled diagram of the Spartan Robokit below (show joints, links, coordinate frames, and directions of motion):

--![656826964_25459289267078580_8560801011013626232_n](https://github.com/user-attachments/assets/ba12c657-b86f-464b-8d34-1b6a9aad9962)


---

## 🔹 Homogeneous Transformation Matrices

### 🔸 Standard D-H Formula Used

[ cos(θi)  -sin(θi)cos(αi)   sin(θi)sin(αi)  ai*cos(θi) ]
[ sin(θi)   cos(θi)cos(αi)  -cos(θi)sin(αi)  ai*sin(θi) ]
[   0         sin(αi)          cos(αi)          di      ]
[   0            0                0              1      ]

---

1. Denavit-Hartenberg (D-H) Notations
Step 1: Assign Frames according to the 4 D-H Rules

![656826964_25459289267078580_8560801011013626232_n](https://github.com/user-attachments/assets/988fa7ec-a493-47ce-9291-9af096c51736)



Step 2: D-H Parametric Table

![653538507_34797554683191524_7175764395397224444_n](https://github.com/user-attachments/assets/ff805339-6796-4b12-8e46-b554170514da)



Step 3: Homogeneous Transformation Matrices
Using the standard D-H transformation matrix:

![653990871_1267525971417381_6504083263643205526_n](https://github.com/user-attachments/assets/dbd099bf-6088-4cdc-a434-06dada222f8b)
![655267471_1215592753988883_879055588574067030_n](https://github.com/user-attachments/assets/c23da29d-5410-44cd-84e2-78a5df3763fb)

---

## 🔹 Circuit Diagram

--dragram arduino pic

---



# 🧪 TESTING & RESULTS 


# 🎥 MOTION VALIDATION (5 MOVEMENTS)

## 🔹 Individual Movement Demonstrations

Each movement corresponds to a unique set of joint variables.


* *Movement 1 to 5  :*
(Insert description)
  [▶️ Watch Video](#)



https://github.com/user-attachments/assets/ac5c21b0-ab11-4983-9f66-112809161212



---

# 🎯 PICK-AND-PLACE DEMONSTRATION

## 🔹 Task Description

The robotic manipulator performs a pick-and-place operation using only forward kinematics calculations. The robot moves from an initial position, picks up an object, and transfers it to a target location.


---

## 🔹 Pick-and-Place Video

[▶️ Watch Pick-and-Place Demo](#)



https://github.com/user-attachments/assets/2e4260db-3bc3-4928-8ca6-8c2550e8daf2



---

## 🔹 Sequence of Operation

1. Move to initial position
2. Align end-effector with object
3. Activate gripper (pick)
4. Move to target location
5. Release object (place)

---

# 💻  CODES

## 🔹 MATLAB Code

--insert matlab code

## 🔹 Arduino Code

--insert arduino code

## 🔹 python Code

--insert python code

---

# 📸 DOCUMENTATION

## 🔹 Project Images

![223f552e-4d42-441e-bc7d-13b5999ed6ad](https://github.com/user-attachments/assets/71df8c51-c54f-48d6-a467-74f2119bf65b)


---

# ⚙️ CALIBRATION

## 🔹 Calibration Procedure

![087c1aea-2826-465e-a1fc-1486c16fe791](https://github.com/user-attachments/assets/c84bfc4f-468a-4b2f-9e64-90775763f3ed)

![649340084_1482395990009421_530936068278990065_n](https://github.com/user-attachments/assets/d222634a-beda-4908-9458-169b53b2b268)
![647924531_761401523495013_5028866445921834899_n](https://github.com/user-attachments/assets/a407594d-b038-480b-9c32-7b1efc6cd414)

![642358632_935319702813217_7064893558162541556_n](https://github.com/user-attachments/assets/8adcd71e-9ac0-43a3-8f92-cead70d372ef)
![653671507_961245206327184_4653076705075570788_n](https://github.com/user-attachments/assets/07038d0e-6fd2-4581-8dd0-ce53bddf2e66)
![642341077_1112760464313935_3172043573863414524_n](https://github.com/user-attachments/assets/3e850e68-81f5-4772-8597-fdd179474102)
![642589016_26593358656949034_6663102183343520272_n](https://github.com/user-attachments/assets/7a2a7ede-46a0-42e3-87d1-cd86e07f468c)



---

# 🦾 KINEMATIC DERIVATIONS

![648330498_1511123100442640_539532584344813030_n](https://github.com/user-attachments/assets/7af59ac1-c3a9-4671-91d9-484f1cb0eb37)
![649567747_2351388082007230_2834486893997274348_n](https://github.com/user-attachments/assets/45f2212f-6382-472e-8fb7-00a4763132cc)

---

# 🧪 TESTING

![Test Procedure](images/test_procedure.png)

![396b1ae7-fc12-4594-a944-708c0703b912](https://github.com/user-attachments/assets/5762b03c-936b-4566-999d-a67f76016ec3)
![9e05c933-e8c1-4e3c-88b2-dddf662e4f9e](https://github.com/user-attachments/assets/0f68e1b7-cd65-43d5-ac5d-5a1da8505d5e)
![92225516-1dcd-4341-afb3-a2faae42ed19](https://github.com/user-attachments/assets/2469b724-e8a6-4f68-b3ef-a062560467ff)


---

# 📊 ANALYSIS & VERIFICATION

* Forward kinematics equations were applied to compute end-effector position
* Actual robot motion was observed and recorded
* Experimental results were compared with theoretical values
* Error percentage calculated (if applicable)

---

# ✅ CONCLUSION

* The forward kinematics model was successfully derived and implemented
* The robotic arm performed the required motions accurately
* MATLAB and Arduino integration was achieved
* The system successfully executed a pick-and-place task

---

Laboratory 2 - Prelims successfully completed.
Group work submitted on March 01, 2026.

Prepared by:
John King Louies R. Solis (Project Leader)
Ian Avenick G. Fornal (Python Programmer)
Stephen Jay G. Caparro (MATLAB Programmer)
Lance Exequiel M. Bonado (Project Engineer)

Thank you to the lecturer and course staff for the guidance and assigned manipulators.
