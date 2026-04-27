# 12V 3S 18650 Battery Management & Power System

This project features a custom-built 12V rechargeable battery pack using three 18650 Lithium-ion cells. It integrates a Battery Management System (BMS) for safety, a buck converter for regulated output, and an integrated charging interface.

## 🛠 Hardware Components
* **Cells:** 3x 18650 Lithium-ion Batteries (3.7V nominal each, 11.1V - 12.6V total).
* **BMS:** 3S 20A Lithium Battery Protection Board (controls overcharge, over-discharge, and short circuits).
* **Regulator:** DC-DC Buck Converter (Step-down module).
* **Indication:** LED with Current-Limiting Resistor.
* **Input/Output:** 2x DC Power Jacks (Charging input and Power output).
* **Control:** Tactile Push Button / Toggle Switch.
* **Protection:** 1N4007 Diode (Reverse polarity protection).

## 🔌 Circuit Configuration
1.  **Battery Pack:** Cells are wired in series. 
    * B- to 0V (Negative of 1st cell)
    * B1 to 4.2V (Positive of 1st cell)
    * B2 to 8.4V (Positive of 2nd cell)
    * B+ to 12.6V (Positive of 3rd cell)
2.  **BMS Output:** P+ and P- provide the protected discharge and charging path.
3.  **Buck Converter:** Connected to the BMS output to provide a stable, lower voltage (e.g., 5V or 3.3V) for microcontrollers.
4.  **Charging:** Handled via the DC Barrel jack, protected by a diode to prevent backflow from the battery.

## ⚠️ Safety Warnings
* **Balance Charging:** Ensure all 18650 cells are at the same voltage level before assembly.
* **Current Limits:** Do not exceed the 20A rating of the BMS.
* **Insulation:** Ensure all solder points are insulated with heat shrink or Kapton tape to prevent shorts in a hostel/portable environment.
