# Embedded-system-foundations
My embedded systems and edge AI learning journey
# Embedded Foundations

My learning journey from digital logic fundamentals to embedded AI and TinyML — i documented as I go,i will also include my mistakes and how i debugged them, courses like digital logic, electronics, computer arichtecture, basic circute, c and c++ and other related courses are base for this journey they are the fundamental or the prerequisites thats why i am starting from this to help me clean the way.

## Why writing this repo
I'm a 2nd-year Electrical and Computer Engineering student , building toward a career in embedded systems and edge AI. This repo is where I track what I study and, what I build, and what I get wrong along the way.

## Progress 

### my Day 1 — Binary & Hexadecimal
- Studied binary and hexadecimal number systems (Neso Academy, youtube)
- Binary is a base-2 system using only 0 and 1, which perfectly reflects how hardware microchips process information using on and off electrical states as we all know on computers and other programmed devices. Hexadecimal means a base-16 system that acts as a shorthand for binary as it has nibbles which is 4 bit or, where one hex digit represents exactly four binary bits. we can use hex because writing out long strings of raw binary (like 10101010) is very tedious and prone to typos, whereas hex like 0xAA keeps the code clean.
- 0xFF=255, 0x0F=15, 0xF0=240, 0xAA=170, 0x55=85, 0x80=128

### my Day 2 — Logic Gates and Full Adders

- i happily Studied the fundamental logic gates used in digital systems, including AND, OR, NOT, XOR, NAND, and NOR. These gates take binary inputs, 0 and 1, and produces outputs according to the specific logical rules. This is really the foundation of how digital circuits process information by binary.

- i Learned about NAND and NOR gates as universal gates. This means that, by combining only NAND gates or only NOR gates in specific ways, we can recreate other logic gates such as NOT, AND, and OR and i practiced it forming the other 6 logic gates using only nand. This also showed me that complex digital systems like chips can be constructed from simpler building blocks.

-i Built a half adder and also Full Adder circuit in Logisim Evolution using two Half Adders and an OR gate. A Full Adder takes three inputs: A, B, and Carry In , and produces two outputs: Sum and Carry-Out.

- The first Half Adder processes A and B. The second Half Adder combines the first result with the Carry-In. The two carry outputs are then it will be combined using an OR gate to produce the Carry-Out.

### my Day 3 — Boolean Algebra, De Morgan's Theorem & Karnaugh Maps

-today i studied Boolean algebra and the fundamental laws used to simplify digital logic, including Identity, Null, Idempotent, Complement, Commutative, Associative, Distributive, and Absorption laws.

-i Studied De Morgan's Theorems and also learned how NOT changes AND into OR and OR into AND while complementing the variables.

-i Learned how the Karnaugh maps can be used to simplify Boolean expressions by grouping adjacent 1s and eliminating variables that change within a valid group and i tested it.

-i also Practiced Boolean simplification using Karnaugh maps and then verified one of my simplifications in Logisim Evolution.

- To verify the result, I built two circuits the one using the ORIGINAL unsimplified Boolean expression and another using the SIMPLIFIED expression obtained from the Karnaugh map.

- I connected the same inputs to both circuits and tested all possible inputs. Both circuits produced identical outputs for every combination, confirming that the simplified expression was logically equivalent to the original expression and that was very satisfying...

- This was an important step for me because I was not only simplifying the expression mathematically but I verified the result physically as a digital circuit. 

- This all helped me understand how simple logic gates can be combined and operate to build arithmetic circuits, its amazing btw. and also By chaining multiple Full Adders together,,, a circuit can perform multibit binary additions, which connects digital logic to the arithmetic hardware.

  ### my Day 4 Sequential Logic, Flip-Flops, Registers & Counters

-i umm learned the difference between combinational and sequential logics. Unlike the combinational circuits I built earlier, sequential circuits have memory, so their behavior depends not only on the current inputs but also on the stored states.

-i studied the D flip-flop and learnes that it stores one bit of data. On the active clock edge, the value on D is captured or stored and appears at Q, while changes on D between clock edges do not immediately change Q but when it comes to latch its a bit different.

-i reviewed SR, JK, and T flip-flops. SR provides Set and Reset, JK improves the SR behavior and can toggle, and T is designed to toggle its stored state when enabled. The D flip-flop is especially useful for storing arbitrary data bits.

