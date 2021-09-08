# Hydrologic Monitoring Reporting Format Guide

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
|**required_recommended_or_optional**|Required|
|**file**|Data File|
|**description**|Date/time of measurement.|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Mixed|
|**additional.instructions**|Time zone must not change in the middle of the file (i.e., no switch to daylight savings). Time must be in 24 hour format. UTC offset must be reported in a header row in each data file. Date and time can be in separate columns if preferred. DateTime_Start column and an DateTime_End column can be used rather than a single DateTime column if applicable. If time is not relevant to the research, Date alone can be specified. If the measurement is taken over a period of time or is an average of multiple values, the data dictionary should indicate what time has been provided (i.e., "the time stamp indicates the start of the 5 minute averaging period").|
|**examples**|2020-03-25 13:25|  

### Latitude
|Metadata_Element|Latitude|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Data File or Installation Methods|
|**description**|Geographic location (latitude)|
|**format**|Decimal degrees WGS84|
|**format_required_or_recommended**|Required|
|**additional.instructions**|North/South and East/West should be indicated with positive and negative values rather than letters.|
|**examples**|43.319487|

### Longitude
|Metadata_Element|Longitude|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Data File or Installation Methods|
|**description**|Geographic location (longitude)|
|**format**|Decimal degrees WGS84|
|**format_required_or_recommended**|Required|
|**additional.instructions**|North/South and East/West should be indicated with positive and negative values rather than letters.|
|**examples**|-119.259388|

### InstallationMethod_ID 
|Metadata_Element|InstallationMethod_ID|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Installation Methods|
|**description**|Unique user-determined ID for a method described in InstallationMethod_Description. Corresponds to Data File header row section "InstallationMethod_ID"|
|**format**|Alphanumeric|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|May be listed as a column in data file(s) also.|
|**examples**|DO_012|

### InstallationMethod_Description
|Metadata_Element|InstallationMethod_Description|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Installation Methods|
|**description**|Free text field. May contain accuracy, range, measurement interval, point to document about calibration, and/or point to document about QAQC.|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**examples**|Sensor deployed to fixed location from top of well casing to 10 m depth. Top of well screen is at 30 m depth from top of casing and extends down 3 m.|




## Optional Fields

### DataFlag
|Metadata_Element|DataFlag|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Data File|
|**description**|Indicator of flagged data|
|**format**|Alphanumeric code defined by user in terminology csv|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Flags to indicate additional information about the measurement. Must be defined in the data dictionary. The definition may indicate that flagged values should not be used or why to use them with particular information in mind. If values are missing, it is strongly suggested that a data flag explain why they are missing (e.g., value was below reported range of the sensor; sensor component had expired; sensor was out of the water for maintenance). A single data flag column can be used, or columns for each parameter can be used but must have characters appended to the column header to differentiate the columns.|
|**examples**|DataFlag_01|

### Notes
|Metadata_Element|Notes|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Data File|
|**description**|Any notes the user would like to include.|
|**format**|Free text|
|**additional.instructions**|Can include field conditions (cloud cover, weather), sensor information, field activities, etc.|
|**examples**|Collected samples for lab analyses|

### Depth
|Metadata_Element|Depth|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Depth at which the sensor is deployed|
|**format**|Numeric|
|**format_required_or_recommended**|Required|
|**examples**|10.5|

### Depth_Unit
|Metadata_Element|Depth_Unit|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Unit for depth measurement|
|**format**|Text|
|**examples**|centimeters|

### Depth_Reference
|Metadata_Element|Depth_Reference|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Reference for depth value|
|**format**|Text|
|**examples**|Below ground surface|

### Elevation
|Metadata_Element|Elevation|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Elevation at which the sensor is deployed|
|**format**|Numeric|
|**format_required_or_recommended**|Required|
|**examples**|104.5|

### Elevation_Unit
|Metadata_Element|Elevation_Unit|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Unit for elevation measurement|
|**format**|Text|
|**examples**|meters|

### Elevation_Reference
|Metadata_Element|Elevation_Reference|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Reference datum for elevation value|
|**format**|Text|
|**examples**|Above mean sea level (NAVD88)|

### Site_ID
|Metadata_Element|SiteID|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|ID of site|
|**format**|Alphanumeric|
|**examples**|SWS-1|

### Site_Name
|Metadata_Element|SiteName|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Full name of site|
|**format**|Text|
|**examples**|Hanford 300 Area|

### Water_Name
|Metadata_Element|WaterName|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Installation Methods|
|**description**|Full name of water body|
|**format**|Text|
|**examples**|Columbia River|

### Site_Type
|Metadata_Element|Site_Type|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Installation Methods|
|**description**|Water body type or local environmental context in which sensor was deployed/installed (controlled vocabulary)|
|**format**|ENVO term and code pasted from website (https://www.ebi.ac.uk/ols/ontologies/envo)|
|**format_required_or_recommended**|Required|
|**additional.instructions**|One or two word description of the water body in which the sensor was deployed. Required to use ENVO ontology (https://www.ebi.ac.uk/ols/ontologies/envo) and choose the most specific term possible. Common ENVO terms include fresh water river [ENVO:01000297]; lake [ENVO:00000020]; water well [ENVO:01000002]; groundwater [ENVO:01001004]; freshwater wetland ecosystem [ENVO:00000243]; and coastal wetland ecosystem [ENVO:00000230]. More that one term may be applicable. Pick the best fit for the system.|
|**examples**|fresh water river [ENVO:01000297]|

### Configuration
|Metadata_Element|Configuration|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Installation Methods|
|**description**|Description of the sensor deployment/installation configuration.|
|**format**|Term pasted from controlled vocabulary found in the additional instructions field|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Choose from the following controlled vocabulary: Well; Piezometer; Open water column; Buried in sediment or soil; Surface of sediment or soil; Engineered flow-through structure.|
|**examples**|Well|

### DateTime_Start
|Metadata_Element|DateTime_Start|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Date and time use of installation method ID information began|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**examples**|2020-03-25 13:25|

### DateTime_End
|Metadata_Element|DateTime_End|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Installation Methods|
|**description**|Date and time use of installation method ID information  ended|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**examples**|2020-03-25 15:45|

### UTC_Offset
|Metadata_Element|UTC_Offset|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Conditional|
|**file**|Installation Methods|
|**description**|UTC offset of DateTime_Start and DateTime_End.|
|**format**|+/-hh:mm|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Required field if DateTime_Start or DateTime_End fields are listed.|
|**examples**|-02:00|


