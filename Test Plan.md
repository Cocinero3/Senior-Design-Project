## Part I.
Our testing strategy for the Android VPN application focuses on ensuring both the reliability of the VPN connection and the functionality of the user interface. We employ a combination of automated and manual testing methods to achieve comprehensive coverage. For VPN reliability, we utilize network simulation tools to test connection stability, performance under various network conditions, and automatic reconnection capabilities. These tests are designed to mimic real-world scenarios that drivers might encounter, such as passing through areas with poor connectivity or high network congestion. 

For UI functionality, we leverage Android-specific testing frameworks, including the Monkey tool for stress testing and UI Automator for simulating user interactions. Our approach includes both unit tests for individual components and integration tests to ensure smooth operation of the entire system. We also incorporate performance testing to measure response times and resource usage, ensuring the application runs efficiently on typical vehicle hardware. Security testing is a critical component of our plan, given the sensitive nature of VPN applications. We conduct regular penetration tests and code reviews to identify and address potential vulnerabilities. Additionally, we implement a continuous integration pipeline that runs a subset of these tests on every code commit, allowing us to catch and fix issues early in the development process.

## Part II.

### UI1.1 User Interface Test 1
- UI1.2 This test will ensure that the user is able to customize the UI controls to their preference by hiding unneeded options.
- UI1.3 This test involves the user hiding certain controls from the UI and making sure they properly disappear.
- UI1.4 Inputs: User input via tapping the screen 
- UI1.5 Outputs: Screen should update to hide whichever control was hidden by the user
- UI1.6 Normal
- UI1.7 Blackbox
- UI1.8 Functional
- UI1.9 Unit Test
- UI1.10 Results: Control is now hidden from the screen, but still available for a user to interact with and bring back if desired

### UI2.1 User Interface Test 2
- UI2.2 This test will ensure that the user is able to customize the UI controls to their preference by unhiding previously hidden options.
- UI2.3 This test involves the user showing certain controls in the UI that were previously hidden.
- UI2.4 Inputs: User input via tapping the screen
- UI2.5 Outputs: Screen updates to show new options 
- UI2.6 Normal
- UI2.7 Blackbox
- UI2.8 Functional
- UI2.9 Unit Test
- UI2.10 Results: The chosen control is now displayed on the main UI alongside the previously shown options

### UI3.1 User Interface Test 3
- UI3.2 This test will ensure that the UI correctly parses and displays information retrieved from active network packets
- UI3.3 For this test we will create a set of mock data packets for the UI to read and display to simulate what will be coming from the VPN service when the entire app is running. This will test that the UI is still readable and can handle various loads of data coming in at once.
- UI3.4 Inputs: Data packets that match the format of what is expected to be read through a vehicle's infotainment network traffic
- UI3.5 Outputs: UI should populate with details regarding each unique network event about the source and destination of the packets
- UI3.6 Normal
- UI3.7 Whitebox
- UI3.8 Functional
- UI3.9 Unit Test
- UI3.10 Results: The expected details for each packet are properly shown without any errors on the UI

### UI4.1 User Interface Test 4
- UI4.2 This test will ensure that a user can filter the network activity view based on a certain application/source IP address.
- UI4.3 The user will navigate to the filter view that displays a list of options based on previously captured network traffic where they will select what to filter the view by.
- UI4.4 Inputs: User input by tapping the screen, source IP to filter by.
- UI4.5 Outputs: UI properly updates to only show network activity corresponding to the new filter rules.
- UI4.6 Normal
- UI4.7 Blackbox
- UI4.8 Functional
- UI4.9 Unit Test
- UI4.10 Results: User can now view the network activity window and see activity only related to their chosen filter rule(s).

