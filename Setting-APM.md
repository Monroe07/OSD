Setting APM to communicate with MinimOSD-Extra
There are a few requirements that have to be met, in order to be able to use MinimOSD-Extra.

The simplest way is to press the MinimOSD button in Mission Planner.

The manual method is below:

You need to have the data stream rates configured correctly. To do so, connect to Mission Planner. Go to configuration. Locate EEPROM parameters and verify that you have the following parameters configured as here;

SERIAL1_BAUD, 57 (telemetry output at 57600)

SR1_EXT_STAT, 2 ( 2hz for waypoints, GPS raw, fence data, current waypoint, etc)

SR1_EXTRA1, 5 ( 5hz for attitude and simulation state)

SR1_EXTRA2, 2 ( 2hz for VFR_Hud data )

SR1_EXTRA3, 3 ( 3hz for AHRS, Hardware Status, Wind )

SR1_POSITION, 2 ( 2hz for location data )

SR1_RAW_SENS, 2 ( 2hz for raw imu sensor data )

SR1_RC_CHAN, 5 ( 5hz for radio input or radio output data )

If you fly copter than you also need to set SR0 also:

SR0_EXT_STAT, 2

SR0_EXTRA1, 5

SR0_EXTRA2, 2

SR0_EXTRA3, 3

SR0_POSITION, 2

SR0_RAW_SENS, 2

SR0_RC_CHAN, 5

Change accordingly and save the parameters to APM.

If you follow this steps, MinimOSD-Extra should work fine!