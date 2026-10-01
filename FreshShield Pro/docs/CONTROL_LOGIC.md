## Sensor Processing

For every sampling cycle:

1.  Read ethylene. 
2.  Read temperature. 
3.  Read relative humidity. 
4.  Check whether readings are valid. 
5.  Store readings. 
6.  Apply the validated control logic. 

## Control

The final implementation should use thresholds and control rules determined from the team's actual prototype testing.

Do not use unvalidated thresholds as experimental conclusions.

## Failure Handling

If a sensor reading is invalid:

-  Flag the reading. 
-  Avoid making unsafe control decisions. 
-  Continue monitoring other available sensors. 
-  Display an error/status message. 
-  Log the event where data logging is implemented. 

## Connectivity Failure

If Wi-Fi is unavailable:

-  Continue local ESP32 operation. 
-  Continue local sensor monitoring. 
-  Continue local control logic where safe. 
-  Resume IoT transmission when connectivity returns.
