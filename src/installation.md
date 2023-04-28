# Installation
How you acquire and install Remote Incident Manager depends on your use case and configuration, but in any case the process is quite straight forward.
## Typical Installation for Individuals
There is only one installation package to use, whether you are offering or receiving assistance.
1. [Download Remote Incident Manager](https://download.pneumasolutions.com/rim/rimsetup.exe)
1. Go to your downloads folder via Finder (*Option+command+L*). Locate the downloaded .pkg file and open it with *Command+O*.
1. An installation wizard will appear. Follow the onscreen instructions.
<!-- end -->
You are all set to run Remote Incident Manager for the first time! You may run it from your applications folder, accessed via *Command+Shift+A* while located in Finder. Additionally, RIM sets up a multipurpose global hotkey (*Option+Shift+Backspace*) which, among other things, automatically launches the program from wherever you are.  

# Permissions
Due to Mac OS's precautionary behavior when dealing with applications of this nature for the first time, you will need to grant some permissions to Remote Incident Manager upon first launch.
## Karabiner HID driver
This is the driver that processes input that is received by RIM. This is a kernel extension, thus you must manually approve it. Rim will bring up a system dialogue that will take you to the Privacy and Security section of system settings. You will then want to scroll until you locate the Allow button. Clicking this will prompt you for your password or touch ID, after which you will be informed that you need to reboot in order to fully enable Karabiner Elements. Whether you reboot now or later is up to you, but should you decide not to reboot until all the permissions have been approved, exit out of System Settings and go back into RIM.
## Receiving Input
RIM needs permission to receive all the input directed to it over a remote connection.  
Click Continue in the RIM window, at which point a system dialogue requesting accessibility service permissions will appear. If VoiceOver does not immediately focus it, press *VO+F1* twice quickly. Then, down arrow to System dialogues, press right arrow, and then down to the keyboard permissions request. Pressing enter on that will open the alert box, at which point you will want to follow it to System Settings and check the Remote Incident Manager box in the list of applications.
## Capturing Screen Output
The next permission request from RIM will be for capturing the screen output which will be piped across the remote connection. The procedure for this is similar to the previous procedure.
## Notifications
The final permission request from RIM will be for notifications. RIM will notify you when a session starts and ends. The procedure for granting this permission is similar to the previous procedure.
## Welcome Screen!
After all the permissions have been approved, the welcome screen will appear. Note that if you chose to reboot later, now would be a good time to reboot.
At this point, RIM is ready to initiate or receive connections.