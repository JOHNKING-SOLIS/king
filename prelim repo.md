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

| Step | Task | Description / Notes |
|------|------|-------------------|
| 1 | Assign D-H frames | Apply the 4 standard D-H rules sequentially from base to end-effector. |
| 2 | Build D-H parametric table | Fill θ, d, a, α for each link based on frame assignments and diagram. |
| 3 | Derive transformation matrices | Substitute table values into standard D-H matrix formula. Create one matrix per link (H0_1, H1_2, …). Capture screenshots of matrices or grouped matrices. |
| 4 | Compute overall transformation | Chain multiply: H0_n = H0_1 × H1_2 × … × H(n-1)_n. Document multiplication sequence. |
| 5 | Python implementation (NumPy) | Input a_i lengths and joint variables (T1, T2, d3, …). Convert angles to radians. Build PT list [theta, alpha, a/r, d]. Manually code 4×4 matrices using cos/sin. Convert to np.array. Print individual matrices. Chain multiply with np.dot and print final H0_n (rounded to 3 decimals). |
| 6 | MATLAB implementation (Robotics Toolbox) | Hard-code example link lengths. Define each Link([θ, d, a, α, offset]). Set qlim and sigma=1 for prismatic joints. Build SerialLink. Plot home pose and use `.teach`. Capture visualization screenshot. |
| 7 | Verification – 5 test configurations | Select 5 joint sets (zero + varied values). Run both Python and MATLAB for each. Capture Python output and MATLAB visualization. Arrange side-by-side comparison images. |
| 8 | Documentation structure | Manipulator title → diagrams → D-H table screenshot → transformation matrix screenshots → MATLAB visualization → Python code/output → 5 comparison pairs. |
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

# 🔹 Kinematic Diagram
**Spartan Robokit**

<div align="center">
  <img 
    src="https://github.com/user-attachments/assets/ba12c657-b86f-464b-8d34-1b6a9aad9962" 
    alt="Kinematic Diagram of Spartan Robokit" 
    width="85%"
  />
  <br><br>
  <strong>Figure 1:</strong> Labeled diagram of the Spartan Robokit showing joints, links, coordinate frames, and directions of motion.
</div>

---

## 1. Denavit-Hartenberg (D-H) Notations

### Step 1: Assign Frames according to the 4 D-H Rules

<div align="center">
  <img 
    width="720" 
    alt="D-H Frame Assignment" 
    src="https://github.com/user-attachments/assets/988fa7ec-a493-47ce-9291-9af096c51736"
  />
  <br><br>
  <strong>Figure 2:</strong> Coordinate frame assignment according to D-H rules.
</div>

### Step 2: D-H Parametric Table

<div align="center">
  <img 
    width="620" 
    alt="D-H Parametric Table" 
    src="https://github.com/user-attachments/assets/ff805339-6796-4b12-8e46-b554170514da"
  />
  <br><br>
  <em>Table 1. D-H parameters for the Spartan Robokit</em>
</div>

### Step 3: Homogeneous Transformation Matrices

**Using the standard D-H transformation matrix:**

<div align="center">
  <table border="0" cellspacing="30">
    <tr>
      <td align="center" valign="top">
        <img 
          width="480" 
          alt="Homogeneous Transformation Matrix 1" 
          src="https://github.com/user-attachments/assets/dbd099bf-6088-4cdc-a434-06dada222f8b"
        />
        <br><br>
      </td>
      <td align="center" valign="top">
        <img 
          width="480" 
          alt="Homogeneous Transformation Matrix 2" 
          src="https://github.com/user-attachments/assets/c23da29d-5410-44cd-84e2-78a5df3763fb"
        />
        <br><br>
      </td>
    </tr>
  </table>
</div>

<p align="center">
  <strong>Figure 3 & 4:</strong> Individual homogeneous transformation matrices derived from the D-H table
</p>


# 🧪 TESTING & RESULTS

---

## 🎥 MOTION VALIDATION (5 MOVEMENTS)

