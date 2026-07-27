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

- i Tested the Full Adder using all 8 possible combinations of the three inputs i saw it first using truth table. The results matched binary addition, confirming that the circuit was working correctly.

- This all helped me understand how simple logic gates can be combined and operate to build arithmetic circuits, its amazing btw. and also By chaining multiple Full Adders together, a circuit can perform multi-bit binary addition, which connects digital logic to the arithmetic hardware used inside computer processors and ALUs as i understood it from different sources.
