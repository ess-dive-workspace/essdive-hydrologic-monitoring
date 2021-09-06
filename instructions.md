# ESS-DIVE Hydrological Monitoring Reporting Format Instructions

#### SCOPE 
* The ESS-DIVE Hydrologic Monitoring Reporting Format (RF) is intended for water level, temperature, electrical conductivity, specific conductance, dissolved oxygen, and pH data measured in situ using sensors deployed in water bodies. **The user can also include data from variables/parameters outside the scope.**
* This RF is designed to be flexible for each user’s needs. Aside from required template fields, the user should only populate their file with the template fields relevant to their data. **The user can also include other columns beyond what is specified in the templates.**
* This RF is designed to comply with other ESS-DIVE RFs, including the ESS-DIVE File Level Metadata (FLMD) and CSV RFs.  

#### CONTENT - This Reporting Format includes the following 
* Two guidance documents
  * This Instructions file.
  * Recommended vocabulary: A file with recommended column headers for measured variables.
* Four templates for required files that are available as MS Excel spreadsheets with instructions and examples and as csv templates with no  guidance content. The user must save their final populated files as csv files.
  * (1) Data File template: A template for sensor data. 
  * (2) Installation Methods template: A template for metadata about the installation (i.e., location, type of water body).
  * (3) File-Level Metadata template: A template for listing a file name and description for every file included in the dataset (requirement of FLMD RF). 
  * (4) Data Dictionary template: A template for defining information about column headers and other terms contained in any csv files from the dataset (requirement of FLMD RF).
    *  Users may choose to provide a single data dictionary to describe column headers provided across all files or create a separate data dictionary for each csv file.

#### NAMING CONVENTION
* We strongly encourage users to put descriptive information in their data file names (e.g., site name, coordinates, or time period). 
* We recommend naming the Installation Methods file, FLMD file, and Data Dictionary csv files “InstallationMethods.csv”, “FLMD.csv”, and “dd.csv”, respectively.
  * If the user chooses to create separate data dictionary files for each csv  file, we recommend naming them the same as the data file with “_dd” appended (e.g., WellData.csv and WellData_dd.csv; RiverData.csv and RiverData_dd.csv).

#### COLUMN HEADERS
* **Column headers must not contain spaces** and **must use only underscores** as special characters.
* **All column headers must be defined in a data dictionary file.** 
  * When possible, copy and paste definitions from the recommended vocabulary file and use the data dictionary template’s pre-populated definitions.
* **For the data file(s), recommended column headers for measured variables are listed in the recommended vocabulary file.** The user can choose to use non-recommended column headers in their data file(s) for measured variables.
* **The column headers for  the Installation Methods file, FLMD file, and Data Dictionary csv files listed in the templates must not be modified.** 
  * However, if an optional column header is not needed in the user’s file, the entire column can be omitted from the file. 
* In all file types, if the provided column headers do not capture all the needed information, the **user may choose to include additional columns not specified in the templates.** 





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
