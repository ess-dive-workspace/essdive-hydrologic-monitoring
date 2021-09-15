# Hydrologic Monitoring Reporting Format Recommended Vocabulary

Guidance: The Reporting Format recommends using the column headers listed below to name the variable and parameter columns in your data files. The definitions can be copy and pasted directly from this file into your data dictionary file(s) after replacing words in brackets and removing the brackets. Units can be pasted directly into your data dictionary file(s) and in the required metadata header rows of your data files. If your needed units are not listed here, you can find more units at http://vocabulary.odm2.org/units/ and http://qudt.org/2.1/vocab/unit. The recommended format for units is to write out the full unit and replace any spaces with underscores. See the Reporting Format Instructions document for a graphic illustrating most water level terms listed here. See http://vocabulary.odm2.org/variablename/ for more variable names. If you use terms from the ODM2 vocabulary, the Reporting Format recommends using underscores for spaces instead of camel case.

## Recommended Column Headers
[Depth_To_Water](#depth_to_water) | [Gage_Height](#gage_height) | [Sensor_Depth](#sensor_depth) | [Sensor_Elevation](#sensor_elevation) | [Sensor_Pressure_Unvented](#sensor_pressure_unvented) [Sensor_Pressure_Vented](#sensor_pressure_vented) | [Water_Depth](#water_depth) | [Water_Surface_Elevation](#water_surface_elevation) | [Electrical_Conductivity](#electrical_conductivity) | [Specific_Conductance](#specific_conductance) | [Dissolved_Oxygen](#dissolved_oxygen) | [Dissolved_Oxygen_Saturation](#dissolved_dxygen_saturation) | [pH](#pH) | [Water_Temperature](#water_temperature) 


---


### Depth_To_Water  
|Recommended_Column_Header|Depth_To_Water|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Vertical distance from [the chosen datum or reference point **out** of the water body] down to the water surface.|
|**Unit**|meters or centimeters|
|**Notes**|Replace the bracketed text to specify the chosen reference point and remove brackets. A use case for this measurement is lowering a sensor from the top of a well casing down to the water surface. In this use case, the definition would be "Vertical distance from the top of well casing down to the water surface."|

### Gage_Height  
|Recommended_Column_Header|Gage_Height|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Vertical distance from [the chosen datum or reference point **in** the water body] up to the water surface.|
|**Unit**|meters or centimeters|
|**Notes**|Replace the bracketed text to specify the chosen reference point if known and remove brackets. A common reference point is the streambed. Gage height is the preferred term over gauge height and stage height. Water level and stage are ambiguous and should be avoided.|

### Sensor_Depth  
|Recommended_Column_Header|Sensor_Depth|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Vertical distance from the sensor up to [the chosen datum or reference point above the sensor].|
|**Unit**|meters or centimeters|
|**Notes**|Replace the bracketed text to specify the reference point (e.g., water surface, top of well casing) and remove brackets. A use case for this measurement is lowering a sensor from a lake surface down to specific water depths to capture stratification. In this use case, the definition would be "Vertical distance from the sensor up to the water surface."|

### Sensor_Elevation  
|Recommended_Column_Header|Sensor_Elevation|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Elevation at which the sensor records a measurement.|
|**Unit**|meters_above_mean_sea_level_NAVD88|
|**Notes**|Note that this is elevation of the sensor not the water. The vertical datum must be defined in the data dictionary file's Unit field. NAVD88 is preferred.  A use case for this measurement is lowering a sensor from a lake surface down to specific water depths to capture stratification.|

### Sensor_Pressure_Unvented  
|Recommended_Column_Header|Sensor_Pressure_Unvented|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Absolute pressure exerted by the water column and atmosphere above the sensor.|
|**Unit**|kilopascals or meters_of_H2O|
|**Notes**|An unvented pressure sensor that has not been corrected for barometric pressure measures total or absolute pressure. Suggest noting the sensor is unvented in the Instrument_Summary field of the required metadata header rows in the data file(s).|

### Sensor_Pressure_Vented  
|Recommended_Column_Header|Sensor_Pressure_Vented|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Pressure exerted by the water column above the sensor relative to atmospheric or ambient pressure.|
|**Unit**|kilopascals or meters_of_H2O|
|**Notes**|A vented pressure sensor measures only the pressure exerted from the water column and does not need to be corrected for barometric pressure. Suggest noting the sensor is vented in the Instrument_Summary field of the required metadata header rows in the data file(s).|

### Water_Depth  
|Recommended_Column_Header|Water_Depth|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Vertical distance between the water surface and the bottom of the water body at a specific location.|
|**Unit**|meters or centimeters|
|**Notes**|This measurement refers to the full water column height at a given location.|

### Water_Surface_Elevation  
|Recommended_Column_Header|Water_Surface_Elevation|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Elevation of the surface of the water body.|
|**Unit**|meters_above_mean_sea_level_NAVD88|
|**Notes**|This measurement refers to the elevation of the surface of any type of water body, including groundwater wells etc. The vertical datum must be defined in the data dictionary file's Unit field. NAVD88 is preferred.|

### Electrical_Conductivity  
|Recommended_Column_Header|Electrical_Conductivity|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Electrical conductivity.|
|**Unit**|microsiemens_per_centimeter or millisiemens_per_centimeter|
|**Notes**|It is recommended to describe the location the measurement was taken (e.g., 50 percent water column depth) in the InstallationMethod_Description field in the Installation Methods file.|

### Specific_Conductance  
|Recommended_Column_Header|Specific_Conductance|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Specific conductance. Electrical conductivity at 25 degrees celsius.|
|**Unit**|microsiemens_per_centimeter or millisiemens_per_centimeter|
|**Notes**|It is recommended to describe the location the measurement was taken (e.g., 50 percent water column depth) in the InstallationMethod_Description field in the Installation Methods file.|

### Dissolved_Oxygen  
|Recommended_Column_Header|Dissolved_Oxygen|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Dissolved oxygen.|
|**Unit**|milligrams_per_liter|
|**Notes**|It is recommended to describe the location the measurement was taken (e.g., 50 percent water column depth) in the InstallationMethod_Description field in the Installation Methods file.|

### Dissolved_Oxygen_Saturation  
|Recommended_Column_Header|Dissolved_Oxygen_Saturation|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Dissolved oxygen.|
|**Unit**|percent_saturation|
|**Notes**|It is recommended to describe the location the measurement was taken (e.g., 50 percent water column depth) in the InstallationMethod_Description field in the Installation Methods file.|

### pH  
|Recommended_Column_Header|pH|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|pH.|
|**Unit**|pH|
|**Notes**|It is recommended to describe the location the measurement was taken (e.g., 50 percent water column depth) in the InstallationMethod_Description field in the Installation Methods file.|

### Water_Temperature  
|Recommended_Column_Header|Water_Temperature|
|:----------------------------------------------------|:----------------------------------------------------|
|**Definition**|Water temperature.|
|**Unit**|degree_celsius|
|**Notes**|If the measurement site was variably inundated, "Temperature" may be more appropriate than "Water_Temperature". It is recommended to describe the location the measurement was taken (e.g., 50 percent water column depth) in the InstallationMethod_Description field in the Installation Methods file.|



