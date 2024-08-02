# Reminder_Application_With_Notification_APP using python 
**Overview
**The Reminder Application is a Python-based program designed to help users set reminders and receive desktop notifications at specified times. It leverages multi-threading to allow multiple reminders to be set concurrently without blocking the main application. The notifications are handled using the plyer library, which supports cross-platform notification delivery.

**Features**
**User-Friendly Interface:**

Simple text-based interface that guides the user through setting reminders.
Prompts for delay time and reminder message are easy to understand.
Customizable Reminders:

**Delay Time: **Users can specify the time in seconds after which they want to receive the reminder.
**Reminder Message**: Users can enter a custom message to be displayed in the notification.
Cross-Platform Notifications:

Utilizes the plyer library to deliver notifications on Windows, macOS, and Linux.
**Multi-threading:**

Each reminder is handled in a separate thread, allowing multiple reminders to be active simultaneously.
The main application remains responsive and can accept new reminders while others are pending.
**Replay Option:**

After setting a reminder, the user is prompted if they want to set another one.
The application continues to accept reminders until the user decides to exit.
How It Works
**Initialization:**

The main function welcomes the user and enters a loop to continuously accept new reminders.
**Setting Reminders:**

The set_reminder function asks the user for the delay time in seconds and the reminder message.
It creates a Reminder object with these details and starts a new thread to handle the reminder.
**Reminder Handling:
**
The Reminder class's remind method is called in a separate thread.
This method sleeps for the specified delay time and then uses plyer.notification to display the notification.
**User Interaction:**

After each reminder is set, the user is asked if they want to set another reminder.
If the user inputs 'y', the loop continues; if 'n', the application exits with a thank you message.
