# Aquaculture-and-Monitering
Project Demonstration & Documentation                                                                                                                                              Title:Aquaculture AndMonitoring  

                                  (Automatic fish feeder) 

Abstract:  

 This project implements an automated feeder control system using a microcontroller, designed to operate a servo motor at predefined time intervals. The system reads user-defined configurations such as servo pin assignment, feeding frequency (in hours), and feed duration (in seconds) from non-volatile memory. If no valid configuration is found, default values are assigned and stored. 

The code initializes the hardware and sets up the feeder mechanism by calling startFeeder() with the retrieved or default configuration. The loop() function maintains the system's runtime with minimal delay, as the feeding logic is expected to run independently, likely based on timers or background tasks. This architecture ensures non-blocking operation, making the system reliable for continuous use in real-world automated feeding applications, such as pet feeders or agricultural automation. 

By abstracting feeding parameters and persisting them across resets, the system provides a user-configurable, scalable, and robust solution for time-based servo actuation tasks. 

 

Project Demonstration  

Overview: 

This code sets up an automatic feeder system using a servo motor controlled by a microcontroller. It loads feeding settings from memory or uses defaults, then starts the feeding process based on a time schedule.  

Demonstration Details:  

Hardware Setup: 

Connect a servo motor to GPIO pin 18 of the microcontroller (e.g., ESP32). 

Ensure the microcontroller is powered and connected to a serial monitor (via USB). 

Upload and Run the Code: 

Upload the code to the microcontroller using the Arduino IDE or PlatformIO. 

Open the serial monitor at 115200 baud rate. 

Behavior Upon Startup: 

The system checks for saved feeder settings (pin, interval, and duration). 

If not set, default values are assigned (pin 18, feed every 5 hours, for 2 seconds). 

The system then initializes the feeder schedule. 

Feeder Operation: 

The servo motor activates based on the schedule. 

During activation, it simulates feeding (e.g., rotating the servo arm to dispense food). 

Testing Manual Trigger (optional): 

You can add a manual serial command (e.g., type 'F') to trigger feeding instantly for testing. 

Expected Output: 

Serial monitor displays status: whether preferences are set, default values used, and feeder started. 

Servo motor should visibly rotate according to the configured duration when triggered. 

 

Outcome:  

The automatic feeder system successfully initializes using stored or default settings and controls a servo motor to dispense food at regular time intervals. The configuration is saved in memory, ensuring reliable and continuous operation even after system restarts. 

1.Project Documentation  

Overview:  

This project focuses on building an Automatic Feeder System using a microcontroller and a servo motor. The system is designed to dispense food at regular time intervals, making it ideal for pet care or small-scale agricultural use. 

The code initializes by checking for stored feeder settings (servo pin, feeding interval in hours, and duration in seconds). If no valid configuration is found, it sets default values and saves them to memory. The servo motor is then scheduled to operate based on these settings, enabling automated, timed feeding without the need for constant user input. 

This project demonstrates how embedded systems can be used for real-world automation by combining hardware control, persistent storage, and time-based task execution. 

Documentation sections: 

System Architecture: 

The system architecture consists of an ESP32 microcontroller controlling a servo motor that dispenses food at defined intervals. 

Configuration data (feeding time, duration, servo pin) is stored in non-volatile memory for persistence. 

The system is intended to be expandable with IoT features for remote management. 

Code Documentation: 

The code is modular, with key functions like setup(), loop(), readFeederPreferences(), writeFeederPreferences(), and startFeeder(). 

Each function is responsible for different parts of the logic (e.g., initializing the serial monitor, reading settings, controlling the feeder). 

User Guide: 

This guide explains how to set up the hardware (connecting the servo motor to the ESP32), upload the code, and monitor feeding cycles through the serial monitor. 

Troubleshooting tips for common issues like invalid configurations or servo misalignment are provided. 

Administrator Guide: 

This section provides details for administrators to modify default settings, maintain hardware, and troubleshoot. 

Suggestions for scaling the system and integrating IoT features are also included. 

Testing Reports: 

Reports include tests for feeding consistency, configuration persistence, and servo operation. 

Performance tests confirm that the feeder dispenses food at the set intervals and retains settings through power cycles. 

Outcome: 

A fully functional automated fish feeder system that works reliably based on stored configuration settings. 

 

3. Feedback and Final Adjustments 

Overview 

Feedback from early testers was collected to refine the system and ensure that it meets user needs. 

Steps 

Feedback Collection: 
 Feedback was gathered from users and testers, particularly on ease of use, reliability of the feeding cycle, and configuration process. 

Refinement: 
 Based on feedback, we added more detailed serial output for users to see feeding schedule details. We also proposed a manual feeding option via the serial interface. 

Final Testing: 
 Comprehensive tests were performed to ensure that the system functions as expected, including testing of configuration persistence, real-time monitoring, and feeding accuracy. 

Outcome 

The system is now more user-friendly, with improved logging and feedback for users. It meets the initial design goals and is ready for deployment in real-world aquaculture applications. 

 

4. Final Project Report Submission 

Overview 

This final report consolidates the development process, challenges faced, and the system's capabilities. 

Report Sections 

Executive Summary: 
 Overview of the automated fish feeder system, its purpose, features, and outcomes. 

Phase Breakdown: 
 Description of the various phases: planning, development, testing, and final adjustments. 

Challenges and Solutions: 
 Key challenges included ensuring configuration persistence and precise servo control. These were solved by using non-volatile memory and adjusting timing logic. 

Outcomes: 
 Successful implementation of the automated fish feeder with clear potential for future IoT-based enhancements. 

Outcomes 

The system is robust, reliable, and ready for deployment in aquaculture. Future enhancements like IoT integration and remote monitoring are possible. 

 

5. Project Handover and Future Works 

Overview 

This section outlines the handover process and future steps to further improve the system. 

Handover Details 

Code Files: All relevant code, configuration files, and hardware schematics are included. 

Documentation: Complete user, administrator, and technical documentation is provided. 

Setup Instructions: Step-by-step instructions for installation and operation. 

Next Steps 

Implement IoT integration for remote management. 

Add additional sensors for water quality monitoring. 

Enhance system to handle multiple tanks. 

Outcome 

The project is successfully handed over, with full documentation and code. Future enhancements will continue to improve the system’s scalability, usability, and features. 

 
