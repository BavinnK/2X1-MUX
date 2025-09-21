# 2-to-1 Multiplexer in Resistor-Transistor Logic (RTL)

## Project Overview

This project is a hardware implementation of a 2-to-1 multiplexer (MUX) built from scratch using discrete components on a breadboard. The logic is based on **Resistor-Transistor Logic (RTL)**, demonstrating the foundational principles of digital circuit design before the era of integrated circuits.

A multiplexer, or MUX, is a digital switch that selects one of several input signals and forwards the selected input to a single output line. This 2-to-1 MUX uses a single select line (`S0`) to choose between two data inputs (`I0` and `I1`).

## Circuit Diagrams and Implementation

Below are the logic diagram for the 2-to-1 MUX and a photo of the final circuit implemented on a breadboard.

### Logic Diagram & Truth Table

![20250921_222618](https://github.com/user-attachments/assets/561389b3-99d8-4932-bb97-27fc3d380bd3)


The behavior of the multiplexer is described by the following truth table and boolean expression:

| S0  | Output (Y) |
| :-- | :--------- |
| 0   | I0         |
| 1   | I1         |

**Boolean Expression:** `Y = (S0' ⋅ I0) + (S0 ⋅ I1)`

### Breadboard Prototype

![20250921_222622](https://github.com/user-attachments/assets/e20faa4b-a860-467c-a25b-f1596e035ed4)

## How It Works

The circuit uses Resistor-Transistor Logic (RTL) to create the necessary AND and OR logic gates to fulfill the boolean expression.
- When the select line `S0` is LOW (logic 0), the first AND gate is enabled, allowing the `I0` signal to pass through to the output.
- When `S0` is HIGH (logic 1), the second AND gate is enabled, allowing the `I1` signal to pass through.

This provides a way to dynamically select a data source in a digital system.

### Components Used
*   9 x Bipolar Junction Transistors (BJTs)
*   16 x Resistors
*   1 x Push button (for the `S0` select line)
*   1 x Bypass capacitor (for switch debouncing)
*   1 x Pull-down resistor (for the push button)

## How to Test the Circuit

To verify the functionality of the multiplexer, you can use two signal generators for the inputs and an oscilloscope to view the output.

### Equipment Needed
*   Two Signal Generators (to provide `I0` and `I1` signals)
*   An Oscilloscope (to observe the output `Y`)
*   A power supply for the breadboard circuit

### Testing Procedure
1.  Connect the output of the first signal generator to the **`I0`** input of the circuit.
2.  Connect the output of the second signal generator to the **`I1`** input.
3.  Connect the output **`Y`** of the multiplexer to a channel on the oscilloscope.
4.  **Test the I0 path:** With the `S0` push button **not pressed** (logic `0`), the oscilloscope should display the signal coming from the first signal generator (`I0`).
5.  **Test the I1 path:** While **pressing** the `S0` push button (logic `1`), the output on the oscilloscope should switch to display the signal from the second signal generator (`I1`).

## Future Enhancements

This project serves as a foundation for building more complex digital logic circuits. Future plans include designing and building:

-   A **4-to-1 Multiplexer** (4 data inputs, 2 select lines)
-   An **8-to-1 Multiplexer** (8 data inputs, 3 select lines)

These projects will continue to explore digital design using discrete components.
