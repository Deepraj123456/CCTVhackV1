Bangladesh Camera Scanner - Combined Tool
Visitors GitHub Views GitHub Stars GitHub Followers

Python Version Termux Support Platform License

🎯 Real-Time Visitor Counter - See Who's Visiting! 👆
A powerful tool that combines IP range collection and camera scanning functionality for Bangladesh networks.

Features
🌐 Fetch Bangladesh IPv4 ranges from APNIC database
📹 Scan for IP cameras and web services
🔍 Detect multiple camera brands:
Anjhua-Dahua Technology Cameras
HIK Vision Cameras
💾 Live save - Results saved instantly as they're found
💻 Termux compatible (Android)
🎨 Colorful terminal interface
🚀 Multi-threaded scanning (100 threads)
📊 Detailed camera information (IP, Port, URL, Timestamp)
Download Camera Live View App

.. https://gofile.io/d/fr8rOB

Installation
For Termux (Android)
Update packages
pkg update && pkg upgrade
Install required packages
pkg install python git
pkg install git -y
Install Python dependencies
pip install requests aiohttp pyfiglet
Optional: For colors (if colorama install fails, the script works without it)
pip install colorama
For Desktop (Windows/Linux/Mac)
Install Python dependencies
pip install requests aiohttp pyfiglet colorama
Usage
Run and clone the script:

git clone https://github.com/W8SOJIB/W8CameraHackV1
cd W8CameraHackV1
python W8CameraHackV1.py
Menu Options
Update IP Ranges from APNIC - Downloads latest Bangladesh IP ranges
Scan IP Ranges for Cameras - Scans the IP ranges for cameras (requires BDALLIP.txt)
Update & Scan (Both) - Does both operations in sequence
Exit - Quit the program
🎮 Scan Controls
During scanning, you can use:

Ctrl+C - ⛔ Stop scan immediately (instant exit)
Ctrl+Z - ⏸️ Pause/Resume scan (toggle on Linux/Mac/Termux)
Output Files
BDALLIP.txt - Contains Bangladesh IP ranges in CIDR notation
CCTV Found.txt - All detected cameras with details (Live Save)
Anjhua-Dahua Technology Cameras (WEB SERVICE detection)
HIK Vision Cameras (login.asp detection)
Output Format
Each detected camera is saved with:

Camera Type (Brand/Model)
IP Address
Port Number
Full URL
Detection Timestamp
Live saving (results appear immediately!)
Example Output:

============================================================
Camera Type: Anjhua-Dahua Technology Camera
IP Address: 192.168.1.100
Port: 80
URL: http://192.168.1.100
Detection Time: 2025-10-01 14:30:45
============================================================
See SAMPLE_OUTPUT.txt for more examples.

How It Works
IP Range Collection: Fetches Bangladesh IPv4 ranges from APNIC's delegation database
CIDR Parsing: Converts custom CIDR notation (IP/count) to individual IP addresses
Multi-threaded Scanning: Uses 100 threads to scan ports 80 and 8080 simultaneously
Detection: Identifies cameras by looking for specific HTML titles and patterns
Ports Scanned
Port 80 (HTTP)
Port 8080 (HTTP Alternative)
Notes
The scanner uses a 0.25 second timeout per connection
Results are saved in real-time to output files (Live Save with file.flush())
Instant Stop: Press Ctrl+C to stop scanning immediately (no delay!)
Pause/Resume: Press Ctrl+Z to pause and resume (Linux/Mac/Termux only)
The tool is optimized for Termux with fallback color codes if colorama is not available
All worker threads properly handle stop signals for clean shutdown
Legal Disclaimer
This tool is for educational and authorized security testing purposes only. Always obtain proper authorization before scanning networks you don't own.

Credits
👨‍💻 Developed by: Deepraj
GitHub Profile Views

Team: Deepraj
Contact: GitHub Profile

📊 Repository Stats
Repo Visitors GitHub code size GitHub repo size

Original Components
📡 All ASN Collector (IP Range Fetcher)
📹 CCTVhackV1  (Camera Scanner)
🔧 Combined & Optimized by Deepraj for Termux Support
⭐ If you like this project, please give it a star! ⭐

Made with ❤️ by Deepraj
