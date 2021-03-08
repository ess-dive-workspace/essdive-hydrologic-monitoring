# Getting started with the ESS-DIVE Hydrological Monitoring Reporting Format
[This Reporting Format content is in draft form and incomplete.]
## About the Hydrological Monitoring Reporting Format
SCOPE - This reporting format is intended for water level, temperature, electrical conductivity, specific conductivity, dissolved oxygen, and pH measured in situ using sensors deployed in water bodies.

SUMMARY - This standard uses a **three file system to organize data, sensor metadata, and terminology metadata.** The reporting format is designed to be flexible for each user’s needs. If the user has measured parameters outside the scope or has other columns they would like to add, they should do so. Aside from required fields, the user should only populate their file with the fields relevant to their data. 

## Quickstart Guide for Hydrologic Monitoring Data and Metadata ESS-DIVE Reporting Format  
1 - **Read the Instructions file**  

2 - **Open the three templates (Data, Sensor, Terminology).** If you have more than one data file or more than one sensor, you have a few options for the total number of files. See the instructions file for details and a graphic depicting the options.
  
3 - **Open the Recommended Vocabulary File** for suggested column headers for your Data File. If you choose to use your own, the only allowed special characters are underscores and hyphens. No spaces are allowed.
  
4 - **Populate all required fields** in the templates and **populate optional fields as desired**. Note that two fields in the Sensor File and the Terminology File have controlled vocabularies. Exclude the optional columns you do not populate. No empty cells are permitted. 

### Summary of information to have ready before you start
**Find the full list of fields to populate in the Term Guide file**
| Required                                                                                       |
|:-----------------------------------------------------------------------------------------------|
| Name of data columns and files within the data package that contain data from the given sensor |
| Latitude of sensor in decimal degrees WGS84                                                    |
| Longitude of sensor in decimal degrees WGS84                                                   |
| Sensor make and model                                                                          |
| Description of sensor deployment setup (water body type, deployment structure)                 |
| Parameters measured and accompanying units                                                     |
  
  
| Recommended                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------|
| Name of water body                                                                                                       |
| Name of site                                                                                                             |
| Sensor ID                                                                                                                |
| Start and end date/time of deployment                                                                                    |
| Real clock time at a given point in time and concurrent sensor clock time                                                |
| Make and model of specific parameter probe on a multi-parameter sonde                                                    |
| Sensor serial number from manufacturer                                                                                   |
| Sensor accuracy  from manufacturer                                                                                       |
| Sensor range from manufacturer                                                                                           |
| Sensor calibration in brief or a document or reference to point to                                                       |
| Data QA/QC in brief or a document or reference to point to                                                               |
| Type of measurement interval of sensor (fixed, event-generated)                                                          |
| Software version of sensor and/or sensor communication program                                                           |
| Other sensors outputting data that can be combined with data from the given sensor (likely due to concurrent co-location)|
| Other notes to record about the sensor, data, or terminology used                                                        |



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


## How to contribute
This ESS-DIVE Hydrologic Monitoring Reporting Format is evolving and growing to meet the needs of the community. Feedback and new contributions are welcome. If you would like to suggest a change to the Reporting Format please submit a GitHub issue using one of the templates we provide.

If you have any questions about this reporting format, you can also directly email ESS-DIVE support at ess-dive-support@lbl.gov. Our issue templates were based on those used by Darwin Core (Darwin Core maintenance group, Biodiversity Information Standards (TDWG) (2014). Darwin Core. Zenodo. https://doi.org/10.5281/zenodo.592792)

## Licensing Information
This repository content is licensed for use under the CC BY 4.0 license (https://creativecommons.org/licenses/by/4.0/)

## Funding and acknowledgements
Funding for the development of ESS-DIVE Hydrologic Monitoring Reporting Format was provided by the U.S. Department of Energy, Office of Science, Office of Biological and Environmental Research, Climate and Environmental Science Division, Data Management program

## Recommended citation
