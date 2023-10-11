---
title: "SIOT based Biometric Ubiety Management using G-Spreadsheets"
description: "Secured Internet of Things (SIoT) based portable biometric attendance system!"
dateString: Dec 2021
draft: false
tags: ["TypeScript", "NodeJS", "Docker", "GitHub Actions"]
showToc: false
weight: 202
cover:
    image: "projects/SIOT/cover.jpg"
--- 
### 🔗 [GitHub](https://github.com/mvipinchand/UG-Design-Project)

## Description
The traditional process of manually taking and maintaining student attendance is highly inefficient and time consuming. The attendance monitoring system based on biometric authentication has a potential to streamline the whole process. A Secured Internet of Things (SIoT) based portable biometric attendance system can prove to be of great value to educational institutions in this regard as it proves to be highly efficient and secure. The cost involved in making this system is quite less, when compared to existing conventional biometric attendance system. The use of cloud computing to store the attendance records makes all the data easy to access and retrieve as end when required by the teachers. 

Build from scratch using **ESP8266 NodeMCU**, **R305 Fingerprint sensor**, **(16*2) Alphanumeric LCD**, **I2C Module**. NodeMCU is programmed to sync with Google sheets using Device ID and send data to the sheets using Pushingbox API.

The unique ID number of the student is recognised. The attendance data is logged into Google Spreadsheet by uploading the student’s ID number in it, For uploading the ID number in Google Spreadsheet, **PushingBox** API is used. After the attendance is granted, i.e. the ID is stored in Google Spreadsheet, the Fingerprint Comparison and Recognition process starts.

## Algorithm

1) Start
2) Print “WELCOME”
3) Print “BIOMETRIC ATTENDANCE”
4) Enter password for respective subject
5) Establishing WiFi Connection
6) Searching for sensors
7) Establishing Interface with sensors
8) Then, Start fingerprint scanning
9) Starting of loop
10) If Fingerprint matches, then mark attendance to a[i]
11) Sent attendance in a[i] to wifi and then show date and time.
12) Using Pushing Box API upload it to google sheets
13) Else Show INVALID
14) Prepare an Cummulative at end of the month
15) And share it to all using Google Classroom
16) Remove the access by entering password again
17) End outer loop
18) Stop.