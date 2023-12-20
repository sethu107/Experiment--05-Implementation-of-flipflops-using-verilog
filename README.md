# Name: AMALJOSH MAADHAV J
# Roll No: 23014023
# Experiment 03: Implementation of flipflops using verilog
# Aim
To implement all the flipflops(SR, JK ,D & T) using verilog and validating their functionality using their functional tables
# Equipments Required
Hardware – PC, Cyclone II , USB flasher

Software - Quartus prime
# THEORY 
### SR Flip-Flop

SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/2c4e4a44-1a1a-492a-9460-7100e31d5b71)


This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/b6684635-0d86-44de-bb87-b2865627cf3a)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/3fc4c563-21d5-4138-a91b-339d452c3c08)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/9309e16b-d9b9-4833-980e-5253a3d5d7d7)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop. 
![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/6c1e6d10-abe1-40b3-a118-ad0f2d5d3f1a)


![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/82aaf589-6919-4645-aaeb-464c27fd3691)


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/22a9dfd2-a140-4228-8934-4685ad9c8561)


Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure. 
![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/30732544-2b51-4596-aaf8-793481e7d20b)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/4e567245-d1eb-4148-aed8-7157c6145bb9)



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/b5bf27fc-26fd-49b0-9e27-bb0da474632f)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/fe08452d-fb2f-4ba4-b2d2-338c4cdaf872)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/9c69e182-433c-4840-a5cc-7d818a2afda6)


This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/76647993-02e8-4e8a-b78e-36d2cf0a9c26)


From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)



# Procedure
1. Using nand gates and wires construct SR flip flop.

2. Repeat same steps to construct JK,D,T flipflops.

3. Find RTL logic and timing diagram for all flipflops.



# PROGRAM 
### SR Flipflop
module sr(S,R,clk,Q,Qbar);

input S,R,clk;

output reg Q;

output reg Qbar;

initial Q=0;

 
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


output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=(J&(~Q))|((~K)&Q);

Qbar=((~J)&(Qbar))|K&(~Qbar);

 
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
![Exp 5 SR Truth Table](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/771f430e-4ba4-4b6a-912b-e00541e41f1a)

### JK Flipflop
![Exp 5 JK Truth Table](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/6be872b8-0218-4c01-82ea-7cdec0a513cc)

### D Flipflop
![Exp 5 D Truth Table](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/b1595f18-c7cf-4987-a99c-62652a454ea6)

### T Flipflop
![Exp 5 T Truth Table](https://github.com/amal-2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/148410730/91e57102-9975-4c48-9a97-2d693d99e6bc)

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
