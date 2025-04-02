# Mobile-to-PC Auto Typer

A Python-based system that allows text input from a mobile device to be automatically typed on a connected PC. Supports both Bluetooth and USB connections.

## Features

- Mobile app with simple text input interface
- PC listener application with connection status GUI
- Support for both Bluetooth and USB connectivity
- Real-time text typing simulation on PC
- Connection status monitoring
- Easy-to-use interface

## Requirements

### Mobile Device (Android with Termux)
- Termux app from F-Droid store
- Python 3.7+
- Kivy framework
- PyBluez
- PySerial

### PC
- Python 3.7+
- PyAutoGUI
- PyBluez
- PySerial
- Tkinter (usually comes with Python)

## Installation

### Setting up Termux on Android
1. Install Termux from F-Droid store (recommended) or Google Play Store
2. Open Termux and update the package list:
   ```bash
   pkg update && pkg upgrade
   ```
3. Install required packages:
   ```bash
   pkg install python
   pkg install git
   ```
4. Install Python package manager:
   ```bash
   pkg install python-pip
   ```
5. Grant storage permission to Termux:
   ```bash
   termux-setup-storage
   ```

### Installing the Application
1. Clone or download this repository:
   ```bash
   git clone <repository-url>
   cd <project-folder>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### PC Application
1. Run the PC listener application:
   ```bash
   python pc_listener.py
   ```
2. Select connection type (Bluetooth or USB)
3. Click "Start Listening" to begin accepting connections

### Mobile Application (Termux)
1. Navigate to the project directory:
   ```bash
   cd storage/downloads/<project-folder>  # or wherever you saved the project
   ```
2. Run the mobile application:
   ```bash
   python mobile_app.py
   ```
3. Select connection type (match with PC)
4. Click "Connect" to establish connection
5. Enter text and click "Send Text" to type on PC

## Troubleshooting

### Termux Issues
- If you get permission denied errors, run: `termux-setup-storage`
- For Bluetooth issues, install Termux:API app and run: `pkg install termux-api`
- If packages fail to install, try: `pkg update && pkg upgrade`

### Bluetooth Issues
- Ensure Bluetooth is enabled on both devices
- Check if devices are paired
- Verify Bluetooth permissions are granted

### USB Issues
- Check USB cable connection
- Verify correct USB port is selected
- Ensure proper USB permissions

## Security Notes

- The connection is device-to-device only
- No data is stored or transmitted to external servers
- Connection is limited to one device at a time

## License

This project is open source and available under the MIT License.