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
     1. `cp org.safecast.upload_safecast.plist ~/Library/LaunchAgents`
     2. `mkdir -p ~/Safecast/bin` 
     3. `mkdir -p ~/Safecast/config` 
     4. `cp upload_safecast ~/Safecast/bin`
     5. `cp upload_safecast.ini ~/Safecast/config`
3. Edit ~/Safecast/config/upload_safecast.ini with your custom settings.
4. Clone the Databot repo and copy export_safecast.py from it:
     1. `git clone https://github.com/bidouilles/Databot`
     2. `cp Databot/export_safecast.py ~/Safecast/bin`
     3. `chmod +x ~/Safecast/bin/export_safecast.py`
5. Check that you have all the required python modules installed.  If not,
     fetch them manually or with `pip`.
6. Load the launchd configuration:
     `launchctl load ~/Library/LaunchAgents/org.safecast.upload_safecast.plist`

Enjoy and feel free to leave suggestions.
[https://github.com/StephenLasseter/safecast_upload](https://github.com/StephenLasseter/safecast_upload)
