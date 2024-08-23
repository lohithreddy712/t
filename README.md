# Automated Backup Script

## Overview

This script performs automated backups of files from a source directory to a destination directory, including only those files with vowels in their names. It is designed to ensure that subsequent backups are only performed if there are changes in the files since the last backup. The script also logs its activity and runs daily at midnight.

## Features

1. **Backup Files with Vowels**: Copies files with vowels in their names from a source directory to a destination directory.
2. **Efficient Backup**: Performs backups only if files have changed since the last backup.
3. **Scheduled Execution**: Runs automatically every day at midnight using cron.
4. **Logging**: Records statistics including the process ID and runtime in a specified log file.

## Cron Job Setup

To schedule the script to run automatically using cron, follow these steps:

1. **Open the Crontab File**:

   Open your cron table for editing by running:
   ```bash
   crontab -e
Then write the following command at the end of the crontab
  ```bash
 0 0 * * * bash /mnt/c/Users/lohit/Desktop/Spring_24/CS3500/Bashing/backup.sh -s /mnt/c/Users/lohit/Desktop/Spring_24/src/ -d /mnt/c/Users/lohit/Desktop/Spring_24/dest/ -o /mnt/c/Users/lohit/Desktop/i1.csv
