# RFID-Based-Attendance-System
**📋 Project Overview**

The RFID-Based Attendance System is an automated solution designed to streamline the process of recording attendance. By using Radio Frequency Identification (RFID) technology, the system eliminates manual paperwork and reduces errors, providing a fast and secure way to log entries and exits in real-time.

**⚙️ How It Works**

The system operates on the principle of electromagnetic fields to identify and track tags attached to objects or people.

Scanning: When a user places their RFID tag (card or keychain) near the RFID reader, the reader emits a high-frequency electromagnetic field.

Authentication: The passive tag draws power from this field to send its unique ID (UID) back to the reader.

Processing: The microcontroller (e.g., Arduino or ESP32) receives the UID and compares it against a pre-registered database.

Logging: If the ID is recognized, the system logs the timestamp and the user's name. This data can be displayed on an LCD, saved to an SD card, or sent to a web server/spreadsheet via Wi-Fi.

**🛠️ Components Used**

To build this system, the following hardware components are typically required:

1. Microcontroller
   Arduino Uno / Nano: The "brain" of the project that handles the logic.

   Alternative: ESP32 / NodeMCU (if you want to sync data to the cloud via Wi-Fi).

2. RFID Module (RC522)
   The MFRC522 is the most common reader used for 13.56 MHz tags. It acts as the interface between the physical tags and the controller.

3. RFID Tags/Cards
   Each user is assigned a unique tag. These are passive devices that do not require a battery.

4. User Interface & Feedback
   16x2 I2C LCD Display: To show messages like "Access Granted" or "Welcome [Name]."

   Buzzer: Provides an audible "beep" to confirm a successful scan.

   LEDs (Red/Green): Visual indicators for authorized or unauthorized access.

5. Data Storage/Connectivity
   RTC Module (DS3231): To keep track of the exact date and time even when power is lost.

   Micro SD Card Module: To store attendance logs locally in a .csv format.

**🚀 Key Features**

Real-time Processing: Attendance is marked instantly upon scanning.

Unique Identification: Each tag has a permanent UID, preventing duplication.

Data Export: Logs can be easily exported for administrative review.

Scalability: New users can be added to the system by simply registering their UIDs in the code.
