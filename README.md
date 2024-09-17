# STM32L412KB-UART

This repo contains STM32CubeIDE projects for an STM32 Nucleo-L412KB board. Each project is a 
different method for transmitting ASCII data with a UART peripheral and blinks the on-board 
LED to show whether the data transmission is blocking the CPU:

- [UART_Transmit](https://github.com/caite21/STM32L412KB-UART/blob/main/UART_Transmit/Core/Src/main.c): Blocking Transmit (HAL_UART_Transmit)
- [UART_Interrupt](https://github.com/caite21/STM32L412KB-UART/blob/main/UART_Interrupt/Core/Src/main.c): Non-Blocking Transmit (HAL_UART_Transmit_IT)
- [UART_Normal_DMA](https://github.com/caite21/STM32L412KB-UART/blob/main/UART_Normal_DMA/Core/Src/main.c): Direct Memory Access (HAL_UART_Transmit_DMA)
- [UART_Double_Buffered_Circular_DMA](https://github.com/caite21/STM32L412KB-UART/blob/main/UART_Double_Buffered_Circular_DMA/Core/Src/main.c): Direct Memory Access (HAL_UART_Transmit_DMA) with Circular Transmission and a Double Buffer

The transmitted data looks like this (serial puTTY terminal):
![STM32_UART_data_puTTY](https://github.com/user-attachments/assets/d58ab3db-0f8c-4ab9-a68e-00372767e390)
