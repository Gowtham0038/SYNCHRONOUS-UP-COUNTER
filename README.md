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
Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.
/* write all the steps invloved */

**PROGRAM**
~~~
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
~~~
/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:Gowtham C
RegisterNumber:24002349
*/

**RTL LOGIC UP COUNTER**
![398194330-d73e36ee-167a-42ed-8036-e2535ebae0a1](https://github.com/user-attachments/assets/b4ab0197-8f91-406c-9258-b4709d2d523b)

**TIMING DIAGRAM FOR IP COUNTER**
![398194387-ff79f97f-10b2-4d97-a3d3-1773a837bece](https://github.com/user-attachments/assets/f2058438-9df3-44b0-851c-be6f3100ad89)

**TRUTH TABLE**
![398194736-e471674d-a684-466b-b2f2-1003a7c18f9a](https://github.com/user-attachments/assets/f44c9abf-2b2a-4272-8d3a-30cc4e4ef550)

**RESULTS**
Thus to implement 4 bit synchronous up counter and validate functionality done successfully.
