# Inventorizing SNMP Devices Using Fusion Inventory (FI)
This is final branch
1. Install FI agent in 1 computer located in the discovered network.
	- For Windows - https://github.com/tabad/fusioninventory-agent-windows-installer/releases/download/2.3.18/fusioninventory-agent_windows-x64_2.3.18.exe
2. Install NMAP
4. Enable SNMP modules for the agent.
	- FI > General > General configuration > Agent modules tab > Tick Network Inventory (SNMP) > Update
![img](http://image.prntscr.com/image/34d13fe1a1fe4512b37f645e16e9b3f3.png)
![img](http://image.prntscr.com/image/aa695873733d45ff97592acbcaf82e0f.png)
3. Create SNMP authentication in FI
	- FI > Networking > SNMP authentication > Add 
![img](http://image.prntscr.com/image/a671e072881c45faa9f580c9b3d03fe8.png)
![img](http://image.prntscr.com/image/c2364af98db941c798ba80fd846fd0a3.png)
5. Add Time Slot
	- FI > Tasks > Time slot > Add > 24x7
![img](http://image.prntscr.com/image/cfba2bbe17014ae0a8c26e40082a6bb6.png)
![img](http://image.prntscr.com/image/2b3494521d8e4c7384533bfc01136392.png)
1. Add Task	
	- FI > Tasks > Task Management > Add
![img](http://image.prntscr.com/image/09baba066a764a1685c5fa4bd1c2e589.png)
	- Add Task Name
	- Tick Active
	- Define Schedule
	- Choose Timeslot
![img](http://image.prntscr.com/image/4b3b1b025ad349d289be2b54cc856b70.png)
1. Go to Jobs Configuration tab > Add Discovery job
	- Select Target
	- Select Actor
	- Select 'Network discovery' in 'Module method'
	- Click Update
![img](http://image.prntscr.com/image/a00588261a964184bd73b4ab2c52e6b7.png)
1. Go to Jobs Configuration tab > Add Inventorize job
	- Select Target
	- Select Actor
	- Select 'Network inventory (SNMP)' in 'Module method'
	- Click Update
![img](http://image.prntscr.com/image/5dfe41add3a14f9f9ad529afaac532dc.png)
1. Add IP range(s)
	- Networking > IP ranges
![img](http://image.prntscr.com/image/7ce661b9a4d54296a77fa0fd7288fb78.png)
	- Define network name, Start IP and End IP.
![img](http://image.prntscr.com/image/1258afa41fcc4d4a84a78d9f1efdc49e.png)
4. Associate SNMP credential to IP ranges.
	- Go to Associated SNMP authentication
![img](http://image.prntscr.com/image/a43a9bb88c874504813f7c047ef1bd90.png)
