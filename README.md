## Name: Mukesh.R
## Register Number:23006020
# Experiment 05 Implementation of flipflops using verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
## 1)Create a New Project:
Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

## 2)Create a New Design File:
Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

## 3)Write the Combinational Logic Code:
Open the newly created Verilog or VHDL file and write the code for your combinational logic.

## 4)Compile the Project:
To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

## 5)Analyze and Fix Errors:
If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.

## 6)Verification:
Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
Give the Input Combinations according to the Truth Table and then simulate the Output Waveform

### PROGRAM 
Developed by: Mukesh.R
RegisterNumber: 23006020
## SR-Flipflop:
```
module sr (q,qbar,s,r,clk);
input s,r,clk;
output q,qbar;
wire nand1_out;
wire nand2_out;
nand(nand1_out,clk,s);
nand(nand2_out,clk,r);
nand(q,nand1_out,qbar);
nand(qbar,nand2_out,q);
endmodule
```
## JK-Flipflop:
```
module jk(q,qbar,k,j,clk);
input j,k,clk;
output q,qbar;
wire nand1_out;
wire nand2_out;
nand(nand1_out,j,clk,qbar);
nand(nand2_out,k,clk,q);
nand(q,nand1_out,qbar,qbar);
nand(qbar,nand2_out,q);
endmodule
```
## D-Flipflop:
```
module d(q,qbar,d1,clk);
input d1,clk;
output q,qbar;
wire n1;
wire n2;
not(x,d1);
nand(n1,clk,d1);
nand(n2,clk,x);
nand(q,n2,qbar);
nand(qbar,n1,q);
endmodule 
```
## T-Flipflop:
```
module tff(t,qbar,q,clk);
input t,clk;
output q,qbar;
wire n1,n2;
nand(n1,t,clk,qbar);
nand(n2,clk,t,q);
nand(q,n1,qbar);
nand(qbar,n2,q);
endmodule
```
### RTL LOGIC FOR FLIPFLOPS 
## SR-Flip Flop
![293587518-78eefde6-e72d-4102-ae55-ff620978e875](https://github.com/2005Mukesh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138849308/e5c4ea7e-bc84-49e9-9634-3169ec794d5c)
## D-Flip Flop
![293587544-7bd2a01d-d1e5-4024-ae2d-06fb901401f4](https://github.com/2005Mukesh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138849308/d68c8c95-066a-439b-b271-4f28abed7420)
## JK Flip-Flop
![293587550-32e84985-ed11-4e7d-ba3f-d1574ba78f81](https://github.com/2005Mukesh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138849308/9f07d585-0a83-4a13-8135-75e041693538)
## T-Flip Flop
![293587560-d07cc8a8-4dc6-44b1-86e9-159bfffc6a44](https://github.com/2005Mukesh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138849308/fda6c9d0-0305-4608-9e3d-b73333cd757d)

### TIMING DIGRAMS FOR FLIP FLOPS 
## SR-Flipflop:
![Screenshot 2023-12-18 153335](https://github.com/2005Mukesh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138849308/6f3a0f3e-743d-4b40-b0a5-16012abe3254)
## JK-Flipflop:
![Screenshot 2023-12-18 153409](https://github.com/2005Mukesh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138849308/83daf3d5-ac7c-4d61-9453-8459b9e51660)
## D-Flipflop:
![Screenshot 2023-12-18 153614](https://github.com/2005Mukesh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138849308/eec7db4b-e9c8-4fa9-b44e-832e534c87f1)
## T-Flipflop:
![Screenshot 2023-12-18 153656](https://github.com/2005Mukesh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138849308/df50dbed-3925-421d-986c-906b159dec2e)
### RESULTS:
Thus implementation of SR,JK,D and T flipflops using nand gates are done sucessfully
