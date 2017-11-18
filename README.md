# ssi_example_ns
SPI Tiva TM4C123GXL send/receive example

Keil uVision 5 project based on TI tivaware ssi example - C:\ti\TivaWare_C_Series-2.1.4.178\examples\peripherals\ssi\spi_master.c

I changed quite a lot before this project could run, what bugged me most was that i had to include both uart.c and uartstdio.c in the project.
I also changed the pins for UART to use the USB debugger port, i left the original code in there.

Open a Putty serial connection on your local com port that the tiva board is assigned and configure it for 115200, 1-8-1.
The connect pins PA4 and PA5. 
If you dont see anything immediately in putty, hit the reset switch on the tiva board :-)

From the TI example:
//! This example shows how to configure the SSI0 as SPI Master.  The code will
//! send three characters on the master Tx then polls the receive FIFO until
//! 3 characters are received on the master Rx.
//!
//! This example uses the following peripherals and I/O signals.  You must
//! review these and change as needed for your own board:
//! - SSI0 peripheral
//! - GPIO Port A peripheral (for SSI0 pins)
//! - SSI0Clk - PA2
//! - SSI0Fss - PA3
//! - SSI0Rx  - PA4
//! - SSI0Tx  - PA5
//!
//! The following UART signals are configured only for displaying console
//! messages for this example.  These are not required for operation of SSI0.
//! - UART0 peripheral
//! - GPIO Port A peripheral (for UART0 pins)
//! - UART0RX - PA0
//! - UART0TX - PA1
