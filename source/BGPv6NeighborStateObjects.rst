BGPv6NeighborState Object
=============================================================

*state/BGPv6Neighbor*
------------------------------------

- Multiple objects of this type can exist in a system.

+---------------------------+---------------+--------------------------------+-------------+------------------+
|    **PARAMETER NAME**     | **DATA TYPE** |        **DESCRIPTION**         | **DEFAULT** | **VALID VALUES** |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| NeighborAddress **[KEY]** | string        | Address of the BGP neighbor    | N/A         | N/A              |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| IntfRef **[KEY]**         | string        | Interface of the BGP neighbor  | N/A         | N/A              |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| SessionStateDuration      | string        | Time duration for which this   | N/A         | N/A              |
|                           |               | neighbor is in the current     |             |                  |
|                           |               | session state.                 |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| HoldTime                  | uint32        | Hold time for the BGP neighbor | N/A         | N/A              |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| NextHopSelf               | bool          | Use neighbor source IP as the  | N/A         | N/A              |
|                           |               | next hop for IBGP neighbors    |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| PeerAS                    | string        | Peer AS of the BGP neighbor    | N/A         | N/A              |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| RouteReflectorClusterId   | uint32        | Cluster Id of the internal     | N/A         | N/A              |
|                           |               | BGP neighbor route reflector   |             |                  |
|                           |               | client                         |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| AdjRIBInFilter            | string        | Policy that is applied for     | N/A         | N/A              |
|                           |               | Adj-RIB-In prefix filtering    |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| Messages                  | BGPMessages   | Rx/Tx counter for BGP update   | N/A         | N/A              |
|                           |               | and notification packets       |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| ConnectRetryTime          | uint32        | Connect retry time to          | N/A         | N/A              |
|                           |               | connect to BGP neighbor after  |             |                  |
|                           |               | disconnect                     |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| LocalAS                   | string        | Local AS of the BGP neighbor   | N/A         | N/A              |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| MaxPrefixesDisconnect     | bool          | Disconnect the BGP peer        | N/A         | N/A              |
|                           |               | session when we receive the    |             |                  |
|                           |               | max prefixes from the neighbor |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| MultiHopTTL               | uint8         | TTL for multi hop BGP neighbor | N/A         | N/A              |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| AddPathsRx                | bool          | Receive additional paths from  | N/A         | N/A              |
|                           |               | BGP neighbor                   |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| KeepaliveTime             | uint32        | Keep alive time for the BGP    | N/A         | N/A              |
|                           |               | neighbor                       |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| MultiHopEnable            | bool          | Enable/Disable multi hop for   | N/A         | N/A              |
|                           |               | BGP neighbor                   |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| BfdNeighborState          | string        | BFD state of the BGP neighbor  | N/A         | N/A              |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| Disabled                  | bool          | Enable/Disable the BGP         | false       | N/A              |
|                           |               | neighbor                       |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| MaxPrefixesRestartTimer   | uint8         | Time to wait before we start   | N/A         | N/A              |
|                           |               | BGP peer session when we       |             |                  |
|                           |               | receive max prefixes           |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| RouteReflectorClient      | bool          | Set/Clear BGP neighbor as a    | N/A         | N/A              |
|                           |               | route reflector client         |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| MaxPrefixesThresholdPct   | uint8         | The percentage of maximum      | N/A         | N/A              |
|                           |               | prefixes before we start       |             |                  |
|                           |               | logging                        |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| PeerGroup                 | string        | Peer group of the BGP neighbor | N/A         | N/A              |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| SessionState              | uint32        | Session state of the BGP       | N/A         | N/A              |
|                           |               | neighbor                       |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| TotalPrefixes             | uint32        | Total number of prefixes       | N/A         | N/A              |
|                           |               | received from the BGP neighbor |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| AddPathsMaxTx             | uint8         | Max number of additional paths | N/A         | N/A              |
|                           |               | that can be transmitted to BGP |             |                  |
|                           |               | neighbor                       |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| AdjRIBOutFilter           | string        | Policy that is applied for     | N/A         | N/A              |
|                           |               | Adj-RIB-Out prefix filtering   |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| Description               | string        | Description of the BGP         | N/A         | N/A              |
|                           |               | neighbor                       |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| MaxPrefixes               | uint32        | Maximum number of prefixes     | N/A         | N/A              |
|                           |               | that can be received from the  |             |                  |
|                           |               | BGP neighbor                   |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| PeerType                  | int8          | Type of the peer               | N/A         | N/A              |
|                           |               | (internal/external)            |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| Queues                    | BGPQueues     | Input/Output size of BGP       | N/A         | N/A              |
|                           |               | packet queues                  |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+
| UpdateSource              | string        | Source IP to connect to the    | N/A         | N/A              |
|                           |               | BGP neighbor                   |             |                  |
+---------------------------+---------------+--------------------------------+-------------+------------------+



*OpxFlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/state/BGPv6Neighbor
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/state/BGPv6Neighbors?CurrentMarker=<x>&Count=<y>
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/BGPv6NeighborState/<uuid>


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
		response, error = swtch.getBGPv6NeighborState(NeighborAddress=neighboraddress, IntfRef=intfref)

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
		response, error = swtch.getBGPv6NeighborStateById(ObjectId=objectid)

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
		response, error = swtch.getAllBGPv6NeighborStates()

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


