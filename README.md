
# Writing a C code to count the sum of numbers from 1 to n and running this program using RISC-V simulator

# Writing a C code to count sum of numbers from 1 to n.

1. First, I opened the terminal and wrote code to create and open a new C file in Leaf pad,
as demonstrated below:

2. Next, I wrote my code in Leaf pad as illustrated below :

3. Then I compiled and ran it in the terminal to verify, and achieved the desired
output.

4. Then I tested different values of n, such as n=100, and obtained the results.


# Running above program in RISC-V Simulator
After running the code in the terminal, I need to execute it in the RISC-V simulator. For this,
a specific set of code is required, which I have implemented in the following steps.:

1) First, I wrote code to compile it with the RISC-V GCC compiler using option 1, which
generates a file with a .o extension.


![WhatsApp Image 2024-05-28 at 7 40 26 PM](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/ae962dce-0e48-4c5b-ab03-35acafa9f94f)

2) With the command `riscv-unknown-elf-objdump -d sum1ton.o` to obtain the assembly
code for the above C program. This generated numerous assembly instructions, which
I filtered by appending `| less` to the command. To locate the main section, I searched
for "main." The byte address for main was found to be 10184, and there were 15
instructions when using option 1. It was observed that the address of each consecutive
instruction increments by 4.

![WhatsApp Image 2024-05-28 at 7 39 49 PM](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/377bff12-741d-4b6b-b1f3-4b5ae1890fe4)

3) Next, I ran the same commands but used the `-Ofast` option instead of `-O1`. This
time, I got fewer instructions, specifically 12. This demonstrates that the assembly
instructions in the file change based on the different compilation options used.


![WhatsApp Image 2024-05-28 at 7 38 58 PM](https://github.com/Olirmathi-Nagarajan/VSDSquadron-Mini-Internship/assets/170841944/f355c671-5f7d-4b84-9edd-794f900137da)

# And that’s all !!!