-i learned how an SR latch can be built from two crossly coupled NAND gates. The feedback between the gates allows the circuit to maintain a stable state even after the original Set or Reset signal is removed. I then used this idea to construct a D latch from NAND gates, an inverter, and clock gating.

-i learned that a register is a group of flip-flops working together to store multiple bits. For example, an 8-bit register can be built from eight D flip-flops, with each flip-flop storing one bit and it has the same clock all together.

-i connected the idea of a D flip-flop to an MCU register: one D flip-flop stores one bit, while multiple flip-flops form a register that stores an entire multi-bit values. 

-i built and tested a 2bit synchronous counter in Logisim Evolution. The counter cycles through 00 → 01 → 10 → 11 → 00 using two D flip-flops driven by the same clocks and one XOR gate and not gate as the digits depend each other

-i added Enable control so that the counter can either continue counting or hold its current state. Verified that when Enable is disabled, clock edges occur but the stored count does not change and i added a synchronous Reset so that the counter returns to 00 on the next clock edge when Reset is activated, i used multiplexer to do that.


### my Day 5  : 4-bit Counter & Hex Display

- i designed the 16-state sequence for a 4-bit synchronous counter, from 0000 through 1111 and back to 0000.

- i extended my previous 2-bit counter into a 4-bit counter using four D flip-flops with a shared clock. The lower bits determine when the higher bits toggle, reproducing normal binary counting behavior i used xor to identify when the neighbour digits be 1 at the same time and that will change the value.

- i added Enable and synchronous Reset controls. With Enable disabled, the counter holds its current state while the clock continues running with Reset enabled, the counter returns to 0000 on the next clock edges.

- i also studied the seven segments of a hexadecimal display and derived the logic for segment 'a' using a 16row truth table and i simplified it via a 4variable Karnaugh map, wow kmap is the goat. This proves how the binary counter output can be converted into the individual signals needed by the display.

-i connected the 4-bit counter to Logisim Evolutions Hex Digit Display and tested the complete sequence from 0 through F

- verified that Enable freezes the displayed value and that synchronous Reset returns the system to 0 on the next clock edge.

- this brought together the main concepts from my first week: Boolean logic, simplification, memory, flip-flops, sequential state, counters, and decoding and its so satisfying.

-  an MCU timer/counter peripheral uses the same idea of clocked counter state and control logics, but the circuitry is implemented directly inside the microcontroller siliconthan as individual Logisim components.

  ### Day 6  Circuit Analysis & First LTspice Simulations

This day marked my first step from digital logic to basic electrical circuit analysis and SPICE simulations. Instead of only constructing logic circuits, I started calculating voltages and currents before simulating them.

-i also revised Ohm's Law, which relates voltage, current, and resistance:

  V = IR

  I used it as the basic tool for predicting current and voltage in resistive circuits before we open the simulator.

-i studied Kirchhoffs Voltage Law (KVL) the algebraic sum of all voltage changes around a closed loop is zero. This gives a way to track how the source voltage is distributed across the different components in the circuit.

-i studied Kirchhoffs Current Law (KCL) the current entering a node must equal the current leaving it. This is also fundamental for understanding how current behaves when a circuit splits into multiple path.

-i built my first LED circuit in LTspice using a 5 V source, a 470 Ω series resistor, an LED, and ground. Before the simulation, I calculated the expected current using a 0.7V geneeric LED forward voltage:

  I = (5 V - 0.7 V) / 470 Ω ≈ 9.15 mA

  The resistor limits the LED current and keeps it below the 20 mA target used

-i simulated the LED circuit in LTspice and compared the simulated behavior with the hand calculation. I also encountered and debugged a simulation that initially produced almost zero current, which helped me understand that a SPICE result is only useful when the circuit topology, component orientation, and connections are correct.

- i built a voltage divider using a 5 V source and two 10 kΩ resistors. Since the two resistors are equal, the midpoint voltage was calculated as:

  V out = 5 × 10kΩ / (10kΩ + 10kΩ) = 2.5 V

  I verified the result in LTspice and then changed the resistor ratio to observe how the output voltage changes.

- i earned why voltage dividers matter in embedded systems The output voltage depends on the resistor ratio, and in a real circuit the load connected to the divider also affects the result too.

- The main lesson from this day was the workflow of calculate → build → simulate → measure → compare → debug. LTspice is not replacing circuit analysis; it gives me a way to verify my calculations and investigate where real circuit behavior differs from simplified assumption.
