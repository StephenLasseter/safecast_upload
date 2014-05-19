safecast_upload
===============

Automation of bGeigie imports from MacOSX platform

With safecast_upload configured on your Mac, you need only to mount your
bGeigie SD card, wait a moment for it to signal that it is done processing,
and remove your SD card.  The program will then open api.safecast.org in your
default browser in order for you to review your uploads for submission.  This
is not a earth shattering tool, but it does automate the data import workflow
enough that it is practically plug-n-play.

## Installation and setup

1. Mount your bGeigie SD card and move all processed logs to ARCHIVE.  Unmount
     the card when you are finished.
2. Run the following from the command-line:
     `cp org.safecast.upload_safecast.plist ~/Library/LaunchAgents`
     `mkdir -p ~/Safecast/bin` 
     `mkdir -p ~/Safecast/config` 
     `cp upload_safecast ~/Safecast/bin`
     `cp upload_safecast.ini ~/Safecast/config`
3. Edit ~/Safecast/config/upload_safecast.ini with your custom settings.
4. Load the launchd configuation:
     `launchctl load ~/Library/LaunchAgents/org.safecast.upload_safecast.plist`

Enjoy and feel free to leave suggestions.
https://github.com/StephenLasseter/safecast_upload
