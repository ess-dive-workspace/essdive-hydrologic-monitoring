# ESS-DIVE Hydrological Monitoring Reporting Format Instructions

### SCOPE 
* The ESS-DIVE Hydrologic Monitoring Reporting Format (RF) is intended for water level, temperature, electrical conductivity, specific conductance, dissolved oxygen, and pH data measured in situ using sensors deployed in water bodies. **The user can also include data from variables/parameters outside the scope.**
* This RF is designed to be flexible for each user’s needs. Aside from required template fields, the user should only populate their file with the template fields relevant to their data. **The user can also include other columns beyond what is specified in the templates.**
* This RF is designed to comply with other ESS-DIVE RFs, including the ESS-DIVE File Level Metadata (FLMD) and CSV RFs.  

### CONTENT
This Reporting Format includes the following 
* Two guidance documents
  * This **Instructions** file.
  * **[Recommended Vocabulary](HydroRF_RecommendedVocabulary.md)**: A file with recommended column headers for measured variables.
* Four templates for required files that are available as MS Excel spreadsheets with instructions and examples and as csv templates with no  guidance content. The user must save their final populated files as csv files.
  * **(1) [Data File template](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/templates/HydroRF_Template_DataFile.xlsx)**: A template for sensor data. 
  * **(2) [Installation Methods template](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/templates/HydroRF_Template_InstallationMethods.xlsx)**: A template for metadata about the installation (i.e., location, type of water body).
  * **(3) [File-Level Metadata template](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/templates/HydroRF_Template_FLMD.xlsx)**: A template for listing a file name and description for every file included in the dataset (requirement of FLMD RF). 
  * **(4) [Data Dictionary template](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/templates/HydroRF_Template_dd.xlsx)**: A template for defining information about column headers and other terms contained in any csv files from the dataset (requirement of FLMD RF).
    *  Users may choose to provide a single data dictionary to describe column headers provided across all files or create a separate data dictionary for each csv file.

### NAMING CONVENTION
* We strongly encourage users to put descriptive information in their data file names (e.g., site name, coordinates, or time period). 
* We recommend naming the Installation Methods file, FLMD file, and Data Dictionary csv files “InstallationMethods.csv”, “FLMD.csv”, and “dd.csv”, respectively.
  * If the user chooses to create separate data dictionary files for each csv  file, we recommend naming them the same as the data file with “_dd” appended (e.g., WellData.csv and WellData_dd.csv; RiverData.csv and RiverData_dd.csv).

### COLUMN HEADERS
* **Column headers must not contain spaces** and **must use only underscores** as special characters.
* **All column headers must be defined in a data dictionary file.** 
  * When possible, copy and paste definitions from the recommended vocabulary file and use the data dictionary template’s pre-populated definitions.
* **For the data file(s), recommended column headers for measured variables are listed in the recommended vocabulary file.** The user can choose to use non-recommended column headers in their data file(s) for measured variables.
* **The column headers for  the Installation Methods file, FLMD file, and Data Dictionary csv files listed in the templates must not be modified.** 
  * However, if an optional column header is not needed in the user’s file, the entire column can be omitted from the file. 
* In all file types, if the provided column headers do not capture all the needed information, the **user may choose to include additional columns not specified in the templates.** 

### EMPTY CELLS
* **Empty cells are not permitted.** They should be filled with missing value terms, which must be defined in the FLMD file. 
* The ESS-DIVE CSV RF recommends -9999 for missing numeric data and N/A for missing text. 

### FILE FORMAT
* Filled out templates from this RF should be saved as comma-separated (.csv) files.
* The data file template includes a series of metadata header rows before the row of typical column headers. The metadata header rows are required. 
 * **First header row** indicates the total number of header rows, including the first row that defines the number of header rows down to the final header row that lists the column headers before presenting the data values. 
 * **Second header row** indicates the format for the subsequent header rows, including the (1) column header, (2) units, (3) corresponding InstallationMethod_ID from the Installation Methods file, and (4) a free text Instrument_Summary (i.e., make, model). **Each one of these four sections of a header row is separated by a semicolon and space.**
 * **Subsequent header rows** present metadata about each column of measured/logged/calculated data by following the format defined in the second header row. They are not needed for columns that present other information (e.g., notes). If a header row does not have information for one of the four sections defined in the format from the second header row, ‘N/A’ should be written in the place of information rather than skipping one of the four  sections. 
 * The figure below provides an example with an explanation. 
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/Graphic_Instructions_HeaderRows.png "Example and explanation of data file metadata header rows")

### MULTIPLE SENSORS
* The user should populate one Installation Methods file and one FLMD file that applies to the whole dataset irrespective of the number of data files. 
* Data from multiple sensors can be organized in several different ways depending on the user’s needs: 
  * (1) **[Preferred option]** Data from each sensor can be in a separate data file; 
  * (2) Data from each sensor can be combined in the same file if the sensors are synced and have identical timestamps, thereby producing a single DateTime column. If a data file has the same variable more than once, a prefix, suffix, or other differentiating text must be added in the column headers; 
  * (3) Data from each sensor can be combined in a single variable column if the same variable was measured. In this case, the single DateTime column may have duplicate timestamps, and it is mandatory that the user distinguishes which rows belong to which sensor using either the notes column or by adding a user-defined column (e.g., Sensor_ID; Site_ID). 
  * Examples of the three approaches are described and illustrated below (metadata header rows are not shown):
    * Approach #1 **[Preferred option]**: Two sensors each with a separate data file with one column for pH.
    * Approach #2: Two sensors compiled in one data file with columns for pH_1 and pH_2.
    * Approach #3: Two sensors compiled in one data file with one column for pH and one column for Sensor_ID.
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/Graphic_Instructions_FileOrganization.png "Options for number and structure of files")

### ADDITIONAL CONTENT
* Users are encouraged to include raw data files, sensor specification PDFs from manufacturers, code used for data collection or data processing, or links to relevant GitHub content. Users can also include documents describing sensor calibration, QA/QC, or other information.
* The RF does not provide specific guidance on formats of these additional files.

### WATER LEVEL TERMS
* See below for an illustration of some of the recommended vocabulary file’s terms. Some measurements have multiple synonymous terms. There is a great diversity of hydrologic terms and communities. These terms were chosen for their application across multiple disciplines and types of deployments and for their common use across data sources, repositories, and standards.  	 
![alt text](https://github.com/ess-dive-community/essdive-hydrologic-monitoring/blob/main/graphics/Graphic_RecommendedVocabulary_HydrologicTerms.png "Recommended vocaulary terms related to water level")
