# Rapid Test API
Documentation for the Rapid Test API

# Data dictionary

## Test fields:

- **tid** - Test ID (32-bit signed int) 
- **did0** - Device #1 ID (32-bit signed int) 
- **did1** - Device #2 ID (32-bit signed int) 
- **did2** - Device #3 ID (32-bit signed int) 
- **did3** - Device #4 ID (32-bit signed int)
- **result0** - Volumetric airflow result from Device #1 (float) a value of -1 indicates no result
- **result1** - Volumetric airflow result from Device #2 (float) a value of -1 indicates no result
- **result2** - Volumetric airflow result from Device #3 (float) a value of -1 indicates no result
- **result3** - Volumetric airflow result from Device #4 (float) a value of -1 indicates no result
- **each** - eACH result from test (float) a value of -1 indicates no eACH was calculated, eACH values will change during active tests
- **target** - Target airflow per person
- **start** - (UTC Timezone datetime)
- **background_end** - (UTC Timezone datetime)
- **diffusion_end** - (UTC Timezone datetime)
- **settling_end** - (UTC Timezone datetime)
- **stop** - (UTC Timezone datetime)
- **zone** -
- **email** -
- **hvac** -
- **configuration** -
- **notes** -
- **owner** -
- **org** -
- **status** -
- **errorcode** -
- **device[0-4]** - (Object)
- - **rid** -
  - **did** -
  - **tid** -
  - 

## Device fields:

- **did** - Device ID (32-bit signed int) 
- **iotid** - Serial number (string)
- **name** - Serial number by default, or assigned name (string) 
- **pm100aqi** - Last reading of AQI Value for PM10 (int 0-500) a value of -1 indicates no data available
- **pm25aqi** Last reading of AQI Value for PM2.5 (int 0-500) a value of -1 indicates no data available
- **pm10aqi** -  Last reading of AQI Value for PM1.0 (int 0-500) a value of -1 indicates no data available
- **vocaqi** - Last reading VOC AQI Value (int 0-500) a value of -1 indicates no data available 
- **temp** - Last reading Temperature \*C to 1 decimal (float) a value of -274 indicates no data available 
- **rh** - Last reading relative humidity 0-100% (float) a value of -1 indicates no data available 
- **co2** - Last reading CO2 PPM Parts per million to 2 decimals (float) a value of -1 indicates no data available 
- **lastupdate** - Last update from sensor (UTC Timezone datetime) 
- **created** - First online date (UTC Timezone datetime) 
- **location** - Assigned location ID (32-bit signed int) 
- **lat** - GPS latitude Coordinates for location (float)
- **lng** - GPS longitude Coordinates for location (float)
- **public** - Public flag enables fetching of data without login: 0=Private, 1=Public (boolean)

## Minute/Hour Average fields:

- **mid/hid** - minute/hour ID (32-bit signed int) 
- **did** - device ID (32-bit signed int) 
- **pc01** - PC Particle Count bin count for PC0.1 in #/Liter (32-bit signed int) 
- **pc03** -  PC Particle Count bin count for PC0.3 in #/Liter (32-bit signed int) 
- **pc05** -  PC Particle Count bin count for PC0.5 in #/Liter (32-bit signed int) 
- **pc10** -  PC Particle Count bin count for PC1.0 in #/Liter (32-bit signed int) 
- **pc25** -  PC Particle Count bin count for PC2.5 in #/Liter (32-bit signed int) 
- **pc50** -  PC Particle Count bin count for PC5.0 in #/Liter (32-bit signed int) 
- **pc100** - PC Particle Count bin count for PC10.0 in #/Liter (32-bit signed int) 
- **pm01** - PM Particle Mass Value for bin PM0.1 in ug/m3 (float) 
- **pm03** - PM Particle Mass Value for bin PM0.3 in ug/m3 (float) 
- **pm05** - PM Particle Mass Value for bin PM0.5 in ug/m3 (float) 
- **pm10** - PM Particle Mass Value for bin PM1.0 in ug/m3 (float) 
- **pm25** - PM Particle Mass Value for bin PM2.5 in ug/m3 (float) 
- **pm50** - PM Particle Mass Value for bin PM5 in ug/m3 (float) 
- **pm100** - PM Particle Mass Value for bin PM10 in ug/m3 (float) 
- **temp** - Temperature in \*C to 1 decimal (float)   a value of -274 indicates no data available 
- **rh** - Relative Humidity in % to 1 decimal (float) a value of -1 indicates no data available 
- **atm** - Atmospheric Pressure in hPa hecto Pascals to 2 decimals (float) a value of -1 indicates no data available 
- **vocaqi** - Volatile organic compounds AQI score 0-400 (32-bit signed int) a value of -1 indicates no data available 
- **vocppm** - Volatile organic compounds parts per million to 2 decimals (float) a value of -1 indicates no data available 
- **gasest** - Future Use as Gas Estimate: 1=true, false=0 (float) a value of -1 indicates no data available 
- **co2** - CO2 Gas Estimate in parts per million to 2 decimals (float) a value of -1 indicates no data available 
- **location** - location ID (32-bit signed int) a value of -1 indicates no data available 
- **time** - Timestamp of readings in UTC Timezone (datetime) 

## Event fields:

- **eid** - event ID (32-bit signed int) 
- **did** - device ID (32-bit signed int) 
- **type** - event type (string) 
- **time** - event timestamps in UTC Timezone (datetime) 
