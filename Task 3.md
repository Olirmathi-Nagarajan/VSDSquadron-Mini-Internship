# Task-3

Functional simulation experiment using RISC-V Core Verilog netlist and testbench.
* IVERILOG:- Icarus Verilog, commonly referred to as IVerilog, is an open-source Verilog simulation and synthesis tool. It is an implementation of the Verilog hardware description language compiler that generates netlists in the desired format (EDIF) and a simulator.It is widely used in both educational and professional settings for hardware design and verification.

* GTKWAVE:- GTKWave is an open-source waveform viewer that allows users to view signal simulations in various digital design formats, such as VCD (Value Change Dump), LXT, and others. It is commonly used for debugging and analyzing digital circuits and systems.

1 .
INSTALL IVERILOG:
using following command:-

     $ sudo apt install iverilog

INSTALL GTKWAVE:
using following command:-

     $ sudo apt install iverilog gtkwave

2 . create the verilog file and testbench file in github repository.

     $ git clone [https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship]
     $ cd vsdsquadron-mini-internship

3 . simulate and run the code, using following command:-
        
     $ iverilog.exe -o dsn olirmathi_rv32i_tb.v olirmathi_rv32i.v

  ![task 3i](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/9be253fe-ac44-4129-a593-26f6ec63f056)

     $ vvp.exe dsn

  ![task 3ii](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/84fb1fe9-06ab-405e-9fed-215a587d7e1b)

4 . And for output waveform give following command:-

     $ gtkwave.exe olirmathi_rv32i.vcd

  ![task 3iv](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/fda57592-4cfa-4741-8847-a59dcea36a15)

5 . Analyze the Wave form of each instruction using gtkwave.

following instruction are:-
1.ADD r6, r2, r1

2.SUB r7, r1, r2

3.AND r8, r1, r3

4.OR r9, r2, r5

5.XOR r10, r1, r4

6.SLT r11, r2, r4

7.ADDI r12, r4, 5

8.SW r3, r1, 2

9.SRL r16, r14, r2

10.BEQ r0, r0, 15

![inter task 3](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/c51a16aa-7b4d-4381-b617-4d9784679900)

![task 3](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/2a512140-5123-4933-a89b-db7d70f57f47)

Full 5-stage instruction pipeline and pc increment description Waveform

![internship task 3](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/815af121-89d1-4853-9999-13acf1df029b)
