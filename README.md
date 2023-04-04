
# IFRIT Nuclear

An overengineered nuclear power plant management system for Minecraft.

## Acknowledgements

 - [Computer Craft Wiki](http://www.computercraft.info/wiki/Main_Page)
 - [IC2 Wiki](https://wiki.industrial-craft.net/index.php?title=Main_Page)


## Documentation
![Structure](/00_MANUAL/IfitNuclear_Plan.drawio.svg?raw=true&sanitize=true "Ifrit Nuclear Structure")

### IFRIT
IFRIT is the central command interface of Ifrit Nuclear, and the namesake of the entire system. It ingests information from ReMON, FuMON and ElMON.
It correlates events and passes them to GARUDA. It also accepts user input and passes it to BAHAMUT.

### BAHAMUT
BAHAMUT is the Reactor Safety System and saves the current state of the system. Based on the current state, certain user actions can be prohibited.
For this purpose, It takes in data from IFRIT, such as state changes, user commands and system commands. It returns the current state of the system, as well as success flag, which IFRIT then displays to the user and/or passes to GARUDA.
BAHAMUT is also the abstraction layer for the control of the Reactor process controls, which are redstone based, the Fuel Management and the Electrical Systems.

### GARUDA
GARUDA is the log-management system of Ifrit Nuclear. It saves all User inputs and correlated Events from IFRIT and makes them accessible for future reference.

### TITAN
TITAN is the Backup Control System, which directly interfaces with the reactor process controls. It allows for emergency actions to be performed.
As it is an emergency system, it is independent from BAHAMUT. However, all TITAN actions are passed to GARUDA for Alarm generation.

### ReMON
ReMON is a system which polls all reactor cores for activity, heat, power output and their inventory. It normalizes the information and makes it available for IFRIT to poll.

### ElMON (WIP)
ElMON is a system which monitors the electrical wiring and storage system of the entire powerplant. ElMON also monitors the emergency power generators.

### FuMON
FuMON is a technical system which monitors the storage, production, recycling and loading of fuel into the reactors.

### AFP
The Automatic Fuel Production System is a computerized and automated system which orchetstrates the fuel production. It takes input from BAHAMUT.

### CEC
The Computerized Electrical Control System is a computerized and automated system to control the electrical systems of the powerplant. This includes: storage, routing and emergency power generation.


See the 00_MANUAL folder for more details.





## Author

- [@LJMunt](https://www.github.com/LJMunt)


## FAQ

#### Why?

Boredom.

#### What Modpack was this made for?

Tekkit 1.12.2

