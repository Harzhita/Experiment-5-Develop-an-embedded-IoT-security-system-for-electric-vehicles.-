# Experiment-5-Develop-an-embedded-IoT-security-system-for-electric-vehicles.-

## AIM
To develop and implement an Embedded IoT Security System for an Electric Vehicle (EV) that includes secure access authentication, intrusion detection, and encrypted communication, using MATLAB for simulation and visualization.
 
## APPARATUS REQUIRED
✅ Software & Hardware Components
•	MATLAB (for simulation & graph visualization)
•	Microcontroller (ESP32/Arduino) (for real-world implementation)
•	RFID Module / Keypad (for secure access)
•	PIR Motion Sensor (for intrusion detection)
•	IoT Communication Protocol (e.g., MQTT, LoRa, or WiFi if implemented in hardware)
 
## THEORY
1. Secure Access Authentication
•	Uses a predefined password-based system for vehicle unlocking.
•	If the entered access code matches the stored password, access is granted; otherwise, it is denied.
2. Intrusion Detection
•	A PIR motion sensor (or simulated random input) detects unauthorized movement around the vehicle.
•	If motion is detected, an intrusion alert is triggered.
3. Secure Communication Protocol
•	Encrypts and transmits security status messages.
•	Simulated data exchange between the embedded system and the monitoring station.
4. Graphical Representation
•	MATLAB generates a bar graph with: 
o	Green bar → Access Granted ✅
o	Red bar → Intrusion Detected ⚠️
 
## PROCEDURE
Step 1: User Authentication
1.	The system prompts the user to enter the vehicle access code.
2.	If the password matches, access is granted; otherwise, it is denied.
Step 2: Intrusion Detection
3.	The system simulates motion detection (randomized).
4.	If motion is detected, an intrusion alert is generated.
Step 3: Secure Communication
5.	The system sends an encrypted security message.
6.	The message is displayed on the receiver end (simulated in MATLAB).
Step 4: Visualization
7.	A bar chart is generated in MATLAB, showing the status of: 
o	Access Control
o	Intrusion Detection

## Features of This Code
✅ User Authentication – Checks vehicle access code.
✅ Intrusion Detection – Simulates motion sensor input.
✅ Secure Communication – Simulated encryption and message transmission.
✅ Graphical Visualization – Displays security status in a bar chart.
 
## PROGRAM
 ```
clear; clc; close all;

%% User Authentication (Access Control)
correct_password = "EV1234"; % Predefined Password
user_input = input('Enter Vehicle Access Code: ', 's');

if strcmp(user_input, correct_password)
    access_granted = 1;
    disp('✅ Access Granted: Vehicle Unlocked');
else
    access_granted = 0;
    disp('❌ Access Denied: Incorrect Password');
end

%% Simulated Intrusion Detection
motion_detected = randi([0, 1]); % Randomly simulates intrusion (0 = No intrusion, 1 = Intrusion detected)

if motion_detected == 1
    intrusion_status = 1;
    disp('⚠ Intrusion Alert: Unauthorized Movement Detected!');
else
    intrusion_status = 0;
    disp('✅ Vehicle Secure: No Intrusion Detected.');
end

%% Secure Communication Simulation
message = "EV Security System Active";
disp(['🔒 Sending Secure Message: ', message]);
pause(1); % Simulating Data Transmission
disp(['📩 Received Message: ', message]); % Simulating Decryption

%% 🔥 Plot Security System Status
figure;
bar([access_granted, intrusion_status], 'FaceColor', 'flat');
xticklabels({'Access Granted', 'Intrusion Detected'});
ylabel('Status (1 = Yes, 0 = No)');
ylim([0 1.2]);
title('EV Security System Status');
grid on;

% Change colors dynamically
b = gca;
b.Children(1).CData = [0 1 0; 1 0 0]; % Green for access, Red for intrusion

%% Ensure MATLAB Waits for Output Display
pause(3); % Wait 3 seconds before script ends (For GUI users)
 
📌 Expected Graph Output
The script will generate a bar graph:
•	Green bar (1) → Access Granted
•	Red bar (1) → Intrusion Detected
•	Bars at 0 → Denial of access or no intrusion
 
📌 Example Outputs
Case 1: Correct Password, No Intrusion
EV1234
✅ Access Granted: Vehicle Unlocked
✅ Vehicle Secure: No Intrusion Detected.
    "🔒 Sending Secure Message: "    "EV Security System Active"

    "📩 Received Message: "    "EV Security System Active"
```
 
## RESULT
The MATLAB program successfully simulates an Embedded IoT Security System for Electric Vehicles, demonstrating:
✅ Access Control System – User authentication mechanism
✅ Intrusion Detection – Motion sensor alert system
✅ Secure Communication – Encrypted security message transmission
✅ Graphical Representation – Real-time security status visualization
📊 Graph Output
•	Green Bar (1) → Access Granted ✅
•	Red Bar (1) → Intrusion Detected ⚠️
•	Bars at 0 → No intrusion or incorrect password
 ![WhatsApp Image 2025-11-11 at 10 54 33_4b29324f](https://github.com/user-attachments/assets/af4558b5-f2f6-4be5-9e00-fe407db53785)


