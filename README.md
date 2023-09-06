# Bash Script for Weekly Server Update and Package Upgrade
# Author: Khalil Elkharbibi
# Date: 2023-08-30

# Purpose of the cron job:
# This script will be executed automatically every Friday at 11 PM to update the server and log the output.

#!/bin/bash

**Schedule script to run weekly on Fridays at 11pm**
`$ 0 23 * * 5 /usr/local/bin/weekly_update.sh`

# Display a message indicating the script is starting
echo "Starting the server update and package upgrade script..."

# Update the server
sudo apt-get update && sudo apt-get upgrade -y

# Get the count of upgradable packages
upgrade_count=$(apt list --upgradable 2>/dev/null | wc -l)

# Create a filename with the current date in the format update
weekly_update.sh="update$(date +'%m.%d.%y').txt"

# Create a new file and write the upgrade count information
echo "$upgrade_count packages can be upgraded." > "$weekly_update.sh"

# Display the upgrade count message on the screen
echo "$upgrade_count packages can be upgraded."

# Display a message indicating the script has finished
echo "Script completed."

# Exit the script
exit 0

