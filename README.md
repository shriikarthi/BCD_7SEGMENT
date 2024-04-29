#  BCD_7SEGMENT
# AIM
To design and simulate BCD 7 Segment using vivado.
# PROCEDURE

# BCD_7SEGMENT
![image](https://github.com/RESMIRNAIR/BCD_7SEGMENT/assets/154305926/804ab8db-8637-45ac-b10f-80e77d818d61)
# VERILOG CODE
~~~
//Verilog module.
module segment7(
     bcd,
     seg
    );
     
     //Declare inputs,outputs and internal variables.
     input [3:0] bcd;
     output [6:0] seg;
     reg [6:0] seg;

//always block for converting bcd digit into 7 segment format
    always @(bcd)
    begin
        case (bcd) //case statement
            0 : seg = 7'b0000001;
            1 : seg = 7'b1001111;
            2 : seg = 7'b0010010;
            3 : seg = 7'b0000110;
            4 : seg = 7'b1001100;
            5 : seg = 7'b0100100;
            6 : seg = 7'b0100000;
            7 : seg = 7'b0001111;
            8 : seg = 7'b0000000;
            9 : seg = 7'b0000100;
            //switch off 7 segment character when the bcd digit is not a decimal number.
            default : seg = 7'b1111111; 
        endcase
    end
    
endmodule
~~~
# OUTPUT
![326376083-431564c6-74a3-4b4a-af6a-44e3be1d721f](https://github.com/shriikarthi/BCD_7SEGMENT/assets/167749134/2135c67c-40a0-4ce1-9187-7c7f9dcd92e3)

# RESULT
Thus the BCD 7 Segment is verified succcessfully.
