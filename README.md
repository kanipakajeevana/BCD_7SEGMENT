# BCD_7SEGMENT
![image](https://github.com/kanipakajeevana/BCD_7SEGMENT/assets/170450203/c993181e-9779-4da3-8d29-2114912b6d08)
# VERILOG CODE
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
# OUPUT
![image](https://github.com/kanipakajeevana/BCD_7SEGMENT/assets/170450203/2cea14a6-2f05-4968-8858-c73a9cce8aa9)


