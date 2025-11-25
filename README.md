# NAME: JANANI V
# REG NO: 212223060099
# Interfacing-of-Stepper-Motor-with-LPC1768-ARM-Processor

**AIM**

To write an embedded C program to interface a temperature sensor (LM35) with an ARM processor (LPC1768 / LPC1343).

**COMPONENTS REQUIRED**

**Hardware**

LPC1768 / LPC1343

LM35 Temperature Sensor

LCD Module

**Software**

Coocox COIDE

Docklight (for serial monitoring)

**PROCEDURE**

1. In Coocox COIDE

2. Go to Start → All Programs → COIDE and open the IDE.

3. Create a new project, give a suitable file name, choose the destination folder, and click Next.

4. Select the microcontroller: Chip → NXP → LPC13xx → LPC1343 → Next.

5. From the repository, select the required library files (SYSCON and GPIO).

6. COIDE will create a new project workspace.

7. Open main.c, double-click it, and type/write the embedded C program.

8. Add required library source files to the project (Right-click on “include” → Add file to group → Add files).

9. Build the program using the Build option.

10. Flash the program using Download Code to Flash.

11. Interface the hardware components (LM35 + LCD) and observe the output.

12. In Docklight

13. Go to Start → Docklight → OK.

14. Start with a Blank Project / Blank Script and click Continue.

15. Enable Keyboard Console.

16. Run/flash the program in COIDE. The serial output will be displayed in the Docklight window.

**FILES TO ADD**

- Repository
- C library
- Retarget printf
- CMSIS Core
- CMSIS Boot
- Common header files
- SYSCON
- GPIO
- IOCON
- UART
- ADC
- Time

**Source Files**

- simpleexample.c
- UartReceiverInterrupt.c
- lcd.c
- lcd.h

**PIN DIAGRAM**

<img width="867" height="512" alt="image" src="https://github.com/user-attachments/assets/3b3be326-e64b-42ff-bdf4-b230565adb7c" />

**CIRCUIT DIAGRAM**

<img width="752" height="382" alt="image" src="https://github.com/user-attachments/assets/e84a63d1-1840-4c6f-8bc7-4543ac9ce6c7" />



**PROGRAM**

```
#include "lcd.h"

void ADCExp();

int main(void)
{
    ReceiverInterrupt();       // Automatically added by CoIDE
    init_lcd();
    lcd_putstring(0, "RAANA LM35 DEMO");
    ADCExp();

    while(1)
    {
    }
}
```

**OUTPUT**

<img width="669" height="520" alt="image" src="https://github.com/user-attachments/assets/ef4c97fd-dbb9-4cbf-bf53-630ff9f027a2" />

**RESULT**

Thus, an embedded C program to interface a temperature sensor with the ARM processor was executed and the output was verified successfully.
