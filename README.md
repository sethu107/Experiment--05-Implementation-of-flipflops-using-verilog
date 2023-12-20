# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
# Name: AMALJOSH MAADHAV J
# Roll No: 23014023
# Experiment 03: Implementation of flipflops using verilog
# Aim
To implement all the flipflops(SR, JK ,D & T) using verilog and validating their functionality using their functional tables
# Equipments Required
Hardware – PC, Cyclone II , USB flasher

Software - Quartus prime
# THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

@@ -101,40 +106,145 @@ From the above characteristic table, we can directly write the next state equati
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */
# Procedure
1. Using nand gates and wires construct sr flip flop.

2. Repeat same steps to construct JK,D,T flipflops.

3. Find Rtl logic and timing diagram for all flipflops.

### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/
4. End the program.

# PROGRAM 
### SR Flipflop
module sr(S,R,clk,Q,Qbar);

input S,R,clk;

output reg Q;

output reg Qbar;

initial Q=0;

### RTL LOGIC FOR FLIPFLOPS 
initial Qbar=1;

always @(posedge clk)

begin

Q=S|((~R)&Q);

Qbar=R|((~S)&(Qbar));

end

endmodule

### JK Flipflop
module jk(J,K,clk,Q,Qbar);

input J,K,clk;

### TIMING DIGRAMS FOR FLIP FLOPS 
output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=(J&(~Q))|((~K)&Q);

Qbar=((~J)&(Qbar))|K&(~Qbar);

### RESULTS 
end

endmodule

### D Flipflop

module d(d,clk,q,qbar);

input d,clk;

output q,qbar;

reg q,qbar;

always @(posedge clk)

begin 

q=d;

qbar=~q;

end 

endmodule

### T Flipflop
module t(clk,T,q,qbar);

input clk,T;

output q,qbar;

reg q,qbar;

always @(posedge clk)

begin

q=(T&~q)|(~T&q);

qbar=~q;

end 

endmodule

# RTL realisation
### SR Flipflop
![Exp 5 SR RTL](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/add9a607-1ced-45ae-afbf-7146eccc6a49)

### JK Flipflop
![Exp 5 JK RTL](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/f9fd8192-73bf-4227-92df-82c0251908c5)

### D Flipflop
![Exp 5 D RTL](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/c87f452c-f36e-46a8-8062-53f6f1ccc11e)

### T Flipflop
![Exp 5 T RTL](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/797e77f8-2396-4ca7-96ea-c07fbb285d72)



# Truth Table
### SR Flipflop

### JK Flipflop

### D Flipflop

### T Flipflop

# Timing Diagram
### SR Flipflop
![Exp 5 SR Timing Diagram](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/62887fa0-7cde-417b-b61d-221bf1634863)

### JK Flipflop
![Exp 5 JK Timing Diagram](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/c3fc201a-0f64-410d-a6e4-fba519ee9c30)

### D Flipflop
![Exp 5 D Timing Diagram](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/a3c83737-2ca7-451e-9f2a-20b79967ac11)

### T Flipflop
![Exp 5 T Timing Diagram](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/3011e448-af70-48e3-a794-bc1bc36bbe85)

### Result
Thus, the  implementation of SR,JK,D and T flipflops using nand gates are done sucessfully.
