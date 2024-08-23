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
   crontab -e #Write the following cmd at the end of the cron table
   0 0 * * * bash /mnt/c/Users/lohit/Desktop/Spring_24/CS3500/Bashing/backup.sh -s /mnt/c/Users/lohit/Desktop/Spring_24/src/ -d /mnt/c/Users/lohit/Desktop/Spring_24/dest/ -o /mnt/c/Users/lohit/Desktop/i1.csv

 - *bash /mnt/c/Users/lohit/Desktop/Spring_24/CS3500/Bashing/backup.sh*:  Path to your backup script.
 - *-s /mnt/c/Users/lohit/Desktop/Spring_24/src/*:    Source directory.
 - *-d /mnt/c/Users/lohit/Desktop/Spring_24/dest/*:    Destination directory.
 - *-o /mnt/c/Users/lohit/Desktop/i1.csv*:      Statistics log file.
### Explanation of Each Field

1. **Minute (0 - 59)**:
- Specifies the minute of the hour when the job should run. * means every minute.

2. **Hour (0 - 23)**:
- Specifies the hour of the day when the job should run. * means every hour.

3. **Day of the Month (1 - 31)**:
- Specifies the day of the month when the job should run. * means every day of the month.

4. **Month (1 - 12)**:
- Specifies the month when the job should run. * means every month.

5. **Day of the Week (0 - 7)**:
- Specifies the day of the week when the job should run. 0 and 7 represent Sunday, 1 represents Monday, and so on up to 6 for Saturday. * means every day of the week.
