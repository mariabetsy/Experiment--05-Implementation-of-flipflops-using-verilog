# Experiment--05-Implementation-of-flipflops-using-verilog
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
~~~
1.using nand gates and wires construct SR flip flop
2.Repeat same steps to construct JK,D,T,flipflop
3.Find Rtl logic and timing diagram for all flipflop 
4.end the prorgam

~~~

### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: mariabetsy
RegisterNumber: 22008543 
*/
~~~
module flipflop(S,R,clock,Q,Qbar);
input S,R,clock;
output Q,Qbar;
wire X,Y;
nand(X,S,clock);
nand(Y,R,clock);
nand(Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule


module df(D,clock,Q,Qbar);
input D,clock;
output Q,Qbar;
assign Dbar = ~D;
wire X,Y;
nand(X,D,clock);
nand(Y,Dbar,clock);
nand(Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule

module JKf(J,K,clock,Q,Qbar);
input J,K,clock;
output Q,Qbar;
wire P,S;
nand(P,J,clock,Qbar);
nand(S,K,clock,Q);
nand(Q,P,Qbar);
nand(Qbar,S,Q);
endmodule

module Tf(T,clock,Q,Qbar);
input T,clock;
output Q,Qbar;
wire A,B;
nand(A,T,clock,Qbar);
nand(B,T,clock,Q);
nand(Q,A,Qbar);
nand(Qbar,B,Q);
endmodule
~~~



### RTL LOGIC FOR FLIPFLOPS 

![214130311-bc328f29-a4c9-4036-8067-1aad515d1b9c](https://user-images.githubusercontent.com/122356434/215348807-371e06da-4ca8-45ca-a42b-17b3ca6a3912.png)


![214201255-7f828efa-066a-4b18-bc25-d11503a136b0](https://user-images.githubusercontent.com/122356434/215348826-0a406bb9-829b-4654-857b-41f027cbfc15.png)
![214204073-5247![214206373-b73a52a1-e7af-47c4-ab7b-b62c3981d6db](https://user-images.githubusercontent.com/122356434/215348855-58796c09-3767-46ae-ad11-54fe6c79ae14.png)
fdf6-7451-49c1-8fd4-514cf485bb75](https://user-images.githubusercontent.com/122356434/215348845-5c32947f-db1e-488e-af73-37fb7349bc58.png)

##TRUTH TABLE

![214209625-c67acfd7-9609-4833-a9a8-80c0a536cff2](https://user-images.githubusercontent.com/122356434/215349092-aa6637d4-8180-4fa9-a275-3db66804a796.png)

![214209642-27f374d4-df64-4f3a-abc9-5e6a8fa7a53b](https://user-images.githubusercontent.com/122356434/215349112-faf22808-5f55-4505-8001-c7a2bd86d15b.png)

![214208533-968c7221-31e3-437a-b2df-d10a926a6bb5](https://user-images.githubusercontent.com/122356434/215349132-eb0bfd1c-38d9-4886-8c56-ae1cc6f5c2ff.png)

![214208666-bd89c8c0-604b-465e-9d4a-f5555e77c88a](https://user-images.githubusercontent.com/122356434/215349160-1f02b5ca-177f-4b04-bea5-509295469d2b.png)
IGRAMS FOR FLIP FLOPS 
  
##TIMING DIAGRAM
 

![214130146-8a965a31-3f59-454f-aa4e-1489195d504c](https://user-images.githubusercontent.com/122356434/215349203-de2aade2-29d6-452c-95a4-78f23fd91807.png)

![214201346-4018bd5e-da03-45c3-87d2-dec11fc6645e](https://user-images.githubusercontent.com/122356434/215349233-0964902a-2551-4f5d-800c-2f89570a9acf.png)

  
![214204185-b2a73e50-71af-4402-9c9f-7f87e2120dc5](https://user-images.githubusercontent.com/122356434/215349266-0da17754-c9f7-4493-8869-e53ddd11c4d3.png)

 
![214206444-d06eb3b8-a790-4034-a8c7-7df8049e3805](https://user-images.githubusercontent.com/122356434/215349273-6950d439-e0e0-4cc8-981a-8ee6148acf07.png)

### RESULTS 



The program for designing book cover page using html and css is executed successfully
