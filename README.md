### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY:**

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

**PROCEDURE:**


1.Type the program in Quartus software.

2.compile and run the program.

3.generate RTL schematic and save the logic diagram.

4.Create node for input and output to generate timing diagram.

5.For different input combinations generate the timing diagram.


**PROGRAM:**

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


**TRUTH TABLE:**

![WhatsApp Image 2024-12-20 at 1 54 25 PM](https://github.com/user-attachments/assets/be75dfc3-8415-4c30-a9bc-3258609ee1d1)

**RTL LOGIC UP COUNTER:**

![Screenshot 2024-12-27 173637](https://github.com/user-attachments/assets/d82c9447-366f-4e62-83fb-1da85f668257)


**TIMING DIAGRAM FOR IP COUNTER:**

![image](https://github.com/user-attachments/assets/aff9423f-82b2-49ca-9423-48f6f40ff73e)


**RESULT:**

Thus 4 bit synchronous up counter is implemented using verilog and their fuctionally using their functional table is validated.

DEVELOPED BY: K DHANUSRI POOJA

REGISTER NO: 24011393
