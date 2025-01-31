# Task-2
DIGITAL LOGIC DESIGN WITH VERILOG
Name: PAVAN NARENDRA JAHAGIRDAR
Company: CODTECH IT SOLUTIONS
ID: CT12DS2941
Domain:VLSI(Very Large Scale Intergation)
Duration: December to Feburary 2025
Mentor:


Project Overview: Designing Basic Digital Logic Circuits in Verilog
This project focuses on designing, implementing, and simulating basic digital logic circuits like logic gates, adders, and multiplexers using Verilog in a VLSI simulation environment. The primary objective is to understand the functional behavior of these circuits and verify their correctness through simulation tools.

Key Steps and Explanation:
1. Introduction to Verilog in VLSI Design
Verilog: A hardware description language (HDL) used to model electronic systems. It is widely utilized in VLSI design for digital circuit modeling, simulation, and synthesis.
VLSI Design Environment: Software like Xilinx Vivado, ModelSim, or Cadence Virtuoso is used to write, simulate, and verify Verilog code.

2. Designing Digital Logic Circuits
a. Logic Gates:
Logic gates (AND, OR, NOT, NAND, NOR, XOR, XNOR) are fundamental building blocks of digital circuits.
Implementation in Verilog:
verilog
module and_gate (input a, b, output y);
    assign y = a & b;
endmodule
assign is used to specify combinational logic.

b. Adders:
Adders perform arithmetic operations in digital systems.
i)Half Adder: Adds two bits (A and B) and outputs the sum and carry.
ii)Full Adder: Adds three inputs (A, B, and Cin) and outputs the sum and carry.

Implementation in Verilog:
module full_adder (input a, b, cin, output sum, carry);
    assign sum = a ^ b ^ cin;
    assign carry = (a & b) | (b & cin) | (a & cin);
endmodule

c. Multiplexers (MUX):
Multiplexers select one input from multiple inputs based on a selection line.
2:1 MUX: Two inputs and one select line.

Implementation in Verilog:

module mux_2to1 (input a, b, sel, output y);
    assign y = (sel) ? b : a;
endmodule

3. Simulation of Verilog Designs
a. Simulation Setup:
Use simulation tools (e.g., ModelSim or Xilinx ISim).
Write a testbench in Verilog to provide input stimuli and observe outputs.

b. Testbench Example:
module testbench;
    reg a, b, sel;
    wire y;

    // Instantiate the design
    mux_2to1 uut (.a(a), .b(b), .sel(sel), .y(y));

    initial begin
        $monitor("Time=%0t: a=%b, b=%b, sel=%b, y=%b", $time, a, b, sel, y);
        a = 0; b = 0; sel = 0;
        #10 a = 1; b = 0; sel = 0;
        #10 a = 1; b = 1; sel = 1;
        #10 a = 0; b = 1; sel = 1;
        #10 $finish;
    end
endmodule
c. Waveform Analysis:
Use a waveform viewer to analyze outputs.
Verify if the circuit behaves as expected by comparing output values with theoretical results.

4. Analyzing Simulation Results
Waveform tools visually depict how output signals change with time.
Key points to analyze:
Timing of signal transitions.
Correctness of functional behavior.
Presence of glitches or incorrect outputs.
Example: For the 2:1 MUX, ensure that y corresponds to a or b based on sel.

5. Conclusion
This project effectively demonstrates the capability of Verilog as a hardware description language for modeling basic digital circuits.
By designing and simulating essential components such as logic gates, adders, and multiplexers, it showcases how Verilog can be used to
represent the functionality of digital systems at a high level.
The simulation process ensures that these circuits operate correctly, providing an opportunity to validate their behavior before progressing
to hardware synthesis. This step is critical in the VLSI design flow, as it minimizes errors and optimizes the designs for real-world implementation.
By engaging with this project, learners build a strong foundation in digital circuit design, simulation, and analysis. These skills serve as a 
stepping stone for understanding and developing more complex VLSI systems, such as sequential circuits, finite state machines, and system-on-chip (SoC) designs.
The tools and software used, such as ModelSim, Xilinx Vivado, or Cadence tools, provide a professional-grade design and simulation environment. 
The built-in waveform viewers in these tools allow for a detailed analysis of simulation results, enabling users to interpret circuit behavior and ensure accuracy.


Outcomes:
Ability to write and debug Verilog code.
Experience in simulating and analyzing circuit behavior.
Understanding of waveform interpretation to verify circuit functionality.

Logic gates Simulation ![image](https://github.com/user-attachments/assets/96cbabba-d3da-46dd-b723-db9055fbfc95)
![Multiplxers waveform](https://github.com/user-attachments/assets/598e629d-677c-4d29-b14c-04fccf97b2cd)
![Adder circuits](https://github.com/user-attachments/assets/07b0a52e-e33e-492a-a986-d5edd7ceaac4)




