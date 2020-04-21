# Overview 
This project will forward stdout and stdin from the System Workbench IDE console to the MCU's UART. Access to the MCU's UART interface will be through a terminal emulator program called PuTTY. 

# Procedure
1. Go to the Device Manager to find the COM port where the UART will be accessed from. The COM port number you need is in blue. In this picture it is COM5.  
![device_mgr](../img/1_device_manager.png)
2. Load the code onto the processor (click Run).  
![run_button](../img/1_run_button.png) 
3. Open a PuTTY window to see the output of the UART.  
![putty_config](../img/1_putty_config.png) 
4. See Output!  
![putty_output](../img/1_putty_output.png)  

# References
[STM32 System Workbench UART Printf project](https://github.com/STMicroelectronics/STM32CubeF4/tree/master/Projects/STM32F411RE-Nucleo/Examples/UART/UART_Printf/SW4STM32) : Even though this project's build configuration didn't work, I used their code to forward the printf to the virtual COM Port supplied by the nucleo.

