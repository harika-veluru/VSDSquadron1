# VSDSquadron1

TASK1

The task was to install RISC-V toolchain and the installation is done.

Then the task was to complile the c program which calculates the sum from 1 to n.For this the command to open is "gedit sum1ton.c".
And after the code is written for sum of integers we need to compile it and the following commands were used to accomplish the same.After the compilation the sum value will be printed as shown below.The command to display the output is "./a.out".

![WhatsApp Image 2024-05-21 at 9 16 54 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/22081e20-03fb-4d4a-a331-5284ac627e41)

![WhatsApp Image 2024-05-21 at 9 15 40 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/c0db19f5-9787-4ea6-84f1-0e76102e7ef0)

![WhatsApp Image 2024-05-21 at 9 16 54 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/6ac14dcc-ce01-4e47-936c-e905dd818197)

Next to compile the same code with RISC-V compiler.
For that we need to open the code in terminal itself.Command to open is "cat sum1ton.c" as shown below.

![WhatsApp Image 2024-05-21 at 9 19 04 PM (1)](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/11f76780-7e05-4eb3-995d-3a65ea1c041d)

Then the following command is used to create .o file as shown below.

![WhatsApp Image 2024-05-21 at 9 30 15 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/54eb1fe8-fb2c-4391-b949-c46213d1b8e3)

Then to open the assembly level instructions for the above written c code  we use the following command

![WhatsApp Image 2024-05-21 at 9 34 44 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/6231d6f1-1ba2-4780-8c17-32520eda5b9e)

Then a huge set of instructions are generated as shown below.

![WhatsApp Image 2024-05-21 at 9 36 26 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/30a00e8f-9ffa-45e5-8eb0-09c48582fe1f)

In this code lets search for the "main".

![WhatsApp Image 2024-05-21 at 9 39 49 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/dd7480ce-c71c-4dc1-8cf9-c7b8c6924b26)

 if we subtract 101b0-10184 it is 11 so there are 11 instructions in this above assembly code in the "main".

To reduce the number of instructions we add"|less"  along with the above command which  generates less assembly code instructions in this we are mainly concerned about main so to search we use "/main" and this is how it looks.

Next we can compile in other way as shown below

![WhatsApp Image 2024-05-21 at 10 04 10 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/85b7bb3c-acf4-42cd-9c7d-136dd0118ff0)

![WhatsApp Image 2024-05-21 at 10 03 23 PM (1)](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/b04e9e0b-e423-43a4-a9fd-afb63d17e1cf)

The number of instructions hasn't changed because it was a simple program.


