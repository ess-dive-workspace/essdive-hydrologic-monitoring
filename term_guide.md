# Hydrologic Monitoring Reporting Format Guide

## Required Fields
[DateTime](#datetime) | [MethodID_Location](#methodid_location) | [MethodDescription_Location](#methoddescription_location) | [MethodID_Sensor](#methodid_sensor)   
[MethodDescription_Sensor](#methoddescription_sensor) | [DateTime_Start](#datetime_start) | [DateTime_End](#datetime_end) | [UTC_Offset](#utc_offset)   

## Optional Fields
[DataFlag](#dataflag) | [Notes](#notes) | [Latitude](#latitude) | [Longitude](#longitude) | [Depth_Reference](#depth_reference) | [Elevation](#elevation) |
[Elevation_Reference](#elevation_reference) | [DeploymentEnvironment](#deploymentenvironment) | [Deployment_Configuration](#deployment_configuration) | 
[Water_Name](#water_name) | [Site_Name](#site_name) | [Site_ID](#site_id) | [Instrument](#instrument)


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
|**additional.instructions**|Time zone must not change in the middle of the file (i.e., no switch to daylight savings). Time must be in 24 hour format. UTC offset must be reported in a header row in the data file. Date and time can be in separate columns if preferred. DateTime_Start column and an DateTime_End column can be used rather than a single DateTime column if applicable. If time is not relevant to the research, Date alone can be specified. If the measurement is taken over a period of time or is an average of multiple values, the data dictionary should indicate what time has been provided (i.e., "the time stamp indicates the start of the 5 minute averaging period").|
|**examples**|2020-03-25 13:25|  

### MethodID_Location
|Metadata_Element|MethodID_Location|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Location Methods|
|**description**| Unique user-determined ID for a method described in MethodDescription_Location. Corresponds to Data File header row section "MethodID_Location" |
|**format**|Alphanumeric|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Also listed as a required field in the Sensor Methods file to link between the Location Methods and Sensor Methods.|
|**examples**|Tow_01|

### MethodDescription_Location
|Metadata_Element|MethodDescription_Location|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Location Methods|
|**description**|Free text field. May contain description of deployment structure or environment.|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**examples**|Sensor towed from boat along the surface of the Columbia River. Latitude/longitude of each time point is reported in data file.|

### MethodID_Sensor  
|Metadata_Element|MethodID_Sensor|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor Methods|
|**description**|Unique user-determined ID for a method described in MethodDescription_Sensor. Corresponds to Data File header row section "MethodID_Sensor"  |
|**format**|Alphanumeric|
|**format_required_or_recommended**|Recommended|
|**examples**|DO_012|

### MethodDescription_Sensor
|Metadata_Element|MethodDescription_Sensor|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor Methods|
|**description**|Free text field. May contain accuracy, range, measurement interval, point to document about calibration, and/or point to document about QAQC.|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**examples**|Temperature and dissolved oxygen logged at 15 minute intervals. See DO_calib.txt for description of calibration protocol.|

### DateTime_Start
|Metadata_Element|DateTime_Start|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor Methods|
|**description**|Date and time sensor use began|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**examples**|2020-03-25 13:25|

### DateTime_End
|Metadata_Element|DateTime_End|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor Methods|
|**description**|Date and time sensor use ended|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**examples**|2020-03-25 15:45|

### UTC_Offset
|Metadata_Element|UTC_Offset|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor Methods|
|**description**|UTC offset of DateTime_Start and DateTime_End.|
|**format**|Numeric|
|**format_required_or_recommended**|Required|
|**examples**|-2|


## Optional Fields

### DataFlag
|Metadata_Element|DataFlag|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Data File|
|**description**|Indicator of flagged data|
|**format**|Alphanumeric code defined by user in terminology csv|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Flags to indicate additional information about the measurement. Must be defined in the data dictionary. The definition may indicate values should not be used or why to use them with particular information in mind . If values are missing, it is strongly suggested that a data flag explain why they are missing (e.g. value was below reported range of the sensor; value was above reported range of the sensor; sensor component had expired; sensor was out of the water for maintenance). A single data flag column can be used, or columns for each parameter can be used but must have characters appended to the column header to differentiate the columns.|
|**examples**|DataFlag_01|

### Notes
|Metadata_Element|Notes|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Data File|
|**description**|Any notes the user would like to include.|
|**format**|Free text|
|**additional.instructions**|Can include field conditions (cloud cover, weather)|
|**examples**|Collected samples for lab analyses|

### Latitude
|Metadata_Element|Latitude|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Location Methods|
|**description**|Geographic location (latitude)|
|**format**|Decimal degrees WGS84|
|**format_required_or_recommended**|Required|
|**additional.instructions**|North/South and East/West should be indicated with positive and negative values rather than letters.|
|**examples**|43.319487|

### Longitude
|Metadata_Element|Longitude|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Location Methods|
|**description**|Geographic location (longitude)|
|**format**|Decimal degrees WGS84|
|**format_required_or_recommended**|Required|
|**additional.instructions**|North/South and East/West should be indicated with positive and negative values rather than letters.|
|**examples**|-119.259388|

### Depth
|Metadata_Element|Depth|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Location Methods|
|**description**|Depth at which the sensor is deployed|
|**format**|Numeric|
|**format_required_or_recommended**|Required|
|**examples**|10.5|

### Depth_Reference
|Metadata_Element|Depth_Reference|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Location Methods|
|**description**|Reference for depth value|
|**format**|Text|
|**format_required_or_recommended**|Required|
|**examples**|Meters below ground surface|

### Elevation
|Metadata_Element|Elevation|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Location Methods|
|**description**|Elevation at which the sensor is deployed|
|**format**|Numeric|
|**format_required_or_recommended**|Required|
|**examples**|104.5|

### Elevation_Reference
|Metadata_Element|Elevation_Reference|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Location Methods|
|**description**|Reference for elevation value|
|**format**|Text|
|**format_required_or_recommended**|Required|
|**examples**|Meters above mean sea level (NAVD88)|

### DateTime_Start
|Metadata_Element|DateTime_Start|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Location Methods|
|**description**|Date and time location use began|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**examples**|2020-03-25 13:25|

### DateTime_End
|Metadata_Element|DateTime_End|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Location Methods|
|**description**|Date and time location use ended|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**examples**|2020-03-25 15:45|

### UTC_Offset
|Metadata_Element|UTC_Offset|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Conditional|
|**file**|Location Methods|
|**description**|UTC offset of DateTime_Start and DateTime_End.|
|**format**|Numeric|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Required field if either DateTime fields are listed.|
|**examples**|-2|

### DeploymentEnvironment
|Metadata_Element|DeploymentEnvironment|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Location Methods|
|**description**|Water body type or local environmental context in which sensor was deployed (controlled vocabulary)|
|**format**|ENVO term and code pasted from website (https://www.ebi.ac.uk/ols/ontologies/envo)|
|**format_required_or_recommended**|Required|
|**additional.instructions**|One or two word description of the water body in which the sensor was deployed. Required to use ENVO ontology (https://www.ebi.ac.uk/ols/ontologies/envo) and choose the most specific term possible. Common ENVO terms include fresh water river [ENVO:01000297]; lake [ENVO:00000020]; water well [ENVO:01000002]; groundwater [ENVO:01001004]; freshwater wetland ecosystem [ENVO:00000243]; and coastal wetland ecosystem [ENVO:00000230]. More that one term may be applicable. Pick the best fit for the system.|
|**examples**|fresh water river [ENVO:01000297]|

### Deployment_Configuration
|Metadata_Element|Deployment_Configuration|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Location Methods|
|**description**|Description of the sensor deployment configuration.|
|**format**|Term pasted from controlled vocabulary found in the additional instructions field|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Choose from the following controlled vocabulary: Well; Piezometer; Open water column; Buried in sediment or soil; Surface of sediment or soil; Engineered flow-through structure.|
|**examples**|Well|

### Water_Name
|Metadata_Element|WaterName|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Location Methods|
|**description**|Full name of water body|
|**format**|Text|
|**examples**|Columbia River|

### Site_Name
|Metadata_Element|SiteName|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Location Methods|
|**description**|Full name of site|
|**format**|Text|
|**examples**|Hanford 300 Area|

### Site_ID
|Metadata_Element|SiteID|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Optional|
|**file**|Location Methods|
|**description**|ID of site|
|**format**|Alphanumeric|
|**examples**|SWS-1|

### Instrument
|Metadata_Element|Instrument|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor Methods|
|**description**|Make and model of sensor. May include make and model of specific parameter probe on a multi-paramater sonde and make and model of the multi-parameter sonde. May include additional detail (serial number, software)|
|**format**|Text|
|**examples**|YSI EXO2 with EXO Optical Dissolved Oxygen Smart Sensor (599100-01)|