### 🔹 Individual Movement Demonstrations

Each movement corresponds to a unique set of joint variables.

<div align="center">
  

https://github.com/user-attachments/assets/0432ee4f-c256-45a3-895f-474847ae9314


  <strong>Figure 5:</strong> Demonstration of the five individual movements of the Spartan Robokit.
</div>

---

## 🎯 PICK-AND-PLACE DEMONSTRATION

### 🔹 Task Description

The robotic manipulator performs a pick-and-place operation using only forward kinematics calculations. The robot moves from an initial position, picks up an object, and transfers it to a target location.

### 🔹 Pick-and-Place Video

<div align="center">


https://github.com/user-attachments/assets/cc20b1a9-07cc-46e8-8848-5f5c982e2f56


  <strong>Figure 6:</strong> Pick-and-Place task demonstration using forward kinematics.
</div>


---


## 🔹 Sequence of Operation

The pick-and-place task is executed through the following 9 sequential steps:

<div align="center">


<table>
  <tr>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/050be1c1-8f8b-4c8c-b01b-392d2d34da0a" width="100%" alt="Step 1"></td>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/f4d1b332-f270-4c05-93e8-5ca0197722ea" width="100%" alt="Step 2"></td>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/5510bea2-be52-44f2-a701-c7a8ab2ee225" width="100%" alt="Step 3"></td>
  </tr>
  <tr>
    <td align="center"><strong>1. Initial Position</strong></td>
    <td align="center"><strong>2. Opening the Gripper</strong></td>
    <td align="center"><strong>3. Positioning Toward the Object</strong></td>
  </tr>
  
  <tr>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/91167759-68a5-4da0-b940-eacac249ec41" width="100%" alt="Step 4"></td>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/0b26f10b-5c60-4bb0-82e8-c8d7a9e339a7" width="100%" alt="Step 5"></td>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/a1746344-743d-4d51-b62d-8f52e377355a" width="100%" alt="Step 6"></td>
  </tr>
  <tr>
    <td align="center"><strong>4. Grasping the Object</strong></td>
    <td align="center"><strong>5. Lifting the Object</strong></td>
    <td align="center"><strong>6. Moving to Target Location</strong></td>
  </tr>

  <tr>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/545dc3d6-5e62-4803-bc1a-462c93bac438" width="100%" alt="Step 7"></td>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/00933440-e9bc-4835-9361-9cc3c58f6fc9" width="100%" alt="Step 8"></td>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/4d5f5bcc-bbca-42de-8926-a7224a34b81b" width="100%" alt="Step 9"></td>
  </tr>
  <tr>
    <td align="center"><strong>7. Lowering to Target Position</strong></td>
    <td align="center"><strong>8. Releasing the Object</strong></td>
    <td align="center"><strong>9. Returning to Initial Position</strong></td>
  </tr>
</table>
Figure 7: Sequence of Operation for Pick-and-Place Task
</div>

### Detailed Steps

| Step | Action | Description |
|------|--------|------------|
| 1 | Initial Position | The robotic arm starts in its home configuration with θ₁ = 0°, θ₂ = 0°, θ₃ = 0°, and the gripper closed. This ensures a consistent reference and repeatability. |
| 2 | Opening the Gripper | The gripper opens to 45° while all joint angles remain unchanged, preparing the end-effector to grasp the object. |
| 3 | Positioning Toward the Object | θ₂ is adjusted to 70° while θ₁ and θ₃ remain at 0°, lowering the arm to align with the object. |
| 4 | Grasping the Object | The gripper closes to 0°, securing the object while maintaining the arm’s position for accurate alignment. |
| 5 | Lifting the Object | θ₂ returns to 0°, lifting the object to a safe height to avoid collisions during movement. |
| 6 | Moving to Target Location | θ₁ rotates to 60°, moving the arm horizontally toward the target location. |
| 7 | Lowering to Target Position | θ₂ is adjusted to 70° to lower the object precisely onto the target surface. |
| 8 | Releasing the Object | The gripper opens to 45°, releasing the object at the target location. |
| 9 | Returning to Initial Position | All joints return to 0° and the gripper closes, resetting the system for the next cycle. |
---

