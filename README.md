Name: Aditya Singh 

Company: CODTECH IT SOLUTIONS

ID: CT08DS7686

Domain: VLSI

Duration: AUGUST TO SEPTEMBER 2024

Mentor: Neela Santhosh Kumar


Overview of the Project

## Project: DESIGN MEMORY CONTROLLER USING VERILOG

## Objective ##

The primary objective of the sram_controller module is to manage read and write operations to an SRAM (Static Random Access Memory). The module handles the control signals required for these operations and ensures proper timing and sequencing by using a finite state machine (FSM). It controls data flow between the SRAM and the system based on read and write requests.

## Key Activities and Technologies Used
    1)  Finite State Machine (FSM):

         Purpose: Manages the controller's states and transitions to handle different phases of read and write operations.
         States Defined:
               IDLE: The default state where the controller waits for read or write requests.
               READ: The state where the controller prepares to read data from the SRAM.
               WRITE: The state where the controller prepares to write data to the SRAM.
               WAIT: A state to allow time for the SRAM operation to complete.
               ERROR: An optional state to handle errors (though not used in this design).
       
      2) Sequential Logic :

             Clock Edge Triggered: Uses always @(posedge clk or posedge reset) to update the current_state based on the next_state or reset the FSM to the IDLE state.
           
      3) Combinational Logic:

              State Transitions and Outputs: Uses always @* to determine the next_state based on the current_state and input signals.
            It also sets control signals (read_enable, write_enable, ready) and assigns 
            the sram_address.
           
        4) Bidirectional Data Bus:

               Data Assignment:
                     Write Operation: When write_enable is high, the sram_data line is driven by the data bus.
                     Read Operation: When read_enable is high, the data bus is driven by the sram_data line.
                     High-Z State: When neither read nor write operations are active, the sram_data and data buses are in high-impedance (high-Z) state.
           
        5) Signal Handling:

             Control Signals:
                  read_enable: Activates the read operation on the SRAM.
                  write_enable: Activates the write operation on the SRAM.
                  ready: Indicates that the SRAM operation has completed and the system can proceed with the next operation.

## Technology Used

       1. Hardware Description Language (HDL)
            Verilog: The code is written in Verilog, a hardware description language used for modeling electronic systems.
            Verilog allows for the description of digital circuits and systems at various levels of abstraction, 
            from high-level functional descriptions to low-level gate-level designs.
      2. Finite State Machine (FSM)
           FSM Concept: The sram_controller module uses a finite state machine to manage the sequence of operations. 
           An FSM is a computational model consisting of states, transitions, and actions that helps in designing sequential logic circuits.
           In this case, the FSM controls the states of the SRAM controller (IDLE, READ, WRITE, WAIT, ERROR) and transitions between them based on input signals.


  The sram_controller project is designed to manage read and write operations for an SRAM module using Verilog HDL. It employs a finite state machine (FSM) to control the sequencing of operations, ensuring that the SRAM is accessed correctly. The FSM transitions through states (IDLE, READ, WRITE, WAIT, ERROR) based on input requests and manages control signals like read_enable, write_enable, and ready. The design uses both sequential and combinational logic to handle state transitions and data flow. Bidirectional data buses are utilized for read and write operations. The project ensures proper synchronization with the clock and handles asynchronous resets. Overall, it demonstrates effective digital design and control of memory operations.


![Screenshot (32)](https://github.com/user-attachments/assets/b6effd90-8c59-45aa-8354-619269372fc5) 
![Screenshot (33)](https://github.com/user-attachments/assets/7c8d228e-e59a-4e10-818e-c4736d790d23) 
![Screenshot (34)](https://github.com/user-attachments/assets/616d8ebc-354f-485f-81a2-5d100f3615b3)


