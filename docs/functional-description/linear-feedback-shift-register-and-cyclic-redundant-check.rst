Linear feedback shift register and cyclic redundant check(LFSR and CRC)
==========================================================================

The Linear Feedback Shift Register (LFSR) is the linear function of the output, given the output of the previous state, used as the displacement register of the input.The xor operation is the most common single-bit linear function: the xor operation is performed on some bits of the register as input, followed by the whole shift of each bit in the register.

Cyclic Redundancy check (CRC) is a data transfer error check function that performs polynomial calculations on the data and attach the results to the frame. The receiving device performs a similar algorithm to ensure the correctness and integrity of the data transfer.If the CRC fails to pass, the system repeatedly copies the data to the hard disk, falling into an infinite loop, resulting in the replication process cannot be completed.

The features of the linear feedback shift register and cyclic redundancy check are as follows:

1.	Support LFSR32: X32+X30+X26+X25
2.	Support CRC16: X16+X12+X5+1

CRC16:

1.	Select which data source
2.	Write CRCDAT to calculate CRC16
3.	Finish, can read CRCRES

LFSR32:

1.	Select which data source
2.	Write LFCRCCON bit8 to trigger LFSR
3.	Finish, can read LFSRRES
