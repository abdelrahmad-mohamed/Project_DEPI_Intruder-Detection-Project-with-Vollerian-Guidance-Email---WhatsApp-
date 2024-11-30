
# Intrusion Detection System

## Project Overview

This project is designed to monitor a specific location, such as a museum, factory, or any premises that remain inactive during specific hours (e.g., 12 AM to 7 AM). A camera continuously observes the area, and as soon as a person is detected with a clear view of their face and torso:
- A photo and a video are captured and saved.
- Alerts are sent to the owner of the premises via:
  1. Email
  2. WhatsApp

The alert contains:
- A warning message with the intruder's photo and video.
- Additional details such as:
  1. Time of intrusion.
  2. Number of people detected by the camera.

## Variables Configuration

To set up and use the code, you need to configure the following variables:

### Mandatory Variables
1. `EMAIL_ADDRESS`: Your email address.
2. `EMAIL_PASSWORD`: The app password for your email (see the **Note** below for details on obtaining this).
3. `PHONE_NUMBER`: The WhatsApp phone number to send alerts to.

### Optional Variables
These variables can be adjusted based on your needs:
1. `EMAIL_COOLDOWN`: The cooldown period (in seconds) between consecutive emails to prevent spamming. This ensures that even if the same person remains in the camera's view, emails are not sent repeatedly in quick succession.
2. `WHATSAPP_COOLDOWN`: Similar to `EMAIL_COOLDOWN`, but for WhatsApp alerts.
3. `VIDEO_DURATION`: The duration (in seconds) of the video recorded when an intruder is detected.
4. `MESSAGE_BODY` and `message`: These define the warning messages sent in the alerts.

## Note on EMAIL_PASSWORD

The `EMAIL_PASSWORD` is **not** your usual email password. To obtain this app-specific password, follow these steps:

1. Open your Gmail account and click on your profile picture.
2. Select **Manage your Google Account**.
3. Navigate to the **Security** tab.
4. Enable **2-Step Verification**.
5. Search for **App Passwords**.
6. Create a name for your project and generate an app password.
7. Copy this password and use it as the `EMAIL_PASSWORD` in the code.

