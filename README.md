IP Network Scanner
The Bariz Network Scanner is a Python-based desktop application designed for network administrators and engineers to perform network discovery, ping scans, port scans, and Remote Desktop Protocol (RDP) connections. Built with a graphical user interface (GUI) using tkinter and ttkbootstrap, it provides a user-friendly way to monitor network devices, check their status, and visualize network topology. The tool also supports command-line interface (CLI) mode for quick scans.
Features

Ping Scans: Scan individual IP addresses or ranges to check for online/offline status, hostname, MAC address, and latency.
Network Scans: Scan entire network ranges (e.g., 192.168.1.0/24) to discover active hosts.
Port Scans: Check specified ports (e.g., 22, 80, 443, 3389) for open/closed status and associated services.
RDP Connectivity: Initiate RDP connections to hosts (Windows only).
Auto-Scan: Schedule periodic scans at user-defined intervals.
Export Options: Save scan results as CSV, JSON, or LaTeX (for PDF generation).
IP List Management: Save and load IP lists to/from files or memory for reuse.
Network Topology Visualization: Display a simple graphical representation of online/offline hosts.
Dark/Light Theme: Toggle between light and dark themes for better usability.
Logging: Detailed logging of all operations to a timestamped log file.
Error Handling: Robust validation and error reporting for IP addresses, ranges, and ports.

Requirements

Python: 3.6 or higher
Dependencies:
ttkbootstrap (for GUI styling)
matplotlib (for topology visualization)
Pillow (optional, for potential image handling)


Operating System: Windows, Linux, or macOS (some features, like RDP, are Windows-only)
Permissions: Administrative privileges may be required for certain operations (e.g., ARP for MAC address resolution)

Install dependencies using pip:
pip install ttkbootstrap matplotlib Pillow

Installation

Clone the repository:git clone https://github.com/your-username/Bariz-network-scanner.git
cd Bariz-network-scanner


Install the required Python packages:pip install -r requirements.txt


Run the application:python Bariz_scanner.py

Or, for CLI mode:python Bariz_scanner.py --no-gui



Usage
GUI Mode

Launch the application: python Bariz_scanner.py
Input IPs:
Enter IP addresses, ranges, or station:IP pairs in the text box (e.g., Server1: 192.168.1.1 or 192.168.1.1-192.168.1.10).
Load saved IP lists from files or memory using the "Load IPs" or "Load from Memory" buttons.


Scan Options:
Start Scan: Ping the entered IPs to check status, hostname, MAC address, and latency.
Scan Network: Enter a CIDR range (e.g., 192.168.1.0/24) to scan all hosts in the network.
Port Scan: Scan specified ports (default: 22, 80, 443, 3389) for the entered or previously scanned IPs.


RDP Connection: Enter a hostname or IP to initiate an RDP session (Windows only).
Export Results: Save scan results as CSV, JSON, or LaTeX (for PDF compilation).
Auto-Scan: Enable auto-scan with a specified interval (in minutes) to periodically scan IPs.
Topology Visualization: View a simple plot of online/offline hosts.
Theme Toggle: Switch between light and dark themes for better visibility.

CLI Mode
Run a single ping scan for a specific IP:
python Bariz_scanner.py --no-gui

This performs a test scan on 192.168.1.1 and outputs the result to the console.
Directory Structure
Bariz-network-scanner/
├── Bariz_scanner.py        # Main application script
├── logs/                 # Log files (auto-generated)
├── saved_lists/          # Saved IP lists (auto-generated)
├── scan_results/         # Scan result exports (auto-generated)
├── README.md             # Project documentation
├── requirements.txt      # Python dependencies
├── .gitignore            # Git ignore file
└── LICENSE               # License file

Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch: git checkout -b feature-name.
Make your changes and commit: git commit -m "Add feature-name".
Push to the branch: git push origin feature-name.
Submit a pull request.

Please ensure your code follows PEP 8 style guidelines and includes appropriate logging.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For issues or suggestions, please open an issue on the GitHub repository or contact the maintainer at [your-email@example.com].

Developed by BARIZ for  Public use
