# SMV_UI_TestBench

This is the test bench for the Safety Board, currently untested.

### Automatic Setup

To setup, clone this repo.

### Code Explanation

The main functions of the UI Board inclue:

1. When recieve Motor message from UI Board via CAN, send ignition signal
2. When optocoupler_output goes low, kill ignition signal (using interrupt for immediate response)
3. Read optocopuler, hydrogen, and relay output



## Pin Assignment Info

|        Name        | Pin  |  GPIO Mode  |     Trigger    | GPIO Pull Up/Down |
|--------------------|------|-------------|----------------|-------------------|
| ignition_signal    | PA0  | GPIO_Output | N/A            | N/A               |
| optocoupler_output | PC0  | GPIO_EXTI0  | Rising/Falling | Pull-up           |
| Hydrogen_Output    | PC14 | GPIO_EXTI14 | Rising/Falling | Pull-down         |
| relay_output       | PB0  | GPIO_Input  | N/A            | Pull-up           |