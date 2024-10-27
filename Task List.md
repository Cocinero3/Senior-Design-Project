***
### Setup SEED VM for testing
Assignee: Tucker Cook
#### Task Details:
- Test environment to utilize and get experience with various aspects of networking and networking tools
- Configure Wireshark
- Configure Scapy
- Configure kernel firewall modules

### Setup Android 4 VM for testing
Assignee: Ayush Verma
#### Task Details:
- Ensure all capabilities and testing are transferable from SEED VM
- Test environment to utilize and get experience with various aspects of networking and networking tools
- Configure Wireshark
- Configure Scapy
- Configure kernel firewall modules

### Configure environment for Android testing
Assignee: Ayush Verma
#### Task Details:
- Configure all necessary attributes to setting up development for Android applications
- https://www.geeksforgeeks.org/guide-to-install-and-set-up-android-studio/
- https://developer.android.com/studio/install

### Connect ID to TCU
Assignee: Tucker Cook & Ayush Verma
#### Task Details:
- Ensure that connection between Infotainment Display and Telematics Control Unit is viable
- Output a file of various data from the TCU that is accessible through the ID (any data)

### Connect application to TCU
Assignee: Tucker Cook & Ayush Verma

Task Details:
- Ensure that application is able to access the same data that ID is able to access from TCU
- Setup debug mode in our application to read various signals from TCU

### TCU Documentation
Assignee: Tucker Cook & Ayush Verma
#### Task Details:
- Prerequisite: figure out if data is encrypted from TCU, if not start documentation on various signals, vehicle speed, sensor data, etc. and document signal name, payload data, and destination
- If data is encrypted, use logger functionality of vehicle to cross-examine when data is being sent out and label data from there, signal name, payload data, and destination

### Implement Scapy and/or kernel firewall modules
Assignee: Tucker Cook & Ayush Verma
#### Task Details:
- Transfer setups/knowledge from testing in SEED VM & Android 4 VM to application within vehicle

### Design UI for application
Assignee: Ayush Verma
#### Task Details:
- Implement UI to cover functionality of:
	-Default screen of application should display all wireless signals
	-Clicking on signals will give signal name, payload data, destination, and general description of signal
		-Within this information screen, display option to disable or spoof signal
			-If spoof, let user input integer values for specific signals they want spoofed
		-Should display warning to user about inherit dangers of disabling certain wireless signals
- Each functionality will be implemented with _Overview button_ users can touch with fingers

### Implement logic to block/spoof signals to IP destinations
Assignee: Tucker Cook
#### Task Details:
- Implement logic from design diagram

### Implement logic to save user settings in a 'default settings file' each drive cycle upon restarting application
Assignee: Tucker Cook
#### Task Details:
- Implement logic from design diagram

### Test application in vehicle environment
Assignee: Tucker Cook & Ayush Verma
#### Task Details:
- Ensure all functionalities of our application work within a running vehicle environment
