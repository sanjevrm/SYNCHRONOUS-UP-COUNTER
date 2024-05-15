### SYNCHRONOUS-UP-COUNTER
To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/sanjevrm/SYNCHRONOUS-UP-COUNTER/assets/155142423/5bdb70e2-2968-4930-9248-3eb2d9babb4f)



![image](https://github.com/sanjevrm/SYNCHRONOUS-UP-COUNTER/assets/155142423/9af317b5-2315-4383-adfe-a018c8e364e1)


Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.


**PROGRAM**
```
Developed by : Sanjev R M
Register no: 212223040186
```
![image](https://github.com/sanjevrm/SYNCHRONOUS-UP-COUNTER/assets/155142423/1369fc1b-6419-4dc9-9320-2f5dc86c519f)




**RTL LOGIC UP COUNTER**
![image](https://github.com/sanjevrm/SYNCHRONOUS-UP-COUNTER/assets/155142423/4a2c1a21-3853-4739-9a19-c38d5f473b31)




**TIMING DIAGRAM FOR IP COUNTER**
![image](https://github.com/sanjevrm/SYNCHRONOUS-UP-COUNTER/assets/155142423/6c9e05ea-b68c-4ea2-b581-6397d3dbd3f4)




**TRUTH TABLE**
![image](https://github.com/sanjevrm/SYNCHRONOUS-UP-COUNTER/assets/155142423/08b3ac4e-c443-433e-b0c3-22751d96b901)





**RESULTS**  
Hence a 4 bit synchronous up counter is implemented correctly