# 💻  CODES

## 🔹 MATLAB Code


function varargout = ROBOT(varargin)
% ROBOT MATLAB code for ROBOT.fig
%      ROBOT, by itself, creates a new ROBOT or raises the existing
%      singleton*.
%
%      H = ROBOT returns the handle to a new ROBOT or the handle to
%      the existing singleton*.
%
%      ROBOT('CALLBACK',hObject,eventData,handles,...) calls the local
%      function named CALLBACK in ROBOT.M with the given input arguments.
%
%      ROBOT('Property','Value',...) creates a new ROBOT or raises the
%      existing singleton*. Starting from the left, property value pairs are
%      applied to the GUI before ROBOT_OpeningFcn gets called. An
%      unrecognized property name or invalid value makes property application
%      stop. All inputs are passed to ROBOT_OpeningFcn via varargin.
%
%      *See GUI Options on GUIDE's Tools menu. Choose "GUI allows only one
%      instance to run (singleton)".
%
% See also: GUIDE, GUIDATA, GUIHANDLES

% Last Modified by GUIDE v2.5 12-Jul-2025 19:56:07

% Begin initialization code - DO NOT EDIT
gui_Singleton = 1;
gui_State = struct('gui_Name',       mfilename, ...
                   'gui_Singleton',  gui_Singleton, ...
                   'gui_OpeningFcn', @ROBOT_OpeningFcn, ...
                   'gui_OutputFcn',  @ROBOT_OutputFcn, ...
                   'gui_LayoutFcn',  [] , ...
                   'gui_Callback',   []);
if nargin && ischar(varargin{1})
    gui_State.gui_Callback = str2func(varargin{1});
end

if nargout
    [varargout{1:nargout}] = gui_mainfcn(gui_State, varargin{:});
else
    gui_mainfcn(gui_State, varargin{:});
end
% End initialization code - DO NOT EDIT


% --- Executes just before ROBOT is made visible.
function ROBOT_OpeningFcn(hObject, eventdata, handles, varargin)
% This function has no output args, see OutputFcn.
% hObject    handle to figure
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
% varargin   command line arguments to ROBOT (see VARARGIN)

% Choose default command line output for ROBOT
handles.output = hObject;

% Initialize Robotics Toolbox
startup_rvc

% Initialize global variables
global robot q_prev serial_connected;
q_prev = [0 0 0];
serial_connected = false;

% Robot parameters
syms a1 a2 a3

%% Link lengths (in mm or cm - be consistent)
a1 = 36;  % Base height
a2 = 72;  % Upper arm length
a3 = 72;  % Forearm length

%% D-H Parameters [theta, d, r, alpha, offset]
H0_1 = Link([0, a1, 0, pi/2, 0, 0]);      % Base to shoulder
H1_2 = Link([0, 0, a2, 0, 0, deg2rad(90)]); % Shoulder to elbow
H2_3 = Link([0, 0, a3, 0, 0, deg2rad(270)]); % Elbow to wrist

% Create robot model
robot = SerialLink([H0_1 H1_2 H2_3], 'name', '3-DOF Robot');

% Initial plot with neutral position0
initial_q = [0 0 0];
robot.plot(initial_q, 'workspace', [-160 160 -160 160 0 200]);

% Calculate initial end-effector position
T = robot.fkine(initial_q);
position = T.t;

