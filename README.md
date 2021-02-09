# ESS-DIVE Hydrological Monitoring Reporting Format

## Getting started [This Reporting Format content is in draft form and incomplete.]

## How to contribute

## About the Hydrological Monitoring Reporting Format
SCOPE - This reporting format is intended for water level, temperature, electrical conductivity, specific conductivity, dissolved oxygen, and pH measured in situ using sensors deployed in water bodies.

SUMMARY - This standard uses a **three file system to organize data, sensor metadata, and terminology metadata.** The reporting format is designed to be flexible for each user’s needs. If the user has measured parameters outside the scope or has other columns they would like to add, they should do so. Aside from required fields, the user should only populate their file with the fields relevant to their data. 

CONTENT - This folder includes 5 files in addition to the readme. The **Quick Start Guide** has short, simple directions for using the reporting format. **Recommended Vocabulary** lists preferred terms with units and definitions. The other three files are **templates**. The **Data** File is for sensor-based data collected in the field. The **Sensor** File is for metadata about the sensors and the locations used to generate the data. The **Terminology** File allows users to define column headers and terms used throughout the files (i.e., data flags, missing value terms). The templates indicate **required fields** includes the information that must be contained in the submitted files. Users can choose items listed in **optional fields** as they see fit; however we strongly suggest users populate all fields for which they have information. Scroll down for screengrabs of the templates.

COLUMN HEADERS - **For the Sensor and Terminology Files, column headers terms must match those listed in the templates.** These column headers are not required to be defined in the Terminology File, because they must match the template terms. **For the Data File(s), column header terms are recommended and listed in the Recommended Vocabulary file.** If non-recommended column header terms are chosen for the Data File(s), they must have no spaces and only use underscores as special characters. The preferred format is to use underscores to separate units from a measurement term  (e.g., SpC_uScm). **All column headers from the Data File(s) must be defined in the Terminology File.** Definitions should be copy and pasted from the Recommended Vocabulary file unless a term is not listed there. Additional detail such as the water body type or depth at which the measurement was taken should be defined in the appropriate Sensor File fields. 

EMPTY CELLS - Empty cells are not permitted. They should be filled with missing value terms, which must be defined in the Terminology File. 	

FILE FORMAT - Files should be saved as comma-separated .csv files.

NAMING CONVENTION - If there is a single Data File in the data package, the preferred naming structure is to use a single file name appended with either "_data", "_sensor", or "_terminology" for each of the three files. If there are multiple data files and a single sensor and single terminology file, the preferred naming structure is to use a chosen name appended with either “_sensor” or “_terminology” for the two files.

ADDITIONAL CONTENT - Users are encouraged to include raw data files, sensor specification PDFs from manufacturers, code used for data collection or data processing, or links to relevant github content in their data packages. Users can also include documents describing sensor calibration, QA/QC, or other information.

REQUIRED FIELDS - Some fields are described as required in “Sensor File (or Data File).” For time series data at a single location, these fields are appropriate in the Sensor File. However, if instead a sensor is moved to multiple locations and the Data File is thus based on spatial changes rather than temporal changes, the fields are likely more appropriate in the Data File. Either choice is acceptable as long as the fields are included somewhere within the dataset.

MULTIPLE SENSORS - Data from multiple sensors can be handled in several different ways depending on the user’s needs: (1) Data from each sensor can be in a separate data file. The user can decide if they would like a single Sensor File and Terminology file that includes information for all the data files or separate accompanying files for each data file; (2) Data from each sensor can be combined in the same file if the sensors are synced and have identical timestamps, thereby producing a single date/time column and multiple parameter columns. If a Data File has the same parameter more than once, a prefix, suffix, or other differentiating text should be added in the column headers; (3) If the sensors have the same data types, the data can be combined in the same file with a single date/time column, a single parameter column, and a sensor ID or sensor serial number column that indicates which rows are linked to which sensor. In this format, time stamps may be repeated.
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/FileStructures.JPG "Options for number and structure of files")

WATER LEVEL TERMS - See the graphic below for a visual representation of the terms listed in the Recommended Vocabulary file. Some measurements have multiple synonymous terms. This is due to the diversity of hydrologic terms and communities. The user can choose the terms they prefer.
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/HydroMonitoringTerms_v3_vert.png "Recommended vocaulary terms related to water level")


## A Quick Look at the Templates
Screengrabs of color-coded versions of the templates are below and in the graphics folder. The csv version of the templates are included in the file list for use.

Data File template:
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/DataFile_template.PNG "Data File template")

Sensor File template (left side):
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/SensorFile_template_left.PNG "Sensor File template (left side)")

Sensor File template (right side):
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/SensorFile_template_right.PNG "Sensor File template (right side)")

Terminology File template:
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/TerminologyFile_template.PNG "Terminology File template")


## Licensing Information

## Funding and acknowledgements

## Recommended citation
