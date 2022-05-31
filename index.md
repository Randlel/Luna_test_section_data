## Luna Test Section Data Management Plan

### Research Overveiw
This research is on instabilities in supercritical carbon dioxide and how they affect heat transfer. We study near-critical CO2 as a working fluid. To improve the efficiency of different types of systems (ie. concentrated solar power generation, nuclear power generation, electronics cooling, etc.) we need to better understand heat transfer and how to control it.
Supercritical CO2 is when we increase the pressure of the system to the point where the CO2 is no longer gas or liquid but has properties similar to both. Near-critical refers to pressures and temperatures near the critial point. In the near critcal region CO2 is more susceptible to instabilities which can change the fluid properties (and therefore the heat transfer) dramatically. This work aims to better understand when these instabilities will be present and if they will enhance or degrade the heat transfer of the CO2.

### Data Description
All of the data is experimental measurements of physical properties at serveral points in the CO2 loop. The measurements are recorded numeric values that are then saved in spreadsheets (.csv). After the raw data is collected we process it using a python script which exports a single .csv file and any figures that we generate from the data. 

#### Measurement Types:
 + Point Temperature Measurements from Thermocouples (A numeric value of temperature over time per thermocouple)
 + Mass Flow Rate from a Coriolis Flow Meter (A numeric value of mass flow rate over time)
 + Pressure from a Pressure Transducer (A numeric value of pressure over time)
 + Power Applied to the Heated Area which is hand recorded from the Power Supply (A single set point for voltage and amperage (does not change with time))
 + 1D Temperature Array at test section wall (several thousand data point) from a Luna Fiber Optic Thermal Imaging System (An 1D array of temperature measurements over time) 
 
The point temperatures, mass flow rate, and pressure measurements are received by a DAQ. The data is then read into the computer by a software called LabView which records the data and saves it as an excel file. The power input is recorded by the experimentalist in a .txt file for each experiment. The Fiber Optic imaging will occur using a LUNA sensor. This sensor comes with software designed to read the signals from the fiber. The data is then saved as a .csv file. 

The total file size for this data set is expected to be about 1-2 GB.

### Roles and Responsibilities
#### Task (Responsible Party):
 + Creation of Safety Procedures (Grad Student and PI)
 + Implementation of Safety Procedures (Grad Student)
 + Enforcement of Safety Procedures (PI)
 + Equipment/Instrumentation Maintenance and Calibration (Grad Student)
 + Data Collection (Grad Student)
 + Data Organization and Backup Creation (Grad Student)
 + Metadata Generation (Grad Student)
 + Data Analysis  (Grad Student)
 + Data Analysis Software Creation and Maintenance (Grad Student)
 + Quality Control and Data Verification (Grad Student and PI)
 + Back up Drive Maintenance (PI)
 + Verifily that DMP is followed (Grad Student and PI)
 + Updating the DMP (PI)

Because this project is fairly independent there is no backup if either the PI or the grad student left unexpectedly. When the grad student graduates they are expected to train a new grad student who will inherit all the remaining responsibilities. 

### Data Standards and Metadata
#### Data Naming Conventions and Version Control:
Folder naming convention: yyyy_mm_dd_ breifDescriptionOfExperiment \
Data File Naming: yyyy_mm_dd_heatingMode_voltage_amperage \
New data files are created every time an experiment is run. New files are then created after the analysis tool is run. The files should never be modified only read into the analysis code and a new copy of the processed data is created every time the code is run. 
There is only one file of raw data per folder (both the file and folder are named using the naming convention). Each time the processing code is run a new file will be created the user should add a meaningful file name to indicate how it was processed. A .txt should also be included in the folder to describe what each iteration of the process files contains. 

#### Metadata Format:
The format of the raw data (internal file organization, definition of variables, units, etc.) will not change between experiments so a ReadMe in the main folder will be sufficient. This level should also contain a description of the project and a list of the experiments. Each experiment will have some hand-recorded data which should be added to the metadata.txt file. The metadata should be added to the folders after the data is collected but preferably before the researcher leaves the lab for that day. After the data is processed, a file should be created to list: each version of the analysis done, which fiber optic file was used in the analysis, and any additional notes about the experiment for example any observations made while running the experiment. The information about the analysis should be added each time the analysis code is run. Each of these metadata files is generated from an project specific template.

### Storage and Security
The data is stored/backed up on the local computer connected to the experimental setup, on OSU’s student drives, and in a Box drive. All backups to the box drive are automatic. The raw data is backed up to all 3 locations as soon as it is collected. As the data is processed it is backed up to the Box drive, a local computer drive, and an external hard drive. The data processing code is saved to seperate git hub repository, which will be shared when the code is fully functional. The Box drive is maintained for the lab and will be accessible after the grad student's graduation. We also have an internal lab procedure for archiving projects after a thesis is complete, so a separate copy of the data will be created and backed up at that point. 

There are no protection or security requirements for the data. We do not use any human-based data, only co2.

### Access and Data Sharing
There are no restrictions to sharing the data. The data set will be published in parallel with the paper that is currently in development. Our lab has prevously used figshare.com to share datasets publicly in the past. The spreedsheets where converted to .ods file type which is an OpenDocument Spreadsheet. This way the spreadsheet format is maintained but the files are more accessible. 

This work is a direct observation of physical phenomena so there is likely no copyright on the data set to start with, but we will use a CC0 license to release any remaining copyright. 

### Archiving and Preservation
After the data set is made publicly available it will be up to the data repository to preserve it. Figshare has an iso 27001 certification and backs up all data in Amazon Web Services S3 storage and in Chronopolis (a digital preservation service based out of The University of California at San Diego). In the short term, it will be backed up on our online Box server as well as on a physical backup hard drive.
