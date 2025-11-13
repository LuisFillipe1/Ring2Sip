================================================================================
                    Ring2SIP - MicroSIP Inbound Call Handler
================================================================================

Ring2SIP automatically routes all your inbound calls to MicroSIP, turning your 
desktop into a powerful phone system.

================================================================================
INSTALLATION
================================================================================

1. Extract the Ring2SIP package to your desired location 
   (e.g., C:\Program Files\Ring2SIP\)
2. Ensure you have MicroSIP installed and running
3. Install the required dependencies by running install_dependencies.bat

================================================================================
CONFIGURATION
================================================================================

Before running Ring2SIP for the first time, you need to configure your settings:

1. Open the config.ini file in the Ring2SIP folder

2. Enter your SIP credentials:

   [SIP_SETTINGS]
   SIP_SERVER=sip.yourprovider.com
   SIP_PORT=5060
   SIP_USERNAME=your_username
   SIP_PASSWORD=your_password
   SIP_EXTENSION=1001

3. Configure your phone numbers to forward:

   [PHONE_NUMBERS]
   FORWARD_FROM=+15551234567
   FORWARD_TO_MICROSIP=true

4. Save and close the file

================================================================================
STARTING RING2SIP
================================================================================

To start Ring2SIP, simply run:

>>> Ring2Sip_start.bat <<<

This will:
- Launch the Ring2SIP service in the background
- Connect to your SIP server
- Begin monitoring for inbound calls
- Display a system tray icon showing the connection status

--- First-Time Setup ---

When you run Ring2Sip_start.bat for the first time:
1. Windows Firewall may ask for permission - click "Allow"
2. The configuration wizard will verify your SIP settings
3. A test call will be placed to confirm MicroSIP connectivity
4. Once successful, Ring2SIP will minimize to the system tray

================================================================================
USING RING2SIP
================================================================================

Once running, Ring2SIP works automatically:

- GREEN ICON  = Connected and ready
- YELLOW ICON = Connecting or call in progress
- RED ICON    = Connection error

Right-click the system tray icon for options:
- View call log
- Enable/disable call forwarding
- Do Not Disturb mode
- Settings
- Exit

================================================================================
STOPPING RING2SIP
================================================================================

To stop Ring2SIP:
- Right-click the system tray icon and select "Exit"
- Or run Ring2Sip_stop.bat

================================================================================
RUNNING AT STARTUP
================================================================================

To have Ring2SIP start automatically when Windows boots:

1. Press Win + R
2. Type shell:startup and press Enter
3. Create a shortcut to Ring2Sip_start.bat in this folder

================================================================================
TROUBLESHOOTING
================================================================================

--- No calls coming through? ---
- Verify MicroSIP is running and logged in
- Check your SIP credentials in config.ini
- Review the log file: logs\ring2sip.log

--- "SIP Connection Failed" error? ---
- Check your internet connection
- Verify your SIP server address and port
- Ensure port 5060 is not blocked by your firewall

--- MicroSIP not ringing? ---
- Confirm your SIP_EXTENSION matches your MicroSIP account
- Check that MicroSIP audio devices are properly configured
- Try restarting both MicroSIP and Ring2SIP

================================================================================
SYSTEM REQUIREMENTS
================================================================================

- Windows 10/11 (64-bit)
- MicroSIP 3.19 or higher
- 100 MB free disk space
- Active internet connection
- Valid SIP account

================================================================================
ADVANCED OPTIONS
================================================================================

Edit config.ini for advanced features:

[ADVANCED]
AUTO_ANSWER=false
RECORD_CALLS=true
RECORDING_PATH=C:\Recordings\
CODEC_PRIORITY=opus,g722,pcmu
MAX_CALL_DURATION=3600
ENABLE_NOTIFICATIONS=true
NOTIFICATION_SOUND=chime.wav

================================================================================
LOGS AND DEBUGGING
================================================================================

All activity is logged to logs\ring2sip.log

To enable debug mode:
1. Open config.ini
2. Set DEBUG_MODE=true under [ADVANCED]
3. Restart Ring2SIP
4. Check logs\ring2sip_debug.log for detailed information

================================================================================
SUPPORT
================================================================================

For issues or questions:
- Check the log files in the logs\ folder
- Review the FAQ at: https://ring2sip.example.com/faq
- Email support: support@ring2sip.example.com

================================================================================
LICENSE
================================================================================

Ring2SIP v2.4.1
(c) 2024 Ring2SIP Development Team
Licensed under MIT License

================================================================================

QUICK START REMINDER:
Just run Ring2Sip_start.bat and you're ready to receive calls!

================================================================================

