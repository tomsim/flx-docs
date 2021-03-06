VrrpVridState Object
=============================================================

*state/VrrpVrid*
------------------------------------

- Multiple objects of this type can exist in a system.

+--------------------+---------------+--------------------------------+-------------+------------------+
| **PARAMETER NAME** | **DATA TYPE** |        **DESCRIPTION**         | **DEFAULT** | **VALID VALUES** |
+--------------------+---------------+--------------------------------+-------------+------------------+
| IfIndex **[KEY]**  | int32         | Interface index for which VRRP | N/A         | N/A              |
|                    |               | state is requested             |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| VRID **[KEY]**     | int32         | Virtual Router's Unique        | N/A         | N/A              |
|                    |               | Identifier                     |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| LastAdverTx        | string        | Time when last advertisement   | N/A         | N/A              |
|                    |               | packet was send out            |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| AdverTx            | int32         | Total number of advertisement  | N/A         | N/A              |
|                    |               | packets send                   |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| LastAdverRx        | string        | Time when last advertisement   | N/A         | N/A              |
|                    |               | packet was received            |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| MasterIp           | string        | Ip Address of the Master VRRP  | N/A         | N/A              |
+--------------------+---------------+--------------------------------+-------------+------------------+
| PreviousState      | string        | Previous State of Local VRRP   | N/A         | N/A              |
+--------------------+---------------+--------------------------------+-------------+------------------+
| TransitionReason   | string        | Reason why we moved from       | N/A         | N/A              |
|                    |               | previous state -> current      |             |                  |
|                    |               | state                          |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| AdverRx            | int32         | Total number of advertisement  | N/A         | N/A              |
|                    |               | packets received               |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| CurrentState       | string        | Current State of Local VRRP    | N/A         | N/A              |
+--------------------+---------------+--------------------------------+-------------+------------------+



*OpxFlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/state/VrrpVrid
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/state/VrrpVrids?CurrentMarker=<x>&Count=<y>
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/VrrpVridState/<uuid>


*OpxFlexSwitch SDK API Supported:*
------------------------------------



- **GET**


::

	import sys
	import os
	from opxflexswitchV2 import OpxFlexSwitch

	if __name__ == '__main__':
		switchIP := "192.168.56.101"
		swtch = OpxFlexSwitch (switchIP, 8080)  # Instantiate object to talk to flexSwitch
		response, error = swtch.getVrrpVridState(IfIndex=ifindex, VRID=vrid)

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


- **GET By ID**


::

	import sys
	import os
	from opxflexswitchV2 import OpxFlexSwitch

	if __name__ == '__main__':
		switchIP := "192.168.56.101"
		swtch = OpxFlexSwitch (switchIP, 8080)  # Instantiate object to talk to flexSwitch
		response, error = swtch.getVrrpVridStateById(ObjectId=objectid)

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'




- **GET ALL**


::

	import sys
	import os
	from opxflexswitchV2 import OpxFlexSwitch

	if __name__ == '__main__':
		switchIP := "192.168.56.101"
		swtch = OpxFlexSwitch (switchIP, 8080)  # Instantiate object to talk to flexSwitch
		response, error = swtch.getAllVrrpVridStates()

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


