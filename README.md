# HVAC_diagnosis

Identification and diagnosis of a chiller system using data analysis and visualisation, with analysis.

## Instructions

An example of the data for one of the chiller systems we are monitoring is provided in data_dump.csv. Chiller systems provide cooling via chilled water.

This chiller system has the symptom of "low chilled water delta T".  That is the chilled water supply and chilled water return temperature differences are small (less than 3 Degree Celsius).

Chilled Water Supply Temp: CHWS_Temp
Chilled Water Return Temp: CHWR_Temp

1. Please consider the readings when the chiller is on (when Comp_Power > 10).
2. Each of the 4 chillers (ACPC 1 to 4) would have their own temperature and power sensors, i.e.: ACPC-XCHWS_Temp, ACPC-XCHWR_Temp, ACPC-XComp_Power
3. (optional) You might also consider the flow rate of chilled water flowing through each chiller.

## ANALYSIS

###Chiller Temperature Difference between supply and return:

  • Each chiller’s Delta T is below 3°C for some of the operating time in all 4 chillers, indicating that none of the chillers achieve a consistently sufficient temperature difference between the supply and return temperatures. This aligns with the symptom of “low chilled water delta T”.
  
  • There are a few outliers in Delta T data for each chiller, suggesting occasional deviations from normal operating conditions.
  
  • Delta T for each chiller exhibit some variability over time but there are no obvious trends indicating a consistent increase or decrease over time.

  
Prioritisation:
  • ACPC1 has the lowest mean temperature difference between supply and return which is below the 3 degrees threshold, followed by ACPC4 and ACPC2 mean temperature differences which are also below the 3 degrees threshold, and then ACPC3 mean temperature difference which is above the 3 degrees threshold.
  
  • ACPC1 has the highest percentage of its temperature difference datapoints beneath the 3 degrees threshold, and so investigation into this chiller should be prioritised, followed by ACPC4, ACPC2, and ACPC3. This aligns with the mean temperature difference prioritisation and mean flow rate prioritisation (detailed below).

###Chiller Flow Rates:

  • The flow rates for each chiller exhibit some variability over time but there are no obvious trends indicating a consistent increase or decrease over time.
  
  • There are a few outliers in the Flow Rate data for each chiller, suggesting occasional deviations from normal operating conditions.

  
Prioritisation:
  • ACPC1 has the lowest mean flow rate, followed by ACPC4, ACPC2, and ACPC3. This means that ACPC1 could struggle the most to achieve optimal temperature differences perhaps due to restrictions or inefficiencies in the system that need to be addressed. Therefore, investigation into APC1 should be prioritised, followed by ACPC4, ACPC2 and ACPC3. This aligns with the mean temperature difference prioritisation and prioritisation based on the percentage of datapoints beneath 3 degrees (detailed above).
  

*Recommendation: Prioritise investigation into ACPC1 due to this chiller having the lowest mean flow rate, the lowest mean temperature difference between supply and return, and the highest percentage of its temperature difference datapoints beneath the 3 degrees threshold.*