### UI5.1 User Interface Test 5
- UI5.2 This will test that a user can properly grant the app permission to begin VPN services.
- UI5.3 The user will hit the start button in the main UI of the app to trigger an Android popup allowing them to grant access to begin the VPN by tapping 'Accept'.
- UI5.4 Inputs: User input by tapping the screen
- UI5.5 Outputs: Application now has permission to initialize a VPN
- UI5.6 Normal
- UI5.7 Blackbox
- UI5.8 Functional
- UI5.9 Unit Test
- UI5.10 Results: Application correctly displays the permissions popup before then being properly granted access to start the VPN.

6. **UI_Functionality_06**  
    **Purpose:** Verify core UI component responsiveness.  
    **Description:** Test all primary buttons/menus using simulated interactions.  
    **Inputs:** Android device, UI automation tools  
    **Expected Results:** <500ms response time for all actions.  
    **Case Indication:** Normal  
    **Test Type:** Blackbox  
    **Test Focus:** Functional  
    **Test Level:** Unit
7. **UI_Functionality_07**  
    **Purpose:** Stress test UI under heavy interaction load.  
    **Description:** Use Android Monkey tool to generate random input bursts.  
    **Inputs:** Monkey testing configuration, performance monitor  
    **Expected Results:** No crashes with 1000+ random events/minute.  
    **Case Indication:** Boundary  
    **Test Type:** Blackbox  
    **Test Focus:** Performance  
    **Test Level:** Integration
8. **UI_Functionality_08**  
    **Purpose:** Validate error handling for invalid inputs.  
    **Description:** Enter malformed credentials/server addresses.  
    **Inputs:** Invalid data set, debug logging enabled  
    **Expected Results:** Clear error messages with guidance.  
    **Case Indication:** Abnormal  
    **Test Type:** Blackbox  
    **Test Focus:** Functional  
    **Test Level:** Unit

9. **VPN_Reliability_01**  
    **Purpose:** Verify VPN connection stability under normal conditions.  
    **Description:** Establish VPN connection and monitor stability over time.  
    **Inputs:** VPN credentials, Android device  
    **Expected Results:** Stable connection without interruptions.  
    **Case Indication:** Normal  
    **Test Type:** Blackbox  
    **Test Focus:** Performance  
    **Test Level:** Integration
10. **VPN_Reliability_02**  
    **Purpose:** Test automatic reconnection after network disruption.  
    **Description:** Simulate network dropout and measure reconnection time.  
    **Inputs:** Network disruption tool, VPN credentials  
    **Expected Results:** Reconnection within 30 seconds.  
    **Case Indication:** Abnormal  
    **Test Type:** Blackbox  
    **Test Focus:** Functional  
    **Test Level:** Integration
11. **VPN_Reliability_03**  
    **Purpose:** Measure performance under high traffic.  
    **Description:** Generate heavy network load while connected to VPN.  
    **Inputs:** Traffic generation tool, latency measurement software  
    **Expected Results:** Latency <150ms, throughput >5Mbps.  
    **Case Indication:** Boundary  
    **Test Type:** Blackbox  
    **Test Focus:** Performance  
    **Test Level:** Integration

|      | Normal/Abnormal | Blackbox/Whitebox | Functional/Performance | Unit/Integration |
| ---- | --------------- | ----------------- | ---------------------- | ---------------- |
| UI1  | Normal          | Blackbox          | Functional             | Unit             |
| UI2  | Normal          | Blackbox          | Functional             | Unit             |
| UI3  | Normal          | Whitebox          | Functional             | Unit             |
| UI4  | Normal          | Blackbox          | Functional             | Unit             |
| UI5  | Normal          | Blackbox          | Functional             | Unit             |
| UI6  | Normal          | Blackbox          | Functional             | Unit             |
| UI7  | Normal          | Blackbox          | Functional             | Unit             |
| UI8  | Normal          | Blackbox          | Functional             | Unit             |
| VPN1 | Normal          | Blackbox          | Performance            | Integration      |
| VPN2 | Abnormal        | Blackbox          | Functional             | Integration      |
| VPN3 | Normal          | Blackbox          | Performance            | Integration      |