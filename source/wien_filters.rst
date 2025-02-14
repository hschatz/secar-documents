 
Wien Filters
============ 

Fernando Montes and Ken Schrock already know how to operate the Wien filters of SECAR, so I will not bother write the instructions here. One has to have special permission to operate these devices, which comes with training given by Fernando and Ken.

a few things I would like to add are discussed in the following:

- If you need to increase the allowed current on any electrode, make sure you first set the "High Current" to the desired :code:`I Setpoint + 10`. This will ensure that this "High Current" is not reached. In other words, it should always be 10 A higher than the set point for current. Otherwise, if "High Current" is smaller than the set point for current, it will interefer with how high the current is allowed to reach by the PLC.

- The :code:`DVDT` set point needs to be chosen wisely. The :code:`DVDT MAX` reading is the highest recorded value since the last "reset" (button below the :code:`DVDT MAX` reading) to help gauge where to set the number. If the PLC scan time is 10 ms (for example), and the voltage drops 5 kV between PLC scans, then :code:`DVDT` would be :math:`- 500000`. So, basically it counts any sudden drops in voltage as an arc. 5 of these arcs will turn the HV power supply OFF.

- Operation of the vacuum systems and vacuum interlocks of both Wien filters have changed. Please refer to the :numref:`Wien_filters_vacuum` for the updates.
