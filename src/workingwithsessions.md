# Working within a Session
## Things to Know before you Begin
A few things will happen immediately after the connection is established.
* The remote control window for the session will appear.
* You will be informed about the status of the running screen reader, or lack thereof, on the client's machine.
* If the client is running a screen reader, a toast notification informing the user that the remote session has begun will provide instant confirmation that the user's system audio is working.
* A Mac target will pop up the keyboard setup assistant if this is the first time a controller has connected to it.
    * This is for the Karabiner virtual keyboard, which listens to keyboard commands sent to it by a controller.
    * As such, you will want to walk the target computer through the setup assistant, because it will be listening for remote keyboard presses in the identification process, not the Mac's own keyboard.
* Last but not least, all keyboard and mouse input will immediately be directed to the target computer. To direct control back to your machine, do either of the following:
    * press Option+Shift+Backspace.
    * right click the RIM window's title bar.
    * left click the RIM icon.
<!-- end -->
## Remote Control Zone
At this point, you're all set to perform whatever tasks need doing on the client side. Should you need to switch back to controlling your own machine, bring up the RIM menu, then select the "Minimize session" option. You will be taken back to your machine until you switch back into the session window or press Option+Shift+Backspace again. When you go back into the session window, keyboard control will once again be directed to the client computer.  
Once you're done, either the controller or the target can go into the RIM menu and choose the "Disconnect Session" option. When the session ends, the target machine will get a toast notification informing them of this.
## The RIM Menu
As mentioned earlier, accessing the RIM menu directs you back to your machine. There are a number of options in this menu. They include:
* Update RIM on Target: Forces an update of RIM on the target computer
    * This option shows if the target's machine is running an older version of RIM
* Minimize Session: brings control back to your machine as described above
    * You can also use the shortcut Option+Shift+M to minimize the session.
* Transfer File to Target: Appears if a file is on the clipboard.
    * Although this alternate method of completing a file transfer is always available, it is only necessary for transferring files to Mac targets.
* Flip Session: Allows your client to remote control your machine and hear its audio. As the original controller, you can flip the session back by selecting this option a second time.
    * You can also use the keyboard shortcut Option+Shift+F to flip the session back and forth.
* Start/stop Voice Conversation: Allows you to toggle the voice chat on or off for your session.
    * Any mac that has this activated for the first time will initiate the permission request for access to the microphone. Once accepted, the voice conversation will begin.
    * Note that this option is unavailable in unattended sessions as they do not support voice chat. However, prompted sessions still support this.
* Start Remote Accessibility: This option appears when no screen reader is running on the remote computer. This will enable speech on your end, but the client will not need to worry about hearing speech.
* Reboot and Reconnect: Allows you to reboot the computer and automatically reconnect the session.
    * This feature is not yet implemented for Mac targets.
* Send Control+Alt+Delete: Sends this keystroke to the remote machine.
    * This option is not yet implemented for Mac targets.
* Request Unattended Access: Allows you to send a request for unattended access to the client computer. This is useful if you are a sysadmin and need to perform routine maintenance, or even for something as simple as controlling your home machine while on the go.
* Lock the Target Machine: Performs the equivalent of Windows+L or pressing the lock/power button on Mac OS.
    * Not yet implemented for Mac
* View Connection Details: Provides a detailed lowdown on your connection, as well as the target machine. Information includes:
    * Connection statistics
    * (soon to come) Information about the computer, including Mac OS version, available ram, etc.
    * (soon to come) Running processes
    * (soon to come) Installed packages
* Disconnect Session: Terminates the session.
    * Remember that this option is available to both sides of the session.
    * This is also possible via the keyboard command Option+Shift+D.
<!-- end -->

## File Transfers
RIM provides a simple avenue for transferring files, irrespective of platform used.
1. Bring up the RIM menu, and click on "Minimize Session." Control will be directed back to your computer.
1. Select the file(s) and/or folder(s) you want to transfer using your file manager.
1. Copy the selected contents to the clipboard in the usual way. You will receive a notification that a file is ready to be transferred. You have two options.
    1. If the target is a Mac
        1. Activate the RIM session menu, and click on the "Transfer File to Target" option.
        1. Upon completion of the transfer, the target Mac will generate a temporary directory containing the transferred contents. These should then be copied and pasted to their intended directories.
    1. If the target is a Windows machine:
        1. Switch back to the remote session, and locate the folder on the target machine where you wish to paste the content.
        1. Last but not least, paste as you normally would, remembering to use Control+V if you are controlling Windows from your Mac.
