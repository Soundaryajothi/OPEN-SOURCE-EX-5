# OPEN-SOURCE-EX-5
# NAME:SOUNDARYA J
# REG NO:212223220108

# Aim

To configure scheduled cron jobs for the user harry that execute specific commands at defined times using the crontab utility in Red Hat Enterprise Linux.

# Algorithm
<h2>Step 1:</h2>
Start the Terminal as Root.
Switch to the root user or use administrative privileges to configure cron jobs for another user.
<h2>Step 2:</h2>
Edit the Crontab for User harry.
Open the crontab editor for user harry using the crontab -e command.
<h2>Step 3:</h2>
Configure Multiple Cron Jobs.

Schedule a job to run daily at 12:30 PM to execute /bin/echo "hello".

Schedule a job to run every 2 minutes to execute /bin/echo "Hi I'm Running".

Schedule a job to run daily at 2:23 PM to log the message "RHCSA EXAM TRAINING".

Schedule a job to run daily at 12:00 PM to log the message "EX200 in Progress".
<h2>Step 4:</h2>
Save and Exit the Crontab.
After adding all jobs, save the file and exit the editor.
<h2>Step 5:</h2>
List and Verify Cron Jobs.
View all scheduled jobs for user harry to confirm correct configuration.
<h2>Step 6:</h2>
Check Cron Service Status.
Verify if the cron service (crond) is active and running properly.
<h2>Step 7:</h2>
Start and Enable Cron Service.
If inactive, start and enable the cron service to ensure jobs run automatically.
<h2>Step 8:</h2>
Manually Test Commands.
Test echo and logger commands as the user harry to confirm correct functionality.
<h2>Step 9:</h2>
Check Logs for Verification.
Review the system journal to confirm that the logger messages have been recorded successfully.

# Steps Involved
```
STEP 1 : sudo -i
STEP 2 : crontab -u harry -e

# Run daily at 12:30 PM
30 12 * * * /bin/echo "hello"

# Run every 2 minutes
*/2 * * * * /bin/echo "Hi I'm Running"

# Run daily at 2:23 PM
23 14 * * * /usr/bin/logger "RHCSA EXAM TRAINING"

# Run daily at 12:00 PM
0 12 * * * /usr/bin/logger "EX200 in Progress"

STEP 4 : crontab -u harry -l
STEP 5 : systemctl status crond
STEP 6 : systemctl start crond
          systemctl enable crond
STEP 7 : sudo -u harry /bin/echo "hello"
          sudo -u harry /usr/bin/logger "RHCSA EXAM TRAINING"
STEP 8 : journalctl | grep RHCSA
```
# Output
<img width="1309" height="976" alt="image" src="https://github.com/user-attachments/assets/0b5da3c0-b103-4726-8762-8a4ff6bf5618" />



# Result

Thus, multiple cron jobs were successfully configured for the user harry to execute commands and log messages at specified intervals in Red Hat Enterprise Linux.
