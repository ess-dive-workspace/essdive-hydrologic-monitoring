# Hydrologic Monitoring Reporting Format Term Guide

## Required Fields
[DateTime](#datetime) | [Latitude](#latitude) | [Longitude](#longitude) | [InstallationMethod_ID](#installationmethod_id) | [InstallationMethod_Description](#installationmethod_description) 

## Optional Fields
[DataFlag](#dataflag) | [Notes](#notes) | [Depth](#depth) | [Depth_Unit](#depth_unit) | [Depth_Reference](#depth_reference) | [Elevation](#elevation) |
[Elevation_Unit](#elevation_unit) |[Elevation_Reference](#elevation_reference) | [Site_ID](#site_id) | [Site_Name](#site_name) |[Water_Name](#water_name) |
[Site_Type](#site_type) | [Configuration](#configuration) | [DateTime_Start](#datetime_start) | [DateTime_End](#datetime_end) | [UTC_Offset](#utc_offset) 


---
## Required Fields

### DateTime  
|Metadata_Element|DateTime|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Required|
|**File**|Data File|
|**Description**|Date and time of measurement formatted as YYYY-MM-DD hh-mm-ss completed to the known precision.|
|**Format**|YYYY-MM-DD hh:mm:ss|
|**Format required or recommended**|Required|
|**Additional Instructions**|Time zone must not change in the middle of the file (i.e., no switch to daylight savings). Time must be in 24-hour format. UTC offset must be reported in a header row in each data file. Date and time can be in separate columns if preferred. DateTime_Start column and a DateTime_End column can be used rather than a single DateTime column if applicable. If time is not relevant to the research, Date alone can be specified. If the measurement is taken over a period of time or is an average of multiple values, the data dictionary should indicate what time has been provided (i.e., "the time stamp indicates the start of the 5 minute averaging period").|
|**Examples**|2020-03-25 13:25|  

### Latitude
|Metadata_Element|Latitude|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Required|
|**File**|Data File or Installation Methods|
|**Description**|Geographic location (latitude)|
|**Format**|Decimal degrees WGS84|
|**Format required or recommended**|Required|
|**Additional Instructions**|North/South and East/West should be indicated with positive and negative values rather than letters.|
|**Examples**|43.319487|

### Longitude
|Metadata_Element|Longitude|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Required|
|**File**|Data File or Installation Methods|
|**Description**|Geographic location (longitude)|
|**Format**|Decimal degrees WGS84|
|**Format required or recommended**|Required|
|**Additional Instructions**|North/South and East/West should be indicated with positive and negative values rather than letters.|
|**Examples**|-119.259388|

### InstallationMethod_ID 
|Metadata_Element|InstallationMethod_ID|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Required|
|**File**|Installation Methods|
|**Description**|Unique user-determined ID for a method described in InstallationMethod_Description. Corresponds to Data File header row section "InstallationMethod_ID"|
|**Format**|Alphanumeric|
|**Format required or recommended**|Recommended|
|**Additional Instructions**|May be listed as a column in data file(s) also.|
|**Examples**|DO_012|

### InstallationMethod_Description
|Metadata_Element|InstallationMethod_Description|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Required|
|**File**|Installation Methods|
|**Description**|Free text field that provides a brief description of the approach to sensor installation or deployment. May contain a description of installation/deployment structure or environment.|
|**Format**|Free text|
|**Format required or recommended**|Recommended|
|**Examples**|Sensor deployed to fixed location from top of well casing to 10 m depth. Top of well screen is at 30 m depth from top of casing and extends down 3 m.|




## Optional Fields

### DataFlag
|Metadata_Element|DataFlag|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Recommended|
|**File**|Data File|
|**Description**|Indicator of flagged data|
|**Format**|Alphanumeric code (defined by user in data dictionary file or a separate file).|
|**Format required or recommended**|Required|
|**Additional Instructions**|Flags to indicate additional information about the measurement. Must be defined in the data dictionary or a separate file. The definition may indicate that flagged values should not be used or why to use them with particular information in mind. If values are missing, it is strongly suggested that a data flag explain why they are missing (e.g., value was below reported range of the sensor; sensor component had expired; sensor was out of the water for maintenance). Flags can be defined in such a way that they refer to one variable or more than one. A single data flag column can be used, or columns for each parameter can be used but must have characters appended to the column header to differentiate the columns.|
|**Examples**|DataFlag_01|

### Notes
|Metadata_Element|Notes|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Recommended|
|**File**|Data File|
|**Description**|Any notes the user would like to include.|
|**Format**|Free text|
|**Additional Instructions**|Can include field conditions (cloud cover, weather), sensor information, field activities, etc. If the installation method deviates from the ID written in the InstallationMethod_ID header row section, the new InstallationMethod_ID pertaining to the deviation can be put in this column if the information is not captured elsewhere.|
|**Examples**|Collected samples for lab analyses|

### Depth
|Metadata_Element|Depth|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Depth at which the sensor is deployed|
|**Format**|Numeric|
|**Format required or recommended**|Required|
|**Examples**|10.5|

### Depth_Unit
|Metadata_Element|Depth_Unit|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Unit for depth measurement|
|**Rormat**|Text|
|**Examples**|centimeters|

### Depth_Reference
|Metadata_Element|Depth_Reference|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Reference for depth value|
|**Format**|Text|
|**Examples**|Below ground surface|

### Elevation
|Metadata_Element|Elevation|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Elevation at which the sensor is deployed|
|**Format**|Numeric|
|**Format required or recommended**|Required|
|**Examples**|104.5|

### Elevation_Unit
|Metadata_Element|Elevation_Unit|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Unit for elevation measurement|
|**Format**|Text|
|**Examples**|meters|

### Elevation_Reference
|Metadata_Element|Elevation_Reference|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Reference datum for elevation value|
|**Format**|Text|
|**Examples**|Above mean sea level (NAVD88)|

### Site_ID
|Metadata_Element|SiteID|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|ID of site|
|**Format**|Alphanumeric|
|**Examples**|SWS-1|

### Site_Name
|Metadata_Element|SiteName|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Full name of site|
|**Format**|Text|
|**Examples**|Hanford 300 Area|

### Water_Name
|Metadata_Element|WaterName|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Recommended|
|**File**|Installation Methods|
|**Description**|Full name of water body|
|**Format**|Text|
|**Examples**|Columbia River|

### Site_Type
|Metadata_Element|Site_Type|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Recommended|
|**File**|Installation Methods|
|**Description**|Water body type or local environmental context in which sensor was deployed/installed (controlled vocabulary)|
|**Format**|ENVO term and code pasted from website (https://www.ebi.ac.uk/ols/ontologies/envo)|
|**Format required or recommended**|Required|
|**Additional Instructions**|One or two word description of the water body in which the sensor was deployed. Required to use ENVO ontology (https://www.ebi.ac.uk/ols/ontologies/envo) and choose the most specific term possible. Common ENVO terms include fresh water river [ENVO:01000297]; lake [ENVO:00000020]; water well [ENVO:01000002]; groundwater [ENVO:01001004]; freshwater wetland ecosystem [ENVO:00000243]; and coastal wetland ecosystem [ENVO:00000230]. More than one term may be applicable. Pick the best fit for the system.|
|**Examples**|fresh water river [ENVO:01000297]|

### Configuration
|Metadata_Element|Configuration|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Recommended|
|**File**|Installation Methods|
|**Description**|Description of the sensor deployment/installation configuration.|
|**Format**|Term pasted from controlled vocabulary found in the additional instructions field|
|**Format required or recommended**|Required|
|**Additional Instructions**|Choose from the following controlled vocabulary: Well; Piezometer; Open water column; Buried in sediment or soil; Surface of sediment or soil; Engineered flow-through structure.|
|**Examples**|Well|

### DateTime_Start
|Metadata_Element|DateTime_Start|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Date and time use of installation method ID information began|
|**Format**|YYYY-MM-DD hh:mm:ss|
|**Format required or recommended**|Required|
|**Examples**|2020-03-25 13:25|

### DateTime_End
|Metadata_Element|DateTime_End|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Optional|
|**File**|Installation Methods|
|**Description**|Date and time use of installation method ID information ended|
|**Format**|YYYY-MM-DD hh:mm:ss|
|**Format required or recommended**|Required|
|**Examples**|2020-03-25 15:45|

### UTC_Offset
|Metadata_Element|UTC_Offset|
|:----------------------------------------------------|:----------------------------------------------------|
|**Required recommended or optional**|Conditional|
|**File**|Installation Methods|
|**Description**|UTC offset of DateTime_Start and DateTime_End.|
|**Format**|+/-hh:mm|
|**Format required or recommended**|Required|
|**Additional Instructions**|Required field if DateTime_Start or DateTime_End fields are listed.|
|**Examples**|-02:00|


