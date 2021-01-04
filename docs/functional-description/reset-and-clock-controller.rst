Reset and clock controller
==================================

Clock management
-----------------

The devices receives the following clock source inputs:

+ Internal oscillator
    + 2MHz RC oscillator
+ External oscillator
    + clock: 26MHz(generated form a crystal/ceramic resonator)

System reset sources
---------------------

The product contains multiple reset sources,which include：

+ POR reset
+ MCLR reset
+ WKP 10S reset
+ LVD reset
+ UART0 key match reset
+ UART1 key match reset
+ UART2 key match reset
+ Wakeup software shut down reset
+ VUSB insert reset
+ WDT reset

The first three reset source will reset all chip except the part which in RTC, and the other reset sources will reset all chip except the part which in RTC or some register in CORE.

