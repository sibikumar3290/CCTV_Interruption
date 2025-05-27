# CCTV Interception Project

## Overview
This project monitors the connectivity status of multiple IP cameras by periodically pinging their IP addresses. It updates the online/offline status of each camera in a MongoDB Atlas database in real-time.

## Features
- Pings IP cameras to check their connectivity.
- Tracks the online/offline status of each camera.
- Pushes status updates to a MongoDB Atlas collection.
- Continuously monitors cameras with near real-time updates.

## Technologies Used
- Python 3.x
- pymongo (MongoDB Python driver)
- MongoDB Atlas (cloud database)
- System ping command for connectivity check

## How It Works
1. The user inputs the number of IP cameras to monitor.
2. The user provides the IP addresses for each camera.
3. The system pings each IP to check if the camera is online.
4. The current status is pushed to a MongoDB Atlas collection.
5. The monitoring runs in a continuous loop, detecting status changes and updating the database.

## Usage
*Note: The source code is confidential and not included here as per company policy.*

- Ensure Python and required libraries (`pymongo`) are installed.
- Set up your MongoDB Atlas connection string in the configuration.
- Run the monitoring script and provide the camera IP addresses when prompted.

## Project Status
- Internship project for real-time IP camera monitoring.
- Designed for integration with MongoDB Atlas for remote status tracking.


*This repository contains only documentation and project description due to confidentiality agreements.*
