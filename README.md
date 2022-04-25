# Luna Test Section Data

# Research Overveiw:
This research is on instabilities in supercritical carbon dioxide and how they affect heat transfer. We study near-critical CO2 as a working fluid. To improve the efficiency of different types of systems (ie. concentrated solar power generation, nuclear power generation, electronics cooling, etc.) we need to better understand heat transfer and how to control it.
Supercritical CO2 is when we increase the pressure of the system to the point where the CO2 is no longer gas or liquid but has properties similar to both. Near-critical refers to pressures and temperatures near the critial point. In the near critcal region CO2 is more susceptible to instabilities which can change the fluid properties (and therefore the heat transfer) dramatically. This work aims to better understand when these instabilities will be present and if they will enhance or degrade the heat transfer of the CO2.

# Data Description:
| Measurement Type | Measurement Tool | Data Type |
| Point Temperature Measurements | Thermocouples | A numeric value of temperature over time per thermocouple |
| Mass Flow Rate | Coriolis Flow Meter | A numeric value of mass flow rate over time |
| Pressure | Pressure Transducer | A numeric value of pressure over time |
| Power Applied to the Heated Area | Hand Recorded from Power Supply | A single set point for voltage and amperage (does not change with time) |
| 1D Temperature Array at test section wall (several thousand data point) | Fiber Optic Thermal Imaging | An 1D array of temperature measurements over time |


The point temperatures, mass flow rate, and pressure measurements are received by a DAQ. The data is then read into the computer by a software called LabView which records the data and saves it as an excel file. The power input is recorded by the experimentalist in a .txt file for each experiment. The Fiber Optic imaging will occur using a LUNA sensor. This sensor comes with software designed to read the signals from the fiber. The data is then saved as a .csv file. 
