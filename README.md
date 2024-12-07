### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
module encoder_8to3 (
    input [7:0] D,    
    output reg [2:0] A 
);

    always @ (D) begin
        case (D)
            8'b10000000: A = 3'b111; 
            8'b01000000: A = 3'b110; 
            8'b00100000: A = 3'b101; 
            8'b00010000: A = 3'b100; 
            8'b00001000: A = 3'b011;
            8'b00000100: A = 3'b010; 
            8'b00000010: A = 3'b001; 
            8'b00000001: A = 3'b000; 
            default: A = 3'bxxx;     
        endcase
    end

endmodule



```

Developed by:Rohith V RegisterNumber:24900447
*/

**RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling**

![Screenshot 2024-12-07 155147](https://github.com/user-attachments/assets/b549de93-ffcd-43f9-867e-98d4e676b1a9)


**TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling**
![Screenshot (60)](https://github.com/user-attachments/assets/009c2c55-d557-4bee-8c40-47beee49e0fe)

Result:
The implementation of  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables







