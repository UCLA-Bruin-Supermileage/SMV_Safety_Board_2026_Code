# SMV_Safety_Board

This board is currently untested.

### Code Explanation

The main functions of the UI Board inclue:

1. Turn Motor on/off in response to UI Board Motor switch
2. When Optocoupler is pressed, kill ignition signal and freeze execution (re-ignition requires resetting the Safety Board STM32)
4. When Hydrogen is detected, kill ignition signal and freeze execution (re-ignition requires resetting the Safety Board STM32)


## Pin Assignment Info

|        Name        | Pin  |  GPIO Mode  |     Trigger    | GPIO Pull Up/Down |
|--------------------|------|-------------|----------------|-------------------|
| ignition_signal    | PA0  | GPIO_Output | N/A            | N/A               |
| optocoupler_output | PC0  | GPIO_EXTI0  | Rising/Falling | Pull-up           |
| Hydrogen_Output    | PC14 | GPIO_EXTI14 | Rising/Falling | Pull-down         |
| relay_output       | PB0  | GPIO_Input  | N/A            | Pull-up           |
