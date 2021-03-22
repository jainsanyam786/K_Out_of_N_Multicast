HostDictionary.py:

	hostDic =  mapping for ip address and port with node id.
	RoutingTables = dictionary for routing tables.
	MulticastTable = dictionary of routers to get best router for scenario 

Routing.py:
	
	Main file to create routing tables, multicast tables and method of this py file are called by Source, Router and Host to get required information. 
	
	After we get topology Run Routing.py with argument createRoutingTable to create Routing Tables and Multicast Table.These will be writtern in HostDictionary.py

Source.py

	on Source run Source.py as  Source.py <nodeid>

Router.py

	on each Router run Router.py  as Router.py <nodeid>

Host.py

	on each Host run  as Host.py <nodeid>