<!-- end -->
Note that the transfer time will depend entirely on the size of the content being sent as well as your network speed.
## Remote Accessibility Module
Whether you're assisting a user who doesn't use a screen reader, or you're diagnosing an issue with a malfunctioning screen reader, RIM is fully prepared to come to your aid. The remote accessibility module is a special configuration initiated on the target Mac at the request of the Windows or Mac controller. The advantage to this approach is that the end user does not hear speech on their computer while you're controlling it. Instead, the Remote Accessibility Module pipes the speech output through to the speech system on the controller side. This way, you can accessibly assist an end user without them having to enable a screen reader.
### Setup Procedure
For first-time initialization of the accessibility module, here is what you will need to do:
1. Bring up the RIM menu.
1. Select the "Start Remote Accessibility" option.
1. If you're using a Windows controller, you will be taken through the process of setting up the NVDA addon for remote accessibility.
1. By now, the remote accessibility module will be fully initialized, and you will hear speech output as you control the remote computer.
<!-- end -->
From this point forward, if you are running a screen reader on the controling computer, the remote accessibility module will automatically start during remote sessions in which the remote computer does not have a screen reader running.
## Rebooting and Reconnecting (not yet implemented)
Whether you're installing system updates or working your way out of a system hang, RIM has got you covered during the reboot process. Selecting the "Reboot and Reconnect" option off the RIM menu will allow you to either perform a graceful reboot or an emergency reboot, depending on what state the computer is in. While the computer is rebooting, RIM will inform you that reconnection attempts are being made.  
Note that if the computer is rebooted by a software installation or manually rebooted in the usual way, you will be asked if you wish to reconnect the session.
## Unattended Access
RIM allows you, as the controller, to configure machines for unattended access. This allows you to provide remote assistance without the user having to launch RIM, enter a keyword, or even be near the computer. This is useful if you are a sysadmin performing routine maintenance on computers in your workgroup. You may also want to allow this for your home computer should you need to access it from someplace else.  
There are a few ways to configure machines for unattended access.
### During an Interactive Session
1. Bring up the RIM menu.
1. Select "Request Unattended Access."
1. You will be asked to give this machine a name. Enter a personal name for the machine, or if applicable, the machine ID as it appears in your workgroup.
1. Press enter.
1. On the client machine, a dialogue pops up asking the user if they're fine with their computer being set up for unattended access. If they answer yes, then you will get a prompt informing you that unattended access has been approved.
<!-- end -->
### Registering a Machine to your RIM account
Should you wish to register one of your own machines for unattended access, you can do so without having to start an interactive session with the machine. 
1. Start RIM in Receive Help Mode.
1. Click on the "Add this machine to your RIM account" button.
1. Enter your email, then click next.
1. Wait for the two-step login code to arrive, enter it, then you should be logged in.
1. You will be asked what type of access you would like configured for this machine. Your options are:
    1. Unattended: Allows sessions to be initiated without any intervention whatsoever from the end user.
    1. Prompted: This configuration presents the user with a prompt informing them that you are conecting to their machine. They will need to press *Option+Shift+Y* on Mac OS, or *Windows+Shift+Y* on Windows, should they wish to accept the connection.
1. Give the machine a name, then activate the "Add Machine" button.
1. The machine will be registered to your account, which will allow any controller machines logged into your RIM account to connect to this machine.
<!-- end -->
### Getting Connected
Now that we've registered the machine for unattended access, here is how we will start a session.
1. Start RIM in controller mode.
1. Rather than entering a keyword, locate and activate the"Choose a machine" button.
1. When you click this, a list of machines will appear. Choose the one you want, then hit enter. You may also use the search bar to narrow the list down to a specific machine.
<!-- end -->
If the target machine is configured for prompted access, the end user will get a prompt. Once they answer yes, you'll be connected. If the session is unattended, you will immediately be connected and dropped into the remote control zone.  
Please note: Voice conversations are not supported during fully unattended sessions.
### Creating a Shortcut for an Unattended Session
For extra convenience, you can create desktop shortcuts that allow you to automatically launch unattended sessions. In order to do this:
1. Access the list of unattended computers, and select the one you want to create a shortcut for.
1. Click on the "Create Shortcut" button.
1. A shortcut will be automatically added to your desktop.
<!-- end -->
Now, when you activate this shortcut, you will either automatically land in the remote session, or send a prompt to the user's machine that they can accept.
#### More Ways to use Unattended Session Shortcuts
Unattended session shortcuts, like any other shortcuts, can have global hotkeys associated with them. This can be extremely useful if you are a maintenance tech managing multiple computers in a workgroup. For example, if your workgroup consists of 6 computers that you perform routine maintenance on, you could configure Alt+Control+1 through 6 as hotkeys for each respective machine. This ought to significantly speed up your workflow.  
### Revoking Unattended Access
If you no longer want your machine to be controlled unattended, you can revoke the controller's access. You do not need to be in a session in order to do this.
1. Access the Remote Incident Manager icon in your menu extras/status menus.
    1. If using VoiceOver, press VO+M twice, then locate the Remote Incident Manager menu icon.
1. Click this icon, or press VO+Space.     
1. Select the "Revoke Unattended Access" option.
1. You will arrive at a list of computers, select the one you want to revoke.
1. You will be asked if you wish to revoke the machine; answer yes.
<!-- end -->
That's it! The controller will receive a message stating that this machine is no longer available for unattended access. Should they need unattended access again, they can reinitiate the procedure to request permission for unattended access as described above.
# Key Command Reference
Action | Command
--- | ---
Activate RIM Menu | Option+Shift+Backspace
Minimize Session | Option+Shift+M
Flip Session | Option+Shift+F
Disconnect Session (Controller or Target) | Option+Shift+D
Accept Incoming Connection Request | Option+Shift+Y
Decline Incoming Connection Request | Option+Shift+N
<!-- end -->