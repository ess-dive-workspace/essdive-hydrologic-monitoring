# Hydrologic Monitoring Reporting Format Guide


[DateTime_[TimeZoneAcronym]](#datetime_[timezoneacronym])  
[DataFileName](#datafilename)  
[DataColumnHeader](#datacolumnheader)  

---

### DateTime_[TimeZoneAcronym]  
|Metadata_Element|DateTime_[TimeZoneAcronym]|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Data File|
|**description**|Date/time of measurement. UTC is strongly encouraged. Other time zones can be listed in a column for local time zone.|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Mixed|
|**additional.instructions**|Time zone must not change in the middle of the file (i.e., no switch to daylight savings). Time must be in 24 hour format. Time zone and/or UTC offset must be reported in the Terminology File and optionally in the column header. We strongly encourage times to be listed in UTC rather than local time An additional column can be added with local time if desired (see optional fields file). Date and time can be in separate columns if preferred. StartDateTime column and an EndDateTime column can be used rather than a single DateTime column if applicable. If time is not relevant to the research, date alone can be specified. If the measurement is taken over a period of time or is an average of multiple values, the Terminology File should indicate what time has been provided (i.e., "the time stamp indicates the start of the 5 minute averaging period").|
|**examples**|3/25/2020 13:25|  

### DataFileName  
|Metadata_Element|DataFileName|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor File|
|**description**|The names of the data file in which the term is used for the specified sensor information|
|**format**|File name and extension|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Full name and file extension of data file(s) that present data from a given sensor. Recommended to have no spaces in file name.  If multiple are listed they should be separated by a semicolon and a space. If too many to list individually, the cell can point to a list of file names contained in a separate file.|
|**examples**|Well_399-4-7_data.csv|  

### DataColumnHeader
|Metadata_Element|DataColumnHeader|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor File|
|**description**|Exact column headers from Data File for parameters that have an associated sensor metadata row|
|**format**|Column header pasted from Data File|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Allows Sensor File row to be linked with a specific column in Data File.|
|**examples**|WaterTemp_DegC|

|Metadata_Element|SensorMake|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor File|
|**description**|Sensor or multi-parameter sonde make|
|**format**|Text (from manufacturer)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|NA|
|**examples**|In-Situ|

|Metadata_Element|SenorModel|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor File|
|**description**|Sensor or multi-parameter sonde model|
|**format**|Text (from manufacturer)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|NA|
|**examples**|AquaTroll 200|

|Metadata_Element|Latitude_Decimal|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor File (or Data File)|
|**description**|Geographic location (latitude)|
|**format**|Decimal degrees WGS84|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Sensor latitude in decimal degrees and WGS84. North/South and East/West should be indicated with positive and negative values rather than letters.|
|**examples**|43.319487|

|Metadata_Element|Longitude_Decimal|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor File (or Data File)|
|**description**|Geographic location (longitude)|
|**format**|Decimal degrees WGS84|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Sensor longitude in decimal degrees and WGS84. North/South and East/West should be indicated with positive and negative values rather than letters.|
|**examples**|-119.259388|

|Metadata_Element|DeploymentEnvironment|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor File (or Data File)|
|**description**|Water body type or local environmental context in which sensor was deployed (controlled vocabulary)|
|**format**|ENVO term and code pasted from website (https://www.ebi.ac.uk/ols/ontologies/envo)|
|**format_required_or_recommended**|Required|
|**additional.instructions**|One or two word description of the water body in which the sensor was deployed. Required to use ENVO ontology (https://www.ebi.ac.uk/ols/ontologies/envo) and choose the most specific term possible. Common ENVO terms include fresh water river [ENVO:01000297]; lake [ENVO:00000020]; water well [ENVO:01000002]; groundwater [ENVO:01001004]; freshwater wetland ecosystem [ENVO:00000243]; and coastal wetland ecosystem [ENVO:00000230]. More that one term may be applicable. Pick the best fit for the system.|
|**examples**|fresh water river [ENVO:01000297]|

|Metadata_Element|SensorContext|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Sensor File (or Data File)|
|**description**|Description of sensor deployment context (controlled vocabulary)|
|**format**|Term pasted from controlled vocabulary found in the additional instructions field|
|**format_required_or_recommended**|Required|
|**additional.instructions**|One or two word description of the entity that allowed for the sensor's deployment. Required to use a term from the following list unless an accurate option is not listed: Well; Piezometer; Buoy; Stationary dock or platform; Vertically mobile dock or platform; Handheld stationary; Handheld walking; Boat anchored; Boat moving; Buried in sediment or soil; Surface of sediment or soil; Anchored in water column; Engineered flow-through structure.|
|**examples**|Well|

|Metadata_Element|Term|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Terminology File|
|**description**|Any terms from the Data File or Sensor File that require definition, including all column headers|
|**format**|Exact term used in Data or Sensor File|
|**format_required_or_recommended**|Required|
|**additional.instructions**|At a minimum, all column headers and the notation used for missing data must be listed. If data flags are used, they must also be listed. If the user has site codes, it is suggested they are listed and defined as well (e.g. CRU = Colorado River Upstream). Additional files in the data package can also be listed here (e.g., data logger script file name which is defined with the scripting language and description of content).|
|**examples**|SpC_uScm|

|Metadata_Element|TermType|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Terminology File|
|**description**|Describes type of term listed in terminology file|
|**format**|Chosen from two options: "Column header" or "Term"|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Controlled vocabulary|
|**examples**|Column header|

|Metadata_Element|Definition|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Terminology File|
|**description**|Definition of term in terminology file|
|**format**|Definition pasted from Recommended Vocabulary (if applicable) or free text|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Anything listed in terms column must be defined. If suggested terms are used, the definitions can be pasted from Recommended Vocabulary and modified as needed.|
|**examples**|Specific conductivity|

|Metadata_Element|Units|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Terminology File|
|**description**|Units for term in terminology file if the term is a measurement|
|**format**|Definition pasted from Recommended Vocabulary (if applicable) or free text|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Define the units for any measurement type. The words should be written out fully to reduce the likelihood of future confusion for data users (e.g., milligrams per liter rather than mg/L)|
|**examples**|Microsiemens per centimeter|

|Metadata_Element|RecommendedBaseTerm|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Required|
|**file**|Terminology File|
|**description**|The matching term recommended from this standard|
|**format**|Term pasted from Recommended Vocabulary that shares the exact definition of the term used|
|**format_required_or_recommended**|Required|
|**additional.instructions**|If the user chooses to use terms that differ from the suggested column headers or recommended vocabulary, but the chosen terms can be mapped directly onto recommended terms, then the user must indicate the mapping in this column. If a recommended term is used, the mapping column will have the identical term. If there is no recommended term that is identical in meaning to what was used, the mapping column will have a missing value code.|
|**examples**|SpC_uScm|

|Metadata_Element|LocalDateTime_[TimeZoneAcronym]|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Data File|
|**description**|Date/time of measurement in local time|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**additional.instructions**|If the user includes timestamps in UTC in the the "DateTime_[TimeZoneAcronym]" column they may also include local timestamps in another column. Time zone must never change in the middle of the file (i.e., no switch to daylight savings). Time must be in 24 hour format. Time zone must be reported in the Terminology File and optionally in the column header.|
|**examples**|3/25/2020 16:25|

|Metadata_Element|DataFlag|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Data File|
|**description**|Indicator of flagged data|
|**format**|Alphanumeric code defined by user in terminology csv|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Flags to indicate additional information about the measurement. Must be defined in the Terminology File (e.g. "SensorDepth_m was estimated based on cable length and the accuracy is approximately +/- 0.25 m"). The definition may indicate values should not be used or why to use them with particular information in mind . If values are missing, it is strongly suggested that a data flag explain why they are missing (e.g. value was below reported range of the sensor; value was above reported range of the sensor; sensor component had expired; sensor was out of the water for maintenance). A single data flag column can be used, or columns for each parameter can be used but must have characters appended to the column header to differentiate the columns.|
|**examples**|DataFlag_01|

|Metadata_Element|Notes|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Data File|
|**description**|Notes|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Any notes the user would like to include. Can include field conditions (cloud cover, weather)|
|**examples**|Collected samples for lab analyses|

|Metadata_Element|SensorID|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Data File and Sensor File|
|**description**|User-determined ID for the sensor or multi-parameter sonde|
|**format**|Alphanumeric code defined by user|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Can be used to link together data and sensor metadata. An example situation is if the data file has a single parameter (i.e., temperature) with data from many deployed sensors in the same column. In the Data File, the SensorID column differentiates which rows match with which sensors, and in the Sensor File, the SensorID column links those rows of data to the sensor metadata.|
|**examples**|ECA2_0034-D|

|Metadata_Element|SensorContextNotes|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Description of sensor deployment (adds detail to the required SensorContext field)|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Additional detail to supplement the SensorContext field from the Required Fields. This can include the object in which the sensor is deployed (e.g. well piezometer) or to which the sensor is attached (e.g. buoy dock) in relation to the water body or other environmental or engineered features. If the sensor is part of a shoreline flowthrough construction describe the general setup. If SensorContext is 'well' or 'piezometer,' then consider including measurements for well construction and screen location/elevation (i.e., casing length, depth to top of screen, depth to bottom of screen, stickup height, elevation of middle of screen). An installation diagram can also be added to the data package.|
|**examples**|Secured near the riverbed inside of a mid-channel piezometer that is screened to the river|

|Metadata_Element|WaterName|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Name of water body|
|**format**|Full name of water body (text)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Full name of water body|
|**examples**|Columbia River|

|Metadata_Element|SiteName|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Name of site|
|**format**|Full site name (text)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Any site name or identifier|
|**examples**|Hanford 300 Area|

|Metadata_Element|SiteID|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|ID of site|
|**format**|Alphanumeric site ID|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Any site ID or identifier|
|**examples**|SWS-1|

|Metadata_Element|StartDateTime_[TimeZoneAcronym]|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Date and time sensor use began|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Format must match timestamp format and timezone in Data File. If Data File had date and time in seperate columns they should be seperate for this field. Replace bracketed text with time zone acronym or UTC offset ("UTCminus2")|
|**examples**|3/25/2020 13:25|

|Metadata_Element|EndDateTime_[TimeZoneAcronym]|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Date and time sensor use ended|
|**format**|YYYY-MM-DD hh:mm:ss|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Format must match timestamp format and timezone in Data File. If Data File had date and time in seperate columns they should be seperate for this field. Replace bracketed text with time zone acronym or UTC offset ("UTCminus2")|
|**examples**|3/25/2020 15:45|

|Metadata_Element|RealClockTime_SensorClockTime|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Real clock time and sensor clock time at a single time point to allow for correction to real time if sensor clock is inaccurate|
|**format**|Real: [hh:mm:ss][timezone]. Sensor: [hh:mm:ss][timezone].|
|**format_required_or_recommended**|Required|
|**additional.instructions**|Time must be in 24-hour format and time zone must be listed and match time zone of sensor start/end fields..|
|**examples**|Real: 13:25:43 UTC. Sensor: 13:30:00 UTC.|

|Metadata_Element|ParameterMake|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Make of specific parameter probe on a multi-parameter sonde|
|**format**|Text (from manufacturer)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|NA|
|**examples**|YSI|

|Metadata_Element|ParameterModel|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Model of specific parameter probe on a multi-parameter sonde|
|**format**|Text (from manufacturer)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|NA|
|**examples**|EXO Optical Dissolved Oxygen Smart Sensor (599100-01)|

|Metadata_Element|SensorSN|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Sensor serial number|
|**format**|Text (from manufacturer)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Sensor serial number provided by manufacturer or permanently designated by researcher|
|**examples**|45123|

|Metadata_Element|SensorAccuracy|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Sensor accuracy|
|**format**|Text (from manufacturer)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Sensor accuracy according to manufacturer|
|**examples**|plus/minus 0.1%|

|Metadata_Element|SensorRange|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Sensor range|
|**format**|Text (from manufacturer)|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Sensor range according to manufacturer|
|**examples**|0-14.5psig (100kPa)|

|Metadata_Element|SensorCalibration|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Sensor calibration|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Description of calibration in a level of detail decided by the user. This field can be used to point to references, SOPs, links, file names within the data package, or other sources. It can also be used for a brief free text description. If the user followed the sensor manufacturer's recommended calibration, please state.|
|**examples**|See calib.txt in data package|

|Metadata_Element|DataQAQC|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|QAQC of data|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Description of QA/QC in a level of detail decided by the user. This field can be used to point to references, SOPs, links, file names within the data package, or other sources. It can also be used for a brief free text description.|
|**examples**|Removed values for periods when sensor was out of water|

|Metadata_Element|MeasurementInterval|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Interval of sensor measurements|
|**format**|Descriptor ([value/units or event type])|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Descriptors could include continuous, fixed interval, and event-generated interval. If the interval is event-generated, indicate the event type. If the interval is fixed, indicate the interval.|
|**examples**|Fixed interval (15 min)|

|Metadata_Element|Software|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Software version of sensor and/or sensor communication program|
|**format**|Text (from manufacturer)|
|**format_required_or_recommended**|Required|
|**additional.instructions**|NA|
|**examples**|Win-Situ 5|

|Metadata_Element|DataCombine|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Identify sensors that have data that can be combined with this sensor's data for analyses|
|**format**|Data file name, SensorID, or Make/Model/SerialNumber/StartDateTime/StopDateTime for any other sensors that have data that can be combined with this sensor's data for analyses|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|List other sensors that have data that can be used together with this sensor for analyses. The common case for this would be if two or more sensors are located in the same place at the same time. The format is suggested but the chosen format must have enough unique information that the data user cannot mistakenly pair sensors that should not be paired.|
|**examples**|PR_004|

|Metadata_Element|SensorNotes|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Sensor File|
|**description**|Notes about sensor|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|Relevant text about specific sensor or associated measurement values. This field can be used to point to references links file names within the data package or other sources.|
|**examples**|Water surface elevation (WE) is measured as pressure (m H2O) from a vented sensor and manually converted to WE using known reference elevation.|

|Metadata_Element|TermNotes|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Terminology File|
|**description**|Free text notes about term|
|**format**|Free text|
|**format_required_or_recommended**|Recommended|
|**additional.instructions**|NA|
|**examples**|Time stamp indicates the start of a 30 second averaging period|

|Metadata_Element|AssociatedFileNames|
|:----------------------------------------------------|:----------------------------------------------------|
|**required_recommended_or_optional**|Recommended|
|**file**|Terminology File|
|**description**|The names of the files in which the term is used|
|**format**|File name and extension|
|**format_required_or_recommended**|Required|
|**additional.instructions**|The names of the files in which the term is used. If multiple are listed they should be separated by a semicolon and a space. If too many to list individually, the cell can point to a list of file names contained in a separate file.|
|**examples**|Well_399-4_data.csv; Well_399-2.csv|
