# Bash Script for Weekly Server Updates and Package Upgrades

## Author: Khalil Elkharbibi
## Date: 2023-08-30

## Overview

This documentation provides a detailed explanation of a Bash script designed to run weekly server updates and create a report on upgradable packages. The script is scheduled to run automatically every Friday at 11 PM using a cron job.

Author: Your Name
Date: 2023-08-30

## Script Purpose

The Bash script serves the following purposes:

1. Updates the server's package list and performs upgrades.
2. Generates a report on the number of packages that can be upgraded.
3. Creates a text file with the upgrade count and the current date appended to its name.

## Cron Job Configuration

To automate the script's execution, a cron job has been set up. The cron job schedule is as follows:


## Schedule script to run weekly on Fridays at 11pm
`$ 0 23 * * 5 /usr/local/bin/weekly_update.sh`


- `0` represents the minute field, indicating the task starts at the beginning of the hour.
- `23` denotes the hour field, specifying that the task runs at 11 PM.
- `*` in the day and month fields means the script runs every day and every month.
- `5` in the day of the week field corresponds to Friday.
- `/path/to/your/weekly_update.sh` should be replaced with the actual path to your script.

## Script Execution

To manually run the script, follow these steps:

1. Open a terminal.
2. Navigate to the directory where you saved the `weekly_update.sh` script.
3. Run the script using the following command:

   ```bash
   ./weekly_update.sh


## Script Output
The script produces the following output:

Updates the server and displays progress messages.
Prints the number of upgradable packages to the terminal.
Creates a text file with the format updateMM.DD.YY.txt, where MM, DD, and YY represent the month, day, and year, respectively. For example, update08.30.23.txt.
Error Handling
The script is designed with limited error handling. It is essential to ensure that you have appropriate permissions and that the system package manager (apt-get in this case) is installed and configured correctly.

## Conclusion
This Bash script automates server updates and package upgrades, creating a report for reference. By setting up the provided cron job, you can ensure that the script runs automatically every Friday at 11 PM, simplifying routine server maintenance tasks.
