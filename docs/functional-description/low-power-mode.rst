Low power mode
================

The product supports two low-power modes to achieve the best compromise between low-power consumption, short startup time and available wakeup sources:

sleep mode
-------------

Sleep mode will auto gate system clock, close memory access, close RC2M, but some asynchronous clock should be disable by software

Sleep mode wake up source as follow. After wakeup, software run continue or enter interrupt if enable:

1.	BT wakeup
2.	port external interrupt wakeup
3.	RTC 1s or alarm wakeup
4.	SPDIF online wakeup
5.	IR receive data or repeat press wakeup

sniff mode
------------

Sniff mode will auto gate system clock, close memory access, close RC2M, but some asynchronous clock should be disable by software. Sniff also change VDDIO/VDDCORE voltage by LPMCON

Sniff mode wake up source as follow. After wakeup, software run continues or enter interrupt if enable:

1.	BT wakeup
2.	Port external interrupt wakeup
3.	RTC 1s or alarm wakeup
4.	SPDIF online wakeup
5.	IR receive data or repeat press wakeup
