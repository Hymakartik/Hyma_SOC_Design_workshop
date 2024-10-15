# **Hyma PD Workshop** 
 <details>
<summary> DAY 0 : TOOL INSTALLATION </summary>

###  **1.) YOSYS** 
```
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make (If make is not installed please install it) 
sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make 
sudo make install
```
![image](https://github.com/user-attachments/assets/d25e8607-dcc4-49e8-bbc4-b2d887147fd2)

```
```
###  **2.) IVERILOG**
```
Steps to install iverilog
sudo apt-get update
sudo apt-get install iverilog

```
![image](https://github.com/user-attachments/assets/92cd5170-b377-4799-b83a-c75a494af934)
```
```
###  **1.) GTKWAVE**
```

gtkwave
Steps to install gtkwave
sudo apt-get update
sudo apt install gtkwave
```
![image](https://github.com/user-attachments/assets/697bbfdc-fa03-45af-93bd-b1ab8f071152)
```
```
</details>
<details>
<summary> DAY 1 : INTRODUCTION TO IVERILOG </summary>

###  **1.) GTKWAVE OUTPUT FOR GOOD_MUX**
``` ```
<img width="1018" alt="Screenshot 2024-10-01 at 11 25 37 PM" src="https://github.com/user-attachments/assets/86944671-0ac3-4ba0-a6e1-371ea5a85fa3">
```
```
###  **2.) GOOD_MUX Design and Testbench**
``` ```
<img width="1011" alt="Screenshot 2024-10-01 at 11 51 04 PM" src="https://github.com/user-attachments/assets/6b1c174e-2347-45ac-a50b-ebaedf97573e">
```
```
</details>
<details>
<summary> DAY 2 : Timing libs, hierarchical vs flat synthesis and efficient flop coding styles
 </summary>

###  **1.) INTRODUCTION TO timing.libs**
``` 
```
<img width="1063" alt="Screenshot d2a" src="https://github.com/user-attachments/assets/d92ab3e1-1be6-40e9-ae59-98f9c2934d81">

Every library is defined PVT (Process, Voltage & Temperature)
In above lib, tt stands for typical (process), 025c stands temperature and 1v80 stands for voltage
In timing library, each and every cell contains below information
- Power Lookup table
- Timing Lookup table
- technology
- units of power,voltage,resistance,time,capacitance etc..
- cell footprints (Area & leakage power)
- Pin information and so on

###  **2.) Hierarchical vs Flat synthesis**
``` ```
<img width="1370" alt="Screenshot 2024-10-15 at 11 37 19 PM" src="https://github.com/user-attachments/assets/237a92e4-0a16-4e90-9799-38511904a248">
<img width="568" alt="Screenshot 2024-10-15 at 11 45 44 PM" src="https://github.com/user-attachments/assets/9eb9e246-1b25-4900-ad38-803d54de602a">
<img width="999" alt="Screenshot 2024-10-15 at 11 45 59 PM" src="https://github.com/user-attachments/assets/dde8b035-f8da-4f53-a368-5a074fac13dc">
<img width="1048" alt="Screenshot 2024-10-15 at 11 50 33 PM" src="https://github.com/user-attachments/assets/387b7c69-a72f-407c-aac3-3b052eb3921b">
<img width="1129" alt="Screenshot 2024-10-15 at 11 55 56 PM" src="https://github.com/user-attachments/assets/4dd1bd84-5ff3-4c6f-8ae7-5c97ca8e80ba">
<img width="771" alt="Screenshot 2024-10-15 at 11 56 13 PM" src="https://github.com/user-attachments/assets/46fd3b31-cfe1-462d-a115-768892fa5e64">
<img width="926" alt="Screenshot 2024-10-15 at 11 59 20 PM" src="https://github.com/user-attachments/assets/0aef5b3e-9d92-4ec3-9b18-148908e070ac">
<img width="713" alt="Screenshot 2024-10-16 at 12 10 08 AM" src="https://github.com/user-attachments/assets/e252e795-7b51-4a52-a685-7750509021ed">
``` ```
- why we do sub module level synthesis?
  - when we have multiple instances of same module
  - When we have massive instances (divide and conquer rule)

###  **2.) Various Flop Coding Styles and optimization**
```
```
<img width="827" alt="Screenshot 2024-10-16 at 12 36 07 AM" src="https://github.com/user-attachments/assets/eb63b154-e07c-4a9d-8fdc-4f9cf063b743">
```
