### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**


1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**PROGRAM**
```
module ex11(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule
```


**RTL LOGIC UP COUNTER**


**SYNCHRONOUS-UP-COUNTER:**
<img width="1600" height="863" alt="image" src="https://github.com/user-attachments/assets/abede820-8306-4e51-bb76-057061a31d5f" />
**SYNCHRONOUS-DOWN-COUNTER:**
<img width="1638" height="857" alt="image" src="https://github.com/user-attachments/assets/882fedc6-55dd-4bfc-9e7a-f3caf67cd48f" />


**TIMING DIAGRAM FOR IP COUNTER**



**SYNCHRONOUS-UP-COUNTER:**
<img width="1918" height="167" alt="image" src="https://github.com/user-attachments/assets/3008e2c4-8fa1-42e0-b5f5-01fee804cd84" />
**SYNCHRONOUS-DOWN-COUNTER:**
<img width="1919" height="174" alt="image" src="https://github.com/user-attachments/assets/e3a34851-804b-4049-acd3-775377a680ad" />



**TRUTH TABLE**



![WhatsApp Image 2025-12-10 at 11 23 17_e4c478a0](https://github.com/user-attachments/assets/d256a7ed-612a-4302-b28d-15ddd7daa2a7)

**RESULTS**

Thus implementation of 4 bit synchronous up counter and validate functionality was completed successfully
