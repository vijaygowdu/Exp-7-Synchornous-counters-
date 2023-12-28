# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY:

## UP COUNTER: 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure:

1.Create a new project in QuartusII software. 2.Name the project as uc for upcounter and dc for
down counter. 3.Create a new verilog hdl file in the project file. 4.Name the module as dc and uc for
down counter and up counter. 5.Within the module declare input and output variables. 6.Create a
loop using if-else with condition parameter as reset value. 7.End the loop. 8.End the module.

### PROGRAM:

Developed by: k Vijay

RegisterNumber: 23004034

### Code:
### UP Counter:

![UPCOUNTER CODE](https://github.com/vijaygowdu/Exp-7-Synchornous-counters-/assets/147473788/5c712808-247c-4e68-998c-6dbae4859304)

### Down Counter:

![DOWNCOUNTER CODE](https://github.com/vijaygowdu/Exp-7-Synchornous-counters-/assets/147473788/6d19b64d-87b5-4042-a087-7e9f84e1ee73)

### RTL LOGIC UP COUNTER AND DOWN COUNTER:
### UP Counter:

![UPCOUNTER RTL](https://github.com/vijaygowdu/Exp-7-Synchornous-counters-/assets/147473788/89f48fe2-15a0-4c57-b2e5-d4312f3a1494)

### Down Counter:

![DOWNCOUNTER RTL](https://github.com/vijaygowdu/Exp-7-Synchornous-counters-/assets/147473788/0e3ac728-0cdf-45f8-b1ab-60a2fe02a0fa)

### TIMING DIGRAMS FOR COUNTER:
### UP COunter:

![UP TIME](https://github.com/vijaygowdu/Exp-7-Synchornous-counters-/assets/147473788/61238d78-6789-455e-8ba3-724acf59914e)

### Down Counter:

![THE REAL DOWN TIME](https://github.com/vijaygowdu/Exp-7-Synchornous-counters-/assets/147473788/e1fbd024-e72f-4d0f-92c4-de0df5c69c60)

### TRUTH TABLE:
### UP Counter:

![UP TT TABLE](https://github.com/vijaygowdu/Exp-7-Synchornous-counters-/assets/147473788/02dfef29-e524-4930-aa12-701001a67747)

### Down Counter:

![DOWN TT](https://github.com/vijaygowdu/Exp-7-Synchornous-counters-/assets/147473788/b65ca087-8671-4f2f-b20c-e6ffd2cce365)

### RESULTS :
Thus Synchornous counters up counter and down counter circuit are studied and the truth table for
different logic gates are verified.
