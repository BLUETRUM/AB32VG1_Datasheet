Serial peripheral interface(SPI)
=================================

SPI can support different mode

1.	general 3 wire mode, 1-bit clock in/out, 1-bit data output, 1-bit data input.
2.	2 wire mode, 1-bit clock in/out, 1-bit data output or input.
3.	2 data bus mode, 1-bit clock in/out, 2-bit data output or input.

SPI Normal 1bit-Mode Operation Flow:

1.	Set 3-wire mode or 2-wire mode and select the pin map.
2.	Select RXSEL for Transmit or receive.
3.	Configure clock frequency .
4.	Select one of the four timing mode.
5.	Enable SPI module by setting SPIEN ‘1’.
6.	Set SPIIE ‘1’ if needed.
7.	Write data to SPIBUF to kick-start the process.
8.	Wait for SPIPND to change to ‘1’, or wait for interrupt.
9.	Read received data from SPIBUF if needed.
10.	Go to Step 8 to start another process if needed or turn off SPI1by clearing SPIIE and SPIEN.

SPI Normal multi-bit-Mode Operation Flow:

1.	Set data bus width(bus 2) and select the pin map.
2.	Select RXSEL for Transmit or receive.
3.	Configure clock frequency .
4.	Select one of the four timing mode.
5.	Enable SPI module by setting SPIEN ‘1’.
6.	Set SPIIE ‘1’ if needed.
7.	Write data to SPIBUF to kick-start the process.
8.	If data bus width are 2 bit, write SPIBUF twice kick-start the transmission.
9.	However, when receive data, only need write once to kick-start receive process.
10.	Wait for SPIPND to change to ‘1’, or wait for interrupt.
11.	Read received data from SPIBUF if needed.
12.	Go to Step 8 to start another process if needed or turn off SPI by clearing SPIIE and SPIEN.

SPI DMA Mode Operation Flow:

1.	Set IO in the correct direction and data width mode.
2.	Select RXSEL for DMA direction.
3.	Configure clock frequency .
4.	Select one of the four timing modes.
5.	Enable SPI module by setting SPIEN to ‘1’.
6.	Set SPIIE ‘1’ if needed.
7.	configure SPI1DMAADR.
8.	Write data to SPI1_DMACNT to kick-start a DMA process.
9.	Wait for SPIPND to change to ‘1’, or wait for interrupt.
10.	Go to Step 8 to start another DMA process if needed or turn off SPI1 by clearing SPI1EN.