% Display initial position
disp('Initial End-effector Position [x y z]:');
disp(position');

% Update position display
set(handles.edit8, 'String', num2str(position(1), '%.2f'));  % X
set(handles.edit9, 'String', num2str(position(2), '%.2f'));  % Y
set(handles.edit10, 'String', num2str(position(3), '%.2f')); % Z

% Initialize servo values in handles
handles.servo1 = 0;
handles.servo2 = 0;
handles.servo3 = 0;
handles.servo4 = 0;
handles.serial_connected = false;
handles.serial_port = [];

% Set default values in edit boxes
set(handles.edit1, 'String', '0');
set(handles.edit2, 'String', '0');
set(handles.edit3, 'String', '0');
set(handles.edit11, 'String', '0');

% Try to connect to Arduino/ESP32
try
    % CHANGE THIS TO YOUR ACTUAL COM PORT
    % On Windows: "COM3", "COM4", etc.
    % On Linux: "/dev/ttyUSB0", "/dev/ttyACM0"
    % On Mac: "/dev/cu.usbserial-XXX"
    s = serialport("COM5", 115200);  % <-- CHANGE THIS PORT
    
    % Test connection by sending initial zeros
    cmd = sprintf("SERVO %d %d %d %d", 0, 0, 0, 0);
    writeline(s, cmd);
    disp("Arduino/ESP32 Connected successfully!");
    disp("Sent initial command: " + cmd);
    
    % Store serial connection
    handles.serial_port = s;
    handles.serial_connected = true;
    serial_connected = true;
    
    % Update status (if you have a status text field)
    % set(handles.status_text, 'String', 'Connected to Arduino');
    
catch ME
    % Connection failed
    disp('Arduino/ESP32 NOT detected. Running in simulation mode only.');
    disp(['Error: ' ME.message]);
    handles.serial_connected = false;
    serial_connected = false;
    % set(handles.status_text, 'String', 'Simulation Mode - No Hardware');
end

% Update handles structure
guidata(hObject, handles);

% UIWAIT makes ROBOT wait for user response (see UIRESUME)
% uiwait(handles.figure1);


% --- Outputs from this function are returned to the command line.
function varargout = ROBOT_OutputFcn(hObject, eventdata, handles)
% varargout  cell array for returning output args (see VARARGOUT);
% hObject    handle to figure
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Get default command line output from handles structure
varargout{1} = handles.output;


% --- Servo 1 Edit Box Callback ---
function edit1_Callback(hObject, eventdata, handles)
% hObject    handle to edit1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Get and validate servo 1 value
servo1_value = str2double(get(hObject, 'String'));

% Validate input
if isnan(servo1_value)
    % Not a number
    set(hObject, 'String', '0');
    servo1_value = 0;
    uiwait(errordlg('Please enter a valid number for Servo 1', 'Input Error'));
elseif servo1_value < 0 || servo1_value > 180
    % Out of range
    set(hObject, 'String', '90');
    servo1_value = 90;
    uiwait(warndlg('Servo 1 angle must be between 0 and 180 degrees', 'Range Error'));
end

% Store in handles
handles.servo1 = servo1_value;
disp(['Servo 1 set to: ' num2str(servo1_value) ' degrees']);

% Save handles
guidata(hObject, handles);


% --- Executes during object creation, after setting all properties.
function edit1_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Set default value
set(hObject, 'String', '0');

% Hint: edit controls usually have a white background on Windows.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Servo 2 Edit Box Callback ---
function edit2_Callback(hObject, eventdata, handles)
% hObject    handle to edit2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Get and validate servo 2 value
servo2_value = str2double(get(hObject, 'String'));

% Validate input
if isnan(servo2_value)
    set(hObject, 'String', '0');
    servo2_value = 0;
    uiwait(errordlg('Please enter a valid number for Servo 2', 'Input Error'));
elseif servo2_value < 0 || servo2_value > 100
    set(hObject, 'String', '90');
    servo2_value = 90;
    uiwait(warndlg('Servo 2 angle must be between 0 and 100 degrees', 'Range Error'));
end

% Store in handles
handles.servo2 = servo2_value;
disp(['Servo 2 set to: ' num2str(servo2_value) ' degrees']);

% Save handles
guidata(hObject, handles);


% --- Executes during object creation, after setting all properties.
function edit2_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Set default value
set(hObject, 'String', '0');

if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Servo 3 Edit Box Callback ---
function edit3_Callback(hObject, eventdata, handles)
% hObject    handle to edit3 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Get and validate servo 3 value
servo3_value = str2double(get(hObject, 'String'));

% Validate input
if isnan(servo3_value)
    set(hObject, 'String', '0');
    servo3_value = 0;
    uiwait(errordlg('Please enter a valid number for Servo 3', 'Input Error'));
elseif servo3_value < 0 || servo3_value > 120
    set(hObject, 'String', '90');
    servo3_value = 90;
    uiwait(warndlg('Servo 3 angle must be between 0 and 120 degrees', 'Range Error'));
end

% Store in handles
handles.servo3 = servo3_value;
disp(['Servo 3 set to: ' num2str(servo3_value) ' degrees']);

% Save handles
guidata(hObject, handles);


% --- Executes during object creation, after setting all properties.
function edit3_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit3 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Set default value
set(hObject, 'String', '0');

if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Gripper Edit Box Callback ---
function edit11_Callback(hObject, eventdata, handles)
% hObject    handle to edit11 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Get and validate gripper value (0 = open, 180 = closed typically)
gripper_value = str2double(get(hObject, 'String'));

% Validate input
if isnan(gripper_value)
    set(hObject, 'String', '0');
    gripper_value = 0;
    uiwait(errordlg('Please enter a valid number for Gripper', 'Input Error'));
elseif gripper_value < 0 || gripper_value > 180
    set(hObject, 'String', '0');
    gripper_value = 0;
    uiwait(warndlg('Gripper value must be between 0 and 180', 'Range Error'));
end

% Store in handles
handles.servo4 = gripper_value;
disp(['Gripper set to: ' num2str(gripper_value)]);

% Save handles
guidata(hObject, handles);




% --- Executes during object creation, after setting all properties.
function edit11_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit11 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Set default value
set(hObject, 'String', '0');

if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Send Button Callback ---
function pushbutton3_Callback(hObject, eventdata, handles)
% hObject    handle to pushbutton3 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

clc;
disp('===================================');
disp('Sending command to robot...');
disp('===================================');

% Initialize Robotics Toolbox if needed
startup_rvc

% Get global variables
global robot q_prev;

if isempty(q_prev)
    q_prev = [0 0 0];
end

% Get servo angles from edit boxes (in degrees)
q1_deg = str2double(get(handles.edit1, 'String'));
q2_deg = str2double(get(handles.edit2, 'String'));
q3_deg = str2double(get(handles.edit3, 'String'));
gripper = str2double(get(handles.edit11, 'String'));

% Validate inputs (ensure they're numbers)
if isnan(q1_deg), q1_deg = 0; set(handles.edit1, 'String', '0'); end
if isnan(q2_deg), q2_deg = 0; set(handles.edit2, 'String', '0'); end
if isnan(q3_deg), q3_deg = 0; set(handles.edit3, 'String', '0'); end
if isnan(gripper), gripper = 0; set(handles.edit11, 'String', '0'); end

% Convert to radians for robotics calculations
q1 = deg2rad(q1_deg);
q2 = deg2rad(q2_deg);
q3 = deg2rad(q3_deg);


% Display values being sent
disp('Command Values:');
disp(['  Servo 1: ' num2str(q1_deg) '°']);
disp(['  Servo 2: ' num2str(q2_deg) '°']);
disp(['  Servo 3: ' num2str(q3_deg) '°']);
disp(['  Gripper: ' num2str(gripper)]);

%% SEND TO ARDUINO/ESP32
if handles.serial_connected && ~isempty(handles.serial_port)
    try
        % Use existing serial connection
        s = handles.serial_port;
        
        % Format command: "SERVO <s1> <s2> <s3> <gripper>"
        cmd = sprintf("SERVO %d %d %d %d", round(q1_deg), round(q2_deg), round(q3_deg), round(gripper));
        
        % Send command
        writeline(s, cmd);
        disp('✓ Command sent to Arduino/ESP32 successfully!');
        
        % Optional: Read response if Arduino sends one
        if s.NumBytesAvailable > 0
            response = readline(s);
            disp(['  Arduino response: ' response]);
        end
        
    catch ME
        % Communication error
        disp('✗ Failed to send command to Arduino!');
        disp(['  Error: ' ME.message]);
        
        % Try to reconnect
        try
            disp('  Attempting to reconnect...');
            delete(handles.serial_port);
            s = serialport("COM5", 115200);  % CHANGE THIS PORT
            handles.serial_port = s;
            handles.serial_connected = true;
            guidata(hObject, handles);
            disp('  Reconnected successfully!');
        catch
            handles.serial_connected = false;
            guidata(hObject, handles);
            disp('  Reconnection failed. Check USB connection.');
        end
    end
else
    disp('⚠ Arduino/ESP32 not connected. Running in simulation mode.');
    disp('  To connect: Check USB and COM port in ROBOT_OpeningFcn');
end

%% ROBOT VISUALIZATION
disp(' ');
disp('Updating 3D visualization...');

% Robot parameters
a1 = 36;  % Base height
a2 = 72;  % Upper arm length
a3 = 72;  % Forearm length

% Define robot links
H0_1 = Link([0, a1, 0, pi/2, 0, 0]);
H1_2 = Link([0, 0, a2, 0, 0, deg2rad(90)]);
H2_3 = Link([0, 0, a3, 0, 0, deg2rad(270)]);

% Joint configuration
q = [q1, -q2, q3];  % Note: negative for q2 based on your kinematics

% Create smooth trajectory from previous position
q_start = q_prev;
nSteps = 15;  % Number of interpolation steps
q_traj = jtraj(q_start, q, nSteps);

% Update robot model
robot = SerialLink([H0_1 H1_2 H2_3], 'name', '3-DOF Robot');

% Animate the movement
for i = 1:nSteps
    robot.animate(q_traj(i, :));
    pause(0.03);  % Small pause for smooth animation
end

% Store current joint angles for next move
q_prev = q;

%% CALCULATE AND DISPLAY END-EFFECTOR POSITION
T = robot.fkine(q);
position = T.t;

disp(' ');
disp('End-effector Position:');
disp(['  X = ' num2str(position(1), '%.2f') ' mm']);
disp(['  Y = ' num2str(position(2), '%.2f') ' mm']);
disp(['  Z = ' num2str(position(3), '%.2f') ' mm']);
disp('===================================');

% Update position displays
set(handles.edit8, 'String', num2str(position(1), '%.2f'));  % X
set(handles.edit9, 'String', num2str(position(2), '%.2f'));  % Y
set(handles.edit10, 'String', num2str(position(3), '%.2f')); % Z

% Save updated handles
guidata(hObject, handles);


% --- X Position Display (Read-only) ---
function edit8_Callback(hObject, eventdata, handles)
% This is typically read-only, so we don't process input

% --- Executes during object creation, after setting all properties.
function edit8_CreateFcn(hObject, eventdata, handles)
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Y Position Display (Read-only) ---
function edit9_Callback(hObject, eventdata, handles)
% This is typically read-only, so we don't process input

% --- Executes during object creation, after setting all properties.
function edit9_CreateFcn(hObject, eventdata, handles)
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Z Position Display (Read-only) ---
function edit10_Callback(hObject, eventdata, handles)
% This is typically read-only, so we don't process input

% --- Executes during object creation, after setting all properties.
function edit10_CreateFcn(hObject, eventdata, handles)
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Optional: Close function to clean up serial connection ---
function figure1_CloseRequestFcn(hObject, eventdata, handles)
% hObject    handle to figure1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Clean up serial connection when GUI closes
if isfield(handles, 'serial_port') && ~isempty(handles.serial_port)
    try
        delete(handles.serial_port);
        disp('Serial connection closed.');
    catch
        % Ignore errors on close
    end
end

% Hint: delete(hObject) closes the figure
delete(hObject);



## 🔹 Arduino Code

--insert arduino code

## 🔹 python Code

--insert python code

---

# 📸 DOCUMENTATION

---

## 🔹 Project Images

<div align="center">
  <img 
    src="https://github.com/user-attachments/assets/71df8c51-c54f-48d6-a467-74f2119bf65b" 
    alt="Project Overview" 
    width="60%"
  />
  <br><br>
  <strong>Figure 8:</strong> Overall view of the Spartan Robokit project setup.
</div>

---

## ⚙️ CALIBRATION

### 🔹 Calibration Procedure

<div align="center">
  <table>
    <tr>
      <td align="center"><img src="https://github.com/user-attachments/assets/c84bfc4f-468a-4b2f-9e64-90775763f3ed" width="48%" alt="Calibration Step 1"></td>
      <td align="center"><img src="https://github.com/user-attachments/assets/d222634a-beda-4908-9458-169b53b2b268" width="48%" alt="Calibration Step 2"></td>
    </tr>
    <tr>
      <td align="center"><img src="https://github.com/user-attachments/assets/a407594d-b038-480b-9c32-7b1efc6cd414" width="48%" alt="Calibration Step 3"></td>
      <td align="center"><img src="https://github.com/user-attachments/assets/8adcd71e-9ac0-43a3-8f92-cead70d372ef" width="48%" alt="Calibration Step 4"></td>
    </tr>
    <tr>
      <td align="center"><img src="https://github.com/user-attachments/assets/07038d0e-6fd2-4581-8dd0-ce53bddf2e66" width="48%" alt="Calibration Step 5"></td>
      <td align="center"><img src="https://github.com/user-attachments/assets/3e850e68-81f5-4772-8597-fdd179474102" width="48%" alt="Calibration Step 6"></td>
    </tr>
  </table>
  <br>
  <strong>Figure 9:</strong> Calibration procedure steps for the Spartan Robokit.
</div>

---

## 🦾 KINEMATIC DERIVATIONS

<div align="center">
  <table>
    <tr>
      <td align="center"><img src="https://github.com/user-attachments/assets/7af59ac1-c3a9-4671-91d9-484f1cb0eb37" width="48%" alt="Kinematic Derivation 1"></td>
      <td align="center"><img src="https://github.com/user-attachments/assets/45f2212f-6382-472e-8fb7-00a4763132cc" width="48%" alt="Kinematic Derivation 2"></td>
    </tr>
  </table>
  <br>
  <strong>Figure 10:</strong> Kinematic derivations and calculations.
</div>

---

## 🧪 TESTING

<div align="center">

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/5762b03c-936b-4566-999d-a67f76016ec3" width="300"><br>
      <sub>Test Procedure 1</sub>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/0f68e1b7-cd65-43d5-ac5d-5a1da8505d5e" width="300"><br>
      <sub>Test Procedure 2</sub>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/2469b724-e8a6-4f68-b3ef-a062560467ff" width="300"><br>
      <sub>Test Procedure 3</sub>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/7a2a7ede-46a0-42e3-87d1-cd86e07f468c" width="300"><br>
      <sub>Test Procedure 4</sub>
    </td>
  </tr>
</table>

<br>
<strong>Figure 11:</strong> Testing procedures and results of the Spartan Robokit.

</div>
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

## Laboratory 2 – Prelims

The Laboratory 2 – Prelims activity was successfully completed.  
The group output was submitted on **March 09, 2026**.

### Prepared by:
- **John King Louies R. Solis** – Project Leader  
- **Ian Avenick G. Fornal** – Python Programmer  
- **Stephen Jay G. Caparro** – MATLAB Programmer  
- **Lance Exequiel M. Bonado** – Project Engineer  

### Acknowledgment
The group would like to express sincere gratitude to the lecturer and course staff for their guidance, support, and for providing the assigned manipulators necessary for completing this laboratory activity.
