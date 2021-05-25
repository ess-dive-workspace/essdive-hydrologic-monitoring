# ESS-DIVE Hydrological Monitoring Reporting Format Instructions

SCOPE - This reporting format is intended for water level, temperature, electrical conductivity, specific conductivity, dissolved oxygen, and pH measured in situ using sensors deployed in water bodies.

SUMMARY - This reporting format includes a **data file template, a location method metadata template, a sensor method metadata template,  a file level metadata template, and four data dictionary templates**. The reporting format is designed to be flexible for each user’s needs. If the user has measured parameters outside the scope or has other columns they would like to add to the data file or metadata templates, they should do so. Aside from required fields, the user should only populate their file with the fields relevant to their data. 

CONTENT - This reporting format includes 9 files in addition to the readme. The **data file template** is for sensor-based data collected in the field.  The **location method metadata and sensor method metadata templates** are for metadata about the sensor- and location-based methods used to generate the data. The **recommended vocabulary** file has recommended column headers for variables measured. In addition, there are **four files included to meet the requirements set forth in the ESS-DIVE File Level Metadata (FLMD) Reporting Format and the ESS-DIVE CSV Reporting Format**: an FLMD file, a data dictionary for the FLMD file, and data dictionaries for the data file template, the location metadata template, and the sensor metadata template. 

COLUMN HEADERS - **For the location and sensor metadata file, the FLMD file, and the data dictionary files,  column headers must match those listed in the templates. For the data file(s), column headers are recommended and listed in the recommended vocabulary file.** If non-recommended column header terms are chosen for the data file(s), they must have no spaces and only use underscores as special characters. **All column headers must be defined in the appropriate data dictionary files**. For the data file data dictionary, definitions should be copied and pasted from the recommended vocabulary file unless a term is not listed there. 

EMPTY CELLS - Empty cells are not permitted. They should be filled with missing value terms, which must be defined in the FLMD file (e.g., -9999 for numeric data and N/A for missing text). 	

FILE FORMAT - Files should be saved as comma-separated (.csv) files.

NAMING CONVENTION - We strongly encourage you to put descriptive information in the data file names (i.e., site name, coordinates, or time period). We recommend naming the location and sensor metadata files “LocationMethods.csv” and “SensorMethods.csv.” 

ADDITIONAL CONTENT - Users are encouraged to include raw data files, sensor specification PDFs from manufacturers, code used for data collection or data processing, or links to relevant GitHub content in their data packages. Users can also include documents describing sensor calibration, QA/QC, or other information.

MULTIPLE SENSORS - Data from multiple sensors can be handled in several different ways depending on the user’s needs. There should be one accompanying set of deployment metadata files (location and sensor) that apply to the whole data package irrespective of the number of data files: (1) **[Preferred option]** Data from each sensor can be in a separate data file; (2) Data from each sensor can be combined in the same file if the sensors are synced and have identical timestamps, thereby producing a single date/time column. If a data file has the same variable more than once, a prefix, suffix, or other differentiating text must be added in the column headers; (3) Data from each sensor can be combined in a single appropriate variable column if the same variable was measured. In this case, the single date/time column may have duplicate time stamps, and it is mandatory that the user distinguishes which rows belong to which sensor using either the methodDeviation column, notes column, or by adding a user-defined column (e.g., sensorID; siteID). In this format, time stamps may be repeated within the DateTime column. Examples of the three approaches are described below:
* Approach #1 **[Preferred option]**: One sensor with one data file with one column for WaterTemp.
* Approach #2: Two sensors compiled in one data file with columns for WaterTemp1 and WaterTemp2.
* Approach #3: Two sensors compiled in one data file with one column for WaterTemp and one column for sensorID.
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/FileStructures2.PNG "Options for number and structure of files")

WATER LEVEL TERMS - See the graphic below for a visual representation of the terms listed in the recommended vocabulary file. Some measurements have multiple synonymous terms. This is due to the diversity of hydrologic terms and communities. The user can choose the terms they prefer. 
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/HydroMonitoringTerms_v3_vert.png "Recommended vocaulary terms related to water level")
