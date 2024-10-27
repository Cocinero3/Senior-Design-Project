## Diagram 1
- Gives inputs and outputs of system
	- Inputs: TCU signals, user input, and infotainment display
	- Outputs: Updated display, updated values to be sent to TCU
- Includes list of functions to be performed by application logic before reaching output
- Demonstrates overall system design to be implemented
## Diagram 2
- Adds drive cycles (represented as rectangles)
	- Each of these drive cycles represents a layer of which certain functionalities will take place
	- Includes initial, change event, and default cycles
- Labels each signal to be sent i.e. default, spoofed, and permissible (represented as arrows)
- Adds hardware & software entities (represented as rounded rectangles)
- Adds end-user entity (represented as stick figure)
- Demonstrates how user & application logic will play a role in updating interface and signals sent to destination
## Diagram 3
- Adds domains, application logic, hardware, and destination
- Details how application logic is to be implemented by developers 
	- Conditional logic (diamonds)
	- Batches/arrays (Labeled rectangles)
	- Algorithm/functions (Ovals)
- Labels flow of signal to either IP destination or no-go batch where the signal will not be utilized at all
	- Green, permissible signals according to user & application logic
	- Orange, signals to be determined permissible or not that are sent automatically by TCU
	- Red, no go signals that will not make it to destination IP
- Demonstrates specific logic on how interface will be updated and which signals to be sent to destination