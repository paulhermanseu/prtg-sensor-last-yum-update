# prtg-sensor-last-yum-update
PRTG Sensor - SSH Script - Yum update status - Days since last yum update

# How To Use?

## Install sensor on Linux server

1. Login to your Linux server
2. Create directory /var/prtg/scripts
3. Put sensor sh-script in this directory
4. Make executable chmod +x sh-script
5. Optional: Test it by executing the script

## Add sensor tot PRTG

1. Login to your Paessler PRTG Network Monitor
2. Add your Linux server as new device if needed and setup "Credentials for Linux/Solaris/MAC OS (SSH/WBEM) Systems"
3. Click "Add Sensor"
4. Choose "SSH Script"
5. Choose the right sh-script in the dropdown box under Sensor Settings > Script
6. Optional: Set Warning or Error limit in days under "Edit Channel Settings" > "Enable Limits" > "Upper Warning Limit" AND "Upper Error Limit"
7. Ready!

# Known issues

## Users with capital "U" in the username who run yum
The script searches for a capital "U" in the output of "yum history", if there is a user with a capital U in the name who did run the yum command, the script will take this date as the last yum update moment. Then this is not necessarily the last update, could also mean last install or remove date in that particular case.

# Compatibility

This sensor is tested with Linux Centos 6.x and 7.x
