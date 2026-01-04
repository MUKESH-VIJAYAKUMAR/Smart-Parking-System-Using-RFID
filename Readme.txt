Project Overview

The Smart Parking System is an IoT-based application designed to automate vehicle entry and exit tracking using RFID technology. An ESP32 microcontroller reads RFID cards and sends real-time parking data to a backend server. The server authenticates the request and stores the data securely in a Microsoft SQL Server database.

This project eliminates manual parking logs and provides accurate, real-time parking records.

⚙️ Technologies Used

Hardware

ESP32

RFID Reader (MFRC522)

RFID Cards

Buzzer

Software

Arduino IDE

Python (Flask)

Microsoft SQL Server (SSMS)

Git & GitHub

REST API (HTTP)

🧠 System Architecture

RFID Card
→ ESP32
→ HTTP POST (with API Key)
→ Flask Server
→ SQL Server (SSMS)

🔐 Security

API Key authentication is implemented

Only authorized ESP32 devices can send data to the server

Prevents unauthorized access to the database

🗄️ Database Structure

Database Name: SmartParkingDB
Table Name: parking_log

Columns:

UID (VARCHAR)

Name (VARCHAR)

Age (INT)

Entry_Time (DATETIME)

Exit_Time (DATETIME)

Status (VARCHAR)

🔁 Working Flow

RFID card is tapped on the reader

ESP32 reads the card UID

Entry or Exit is detected automatically

ESP32 sends data to Flask server in real time

Server validates API key

Data is stored in SQL Server instantly

Buzzer provides audio feedback

▶️ How to Run the Project

Step 1: Database Setup

Create database SmartParkingDB

Create table dbo.parking_log in SQL Server

Step 2: Run Server

pip install flask pyodbc
python server1.py


Step 3: Upload ESP32 Code

Open Arduino IDE

Select ESP32 board

Upload the ESP32 code

Open Serial Monitor

✅ Features

Real-time entry and exit tracking

Secure API communication

SQL-based persistent storage

Audible feedback using buzzer

Modular and scalable design

🎯 Future Enhancements

Java Swing dashboard

Parking duration calculation

Slot availability tracking

Admin login system

Cloud deployment