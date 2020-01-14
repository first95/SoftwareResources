# Updating firmware

To update all firmware on the robot, follow this procedure:
- Make sure the following software is installed on your laptop:
    - WpiLib
    - [Phoenix Framework](http://www.ctr-electronics.com/hro.html#product_tabs_technical_resources)
    - Rev Roborics SparkMax client
- Download and unzip the latest Talon SRX firmware here: http://www.ctr-electronics.com/control-system/motor-control/talon-srx.html#product_tabs_technical_resources
- Power on your robot, connect an Ethernet cable, and turn off your WiFi.
- Run the "RoboRIO imaging tool", which was installed with WpiLib.  It'll likely be a link on your desktop.
    - Follow the prompts to update the image on the roboRIO.  This will take about 10-20 minutes.
    - Follow the prompts to update the firmware on the roboRIO.  This should be under 10 minutes.
- Deploy code to the robot.  (This is required for the next step to work.)
- Open the Phoenix Tuner (came with Phoenix Framework)
    - Connect to the robot.  
    - Open the "CAN Devices" tab.  You should see a listing of all Talon SRX's and their firmware revision numbers.
    - Under the box labeled "Field-Upgrade Device Firmware", click "..." and browse to the unzipped Talon SRX firmware (a *.crf file)
    - Select a Talon SRX from the list.
    - Check the box labeled "Update all Talon SRX devices"
    - Click "Update device".  Process should take a few minutes.
    