# Automated Bible Reading Email Reminder

## Overview
This script is designed to automate the process of sending daily Bible reading reminders via email. It divides the Bible into specific sections, and each day, the script selects the next chapter to read from each section. Once the end of a section is reached, it loops back to the beginning. The script then sends an email with the daily reading plan.

## Features
- Automated selection of daily Bible reading chapters from predefined sections.
- Email notification with the day's reading plan.
- Progress tracking through a JSON file to keep up with the reading schedule.

## Requirements
- Python 3.x
- `smtplib` and `email` libraries (standard in Python 3.x)
- Access to an email server (e.g., Gmail) for sending emails.

## Setup Instructions

### General Setup
1. Clone or download the repository to your local machine.
2. Open the script and fill in your email details:
   - `sender_email`: Your email address (used to send the reminders).
   - `receiver_email`: The email address where you want to receive the reminders.
   - `password`: The password or app password for your email account.

### Automated Execution Setup

#### For Mac Users
1. Convert the Jupyter Notebook (`automated_bible_reading_email_reminder.ipynb`) to a Python script (`.py`).
2. Open Terminal.
3. Use `crontab` to schedule the script:
   - Run `crontab -e` to edit the cron jobs.
   - Add a line in the format: `0 6 * * * /path/to/python /path/to/script.py` to schedule the script for 6 AM daily.
   - Ensure the path to Python and the script is correct.

#### For Windows Users
1. Convert the Jupyter Notebook to a Python script.
2. Open Task Scheduler.
3. Create a basic task:
   - Name the task (e.g., "Daily Bible Reading Reminder").
   - Set the trigger to daily at 6 AM.
   - Set the action to start a program.
   - In Program/Script, enter the path to your Python executable.
   - In Add arguments, enter the path to your script.
4. Save the task and ensure your computer is awake at the scheduled time.

## Usage
Once set up, the script will run automatically at the specified time each day, sending an email with the day's Bible reading plan.
