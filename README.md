## AIM:

To implement and design synthesis and simulation for uart using cadence - genus and innovus.

## TOOLS REQUIRED:

Functional Simulation: Incisive Simulator (ncvlog, ncelab, ncsim) Synthesis: Genus Floorplanning: Innovus

## PROCEDURE:

Step 1: Synthesis requires the following files as follows: ◦ Liberty Files (.lib) ◦ VerilogFiles (.v )

### Add Verilog  (.v ) file

### Add Testbench file

### Add run.tcl file

SDC (Synopsis Design Constraint) File (.sdc)

In your terminal type “gedit input_constraints.sdc” to create an SDC File if you do not have one.

The SDC File must contain the following commands; 

### Add SDC file

i→ Creates a Clock named “clk” with Time Period 2ns and On Time from t=0 to t=1. 

ii, iii → Sets Clock Rise and Fall time to 100ps. 

iv → Sets Clock Uncertainty to 10ps. 

v, vi → Sets the maximum limit for I/O port delay to 1ps.

•	The Liberty files are present in the library path,

•	The Available technology nodes are 180nm ,90nm and 45nm.

•	In the terminal, initialise the tools with the following commands if a new terminal is being used. ◦ csh ◦ source /cadence/install/cshrc

•	The tool used for Synthesis is “Genus”. Hence, type “genus -gui” to open the tool.

•	Genus Script file with .tcl file Extension commands are executed one by one to synthesize the netlist. Step 2 : Creating an SDC File Step 3 : Performing Synthesis

### Fig 1: RTL Simulation:
![WhatsApp Image 2025-11-21 at 20 41 45_f0f0308b](https://github.com/user-attachments/assets/39b4ab91-aee3-4f89-9462-3560312aa372)

### Fig 2: Synthesis RTL Schematic:
![WhatsApp Image 2025-11-21 at 20 39 24_f20f2295](https://github.com/user-attachments/assets/de7b919e-d506-4042-91f9-e899469913ac)

### Fig 3: Area Report:
![WhatsApp Image 2025-11-21 at 20 39 25_3dd8785a](https://github.com/user-attachments/assets/5346afd0-b10e-4906-b223-aba479a22896)

### Fig 4: Power Report:
![Uploading WhatsApp Image 2025-11-21 at 20.39.23_c83a58f4.jpg…]()

### Fig 5: Timing Report:
![WhatsApp Image 2025-11-21 at 20 39 26_5754e9b0](https://github.com/user-attachments/assets/2a6cfeb3-1935-4c2e-92a4-3af5e4618e81)

### Fig 6: UART APR:

## RESULT:

The functionality of the uart was successfully verified using a testbench and simulated with the nclaunch tool and genus and for innovus creating the physical design.
