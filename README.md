### study-of-basic-gates

**AIM:** 

To study and verify the truth table of logic gates in Quartus II using Verilog programming.

**Equipments Required:**

Software – Quartus prime 

**Theory**

Introduction Logic gates are the basic building blocks of any digital system. Logic gates are electronic circuits having one or more than one input and only one output. The relationship between the input and the output is based on a certain logic. Based on this, logic gates are named as

AND gate OR gate NOT gate NAND gate NOR gate Ex-OR gate Ex-NOR gate

**AND gate**

The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB
Y= A.B

**OR gate** 

The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation.
Y= A+B

**NOT gate**

The NOT gate is an electronic circuit that produces an inverted version of the input at its output. It is also known as an inverter. If the input variable is A, the inverted output is known as NOT A. This is also shown as A' or A with a bar over the top, as shown at the outputs.
Y= A'

**NAND gate**

This is a NOT-AND gate which is equal to an AND gate followed by a NOT gate. The outputs of all NAND gates are high if any of the inputs are low. The symbol is an AND gate with a small circle on the output. The small circle represents inversion.
Y= (AB)’

**NOR gate**

This is a NOT-OR gate which is equal to an OR gate followed by a NOT gate. The outputs of all NOR gates are low if any of the inputs are high. The symbol is an OR gate with a small circle on the output. The small circle represents inversion.
Y= (A+B)’

**Ex-OR gate**

The 'Exclusive-OR' gate is a circuit which will give a high output if either, but not both of its two inputs are high. An encircled plus sign (⊕) is used to show the Ex-OR operation.
Y= A⊕B

**Ex-NOR gate**

The 'Exclusive-NOR' gate circuit does the opposite to the EX-OR gate. It will give a low output if either, but not both of its two inputs are high. The symbol is an EX-OR gate with a small circle on the output. The small circle represents inversion.
Y= A⊕B

**Procedure** 

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**PROGRAM**

Program for logic gates and verify its truth table in quartus using Verilog programming
```
/*
WARNING: Do NOT edit the input and output ports in this file in a text
editor if you plan to continue editing the block that represents it in
the Block Editor! File corruption is VERY likely to occur.
*/

/*
Copyright (C) 1991-2013 Altera Corporation
Your use of Altera Corporation's design tools, logic functions 
and other software and tools, and its AMPP partner logic 
functions, and any output files from any of the foregoing 
(including device programming or simulation files), and any 
associated documentation or information are expressly subject 
to the terms and conditions of the Altera Program License 
Subscription Agreement, Altera MegaCore Function License 
Agreement, or other applicable license agreement, including, 
without limitation, that your use is for the sole purpose of 
programming logic devices manufactured by Altera and sold by 
Altera or its authorized distributors.  Please refer to the 
applicable agreement for further details.
*/

HEADER
{
	VERSION = 1;
	TIME_UNIT = ns;
	DATA_OFFSET = 0.0;
	DATA_DURATION = 100.0;
	SIMULATION_TIME = 0.0;
	GRID_PHASE = 0.0;
	GRID_PERIOD = 10.0;
	GRID_DUTY_CYCLE = 50;
}

SIGNAL("a")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = INPUT;
	PARENT = "";
}

SIGNAL("b")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = INPUT;
	PARENT = "";
}

SIGNAL("f1")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = OUTPUT;
	PARENT = "";
}

SIGNAL("f2")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = OUTPUT;
	PARENT = "";
}

SIGNAL("f3")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = OUTPUT;
	PARENT = "";
}

SIGNAL("f4")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = OUTPUT;
	PARENT = "";
}

SIGNAL("f5")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = OUTPUT;
	PARENT = "";
}

SIGNAL("f6")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = OUTPUT;
	PARENT = "";
}

SIGNAL("f7")
{
	VALUE_TYPE = NINE_LEVEL_BIT;
	SIGNAL_TYPE = SINGLE_BIT;
	WIDTH = 1;
	LSB_INDEX = -1;
	DIRECTION = OUTPUT;
	PARENT = "";
}

TRANSITION_LIST("a")
{
	NODE
	{
		REPEAT = 1;
		NODE
		{
			REPEAT = 5;
			LEVEL 0 FOR 10.0;
			LEVEL 1 FOR 10.0;
		}
	}
}

TRANSITION_LIST("b")
{
	NODE
	{
		REPEAT = 1;
		NODE
		{
			REPEAT = 6;
			LEVEL 0 FOR 8.0;
			LEVEL 1 FOR 8.0;
		}
		LEVEL 0 FOR 4.0;
	}
}

TRANSITION_LIST("f1")
{
	NODE
	{
		REPEAT = 1;
		LEVEL X FOR 100.0;
	}
}

TRANSITION_LIST("f2")
{
	NODE
	{
		REPEAT = 1;
		LEVEL X FOR 100.0;
	}
}

TRANSITION_LIST("f3")
{
	NODE
	{
		REPEAT = 1;
		LEVEL X FOR 100.0;
	}
}

TRANSITION_LIST("f4")
{
	NODE
	{
		REPEAT = 1;
		LEVEL X FOR 100.0;
	}
}

TRANSITION_LIST("f5")
{
	NODE
	{
		REPEAT = 1;
		LEVEL X FOR 100.0;
	}
}

TRANSITION_LIST("f6")
{
	NODE
	{
		REPEAT = 1;
		LEVEL X FOR 100.0;
	}
}

TRANSITION_LIST("f7")
{
	NODE
	{
		REPEAT = 1;
		LEVEL X FOR 100.0;
	}
}

DISPLAY_LINE
{
	CHANNEL = "a";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 0;
	TREE_LEVEL = 0;
}

DISPLAY_LINE
{
	CHANNEL = "b";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 1;
	TREE_LEVEL = 0;
}

DISPLAY_LINE
{
	CHANNEL = "f1";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 2;
	TREE_LEVEL = 0;
}

DISPLAY_LINE
{
	CHANNEL = "f2";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 3;
	TREE_LEVEL = 0;
}

DISPLAY_LINE
{
	CHANNEL = "f3";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 4;
	TREE_LEVEL = 0;
}

DISPLAY_LINE
{
	CHANNEL = "f4";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 5;
	TREE_LEVEL = 0;
}

DISPLAY_LINE
{
	CHANNEL = "f5";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 6;
	TREE_LEVEL = 0;
}

DISPLAY_LINE
{
	CHANNEL = "f6";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 7;
	TREE_LEVEL = 0;
}

DISPLAY_LINE
{
	CHANNEL = "f7";
	EXPAND_STATUS = COLLAPSED;
	RADIX = Binary;
	TREE_INDEX = 8;
	TREE_LEVEL = 0;
}

TIME_BAR
{
	TIME = 0;
	MASTER = TRUE;
}
;
```

 Developed by: P Manasa RegisterNumber: 212224230149
 
**Logic symbol & Truthtable**![ex1](https://github.com/user-attachments/assets/a23c0717-d305-4dec-b161-4461e961ebcf)


**RTL realization Output:** 
![Screenshot 2025-03-12 102903](https://github.com/user-attachments/assets/ebf35a24-fe29-4b71-b4ef-47fcc556e4f5)

**RTL**

**Result:**
Thus it has been study and verified the truth table of logic gates in Quartus II using Verilog programming.

