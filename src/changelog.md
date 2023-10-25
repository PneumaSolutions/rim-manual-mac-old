# Change Log
Versions of RIM will be denoted by headings at level 2. Substantial updates with several features for both platforms will be divided into Mac and Windows subheadings at level 3.
## 3.2.12
* Worked around a rare problem that could prevent the RIM app from connecting to the cloud service.
## 3.2.11
* Added a new button to the Connection Details window to request that the target machine send its RIM logs to Pneuma Solutions. Please only use this feature if requested by Pneuma Solutions.
## 3.2.10
* Fixed a problem that could cause RIM to stop working until the next application restart if the machine's Internet connection is temporarily unavailable.
## 3.2.9
* macOS: We are unfortunately no longer able to offer automatic stereo microphone input in voice conversations on this platform, because in some cases, this prevented microphone input from working at all on a Mac. Note that this change has no effect on captured audio output from the target machine; that is still stereo.
## 3.2.8
* macOS: Fixed a bug that prevented RIM from coming up when activating the application through the Finder or Dock, rather than using the global hotkey.
## 3.2.7
* Voice conversations now automatically use stereo when the audio hardware supports it. This is useful when using RIM for training in audio production.
## 3.2.6
* Fixed a recently introduced problem that could prevent RIM from working on a fresh operating system installation.
## 3.2.5
* Fixed the message that displays remaining free time.
## 3.2.4
* Localization of RIM into other languages is now in beta. The following languages are currently supported: German, Spanish, French, Italian, and Swedish. To use RIM in one of these languages, press the "Language (BETA)" button at the bottom of the "Provide Help" or "Receive Help" window, then choose your language from the drop-down list and press the "Switch Language" button. We look forward to your feedback.
## 3.2.1
* The process of starting a new RIM session on the controller side is now smoother. The original window, where you entered your keyword or chose a target machine, will not go away until the main session window is ready. If the initial window no longer has focus when the session starts, e.g. if you switched tasks while waiting for the target user to enter a keyword, then RIM will notify you that the session is ready, and the main session window will appear when you return focus to RIM.
* macOS only: As part of the previous change, we modified the way that RIM adds and removes itself in the Dock and the Command+Tab list. Please let us know if you find any problems with the current behavior.
* Windows targets only: If a screen reader is started on the target machine while remote accessibility is active, then remote accessibility will quietly shut down to avoid double speech output.
## 3.2.0
First official release for Mac OS! New features include:
* ability to configure unattended or prompted sessions from within an interactive session.
* All new permissions instructions for users who are not using VoiceOver.
## 3.1.49
This version provides a consistent, cross-platform way of opening the RIM controller session menu with the mouse. A controller can either click the large RIM icon at the upper-left corner of the session window, or as was previously possible on Windows, they can right-click anywhere on the title bar.
## 3.1.48
### Mac
* Added support for the FN+Number key workaround for using the function row on MacBooks.
* RIM for Mac now customizes the menu bar, and in particular, the "About" option on the application menu now opens our own About dialog rather than the generic one.
## 3.1.47
### Windows
When connecting a Mac controller to a Windows target, with both sides using the same non-US keyboard layout, keyboard input from the controller wasn't being translated correctly. Version 3.1.47 for Windows fixes this problem.
## 3.1.46
* Added support for the new RIM Personal Community Support subscription package.

## 3.1.45
### Mac
RIM is now able to automatically resume capturing screen content and audio output if the target machine switches to the lock screen during a session.

## 3.1.44
### Mac
* Implements reboot and reconnect for Mac targets, including both standard and emergency reboots.
    * As with unattended access, RIM doesn't come up on the macOS login screen due to platform restrictions, particularly FileVault. So the target user will need to log back in before RIM can reconnect.
* The notification about file transfers, introduced in the previous update, is now shown only once per RIM session.
## 3.1.43
### Mac
* This update modifies the user interface for file transfers. When one or more files are placed on the clipboard on either side of the connection, the controller now receives a notification saying that the file transfer can be completed through the RIM menu. If the controller chooses this menu option, the file transfer is performed, and when done, a temporary folder containing the transferred file or files is opened on the destination machine. This method of file transfer is necessary when the destination machine is a Mac. When the destination is a Windows machine, the file transfer can be completed using either this new method or the old method of pasting in File Explorer on the destination machine.
## 3.1.42
### Mac
* RIM for Mac now works as an unattended target. It also performs updates in the background as the Windows version does.
    * We still have some work to do on access to the lock screen, and we don't believe we'll be able to provide access to the login screen before a user is logged in at all, due to limitations of the platform.
    * we haven't yet figured out how, or if, we'll be able to implement pre-configured target installers, so you'll need to use one of the other available methods of setting up unattended access.
* Eliminates one source of latency in audio captured from Mac targets.
<!-- end -->
## 3.1.41
### Windows
Fixed a problem that sometimes caused RIM to crash in response to activity on the Windows clipboard during a RIM session.
## 3.1.40
Adds some more logging related to audio on the target. So if you can reproduce laggy audio on the target, please do so with this version, then send logs. 
## 3.1.39
### Mac
This update adds mouse support for Mac targets.
RIM now requests permission to use macOS accessibility features. For new
installations, this replaces the input monitoring permission request, so
the total number of permission steps doesn't go up. But for updates,
you'll need to grant this permission before you can use RIM after updating.
## 3.1.38
### Mac
Fixed a crash that was affecting Mac targets at session initialization.
## 3.1.37
This update marks a major milestone in the Mac port of RIM. The remote
accessibility feature of RIM is now available when connecting to Mac
targets. Using a special configuration of VoiceOver on the target
machine, the controller, whether using Windows or Mac, will hear speech
while the target user does not hear any speech or sound effects. There
is also no visible indication that VoiceOver is running on the target.
The process of starting remote accessibility, either automatically or
manually, works just as it does with Windows targets. And of course,
when the session ends, the special configuration of VoiceOver is shut
down, and VoiceOver is restored to its previous settings.

Note that both Windows and Mac controllers now need to be running
version 3.1.37 to get full functionality when connecting to a Mac target.
## 3.1.36
### Windows
The remote accessibility feature is now compatible with NVDA 2023.1.
## 3.1.35
### Mac
* RIM now consistently uses stereo audio, particularly for Mac controllers.
* When using RIM for Mac as a controller with the remote accessibility feature, RIM now uses the voice and speaking rate as defined in the Spoken Content section of system settings.

## 3.1.34
### Mac
When a Mac controller connects to a Windows target that's not running a screen reader, you can now run the remote accessibility module on the Windows target and get speech output on the Mac controller. Note that you still need to use NVDA keyboard commands when interacting with the Windows target, not VoiceOver commands, and we're using the NVDA laptop keyboard layout. 
## 3.1.33
In response to user feedback, we removed the sound effect when displaying notifications about the status of a remote session.
## 3.1.32
### Mac
RIM now supports the Fn key when using a Mac laptop as a controller.  
Note that for the top row of function keys, RIM always treats them as F1 through F12, and you need to use the Fn key if you want to use these keys as system function keys (for adjusting volume and so on), regardless of how the system preference is set on either end of the connection. We figure that in a remote session, you probably want to use these keys as F keys most of the time anyway. Behavior like using Fn+Left Arrow to press Home works as expected.
## 3.1.31
### Mac
* RIM previously didn't let go of its lock on keyboard input when some dialogs were displayed, such as the dialog requesting permission to access the microphone. This is now fixed.
* When connecting from Mac to Windows or vice versa, it's no longer possible for the controller to trigger the RIM menu on the target machine. This fix requires the corresponding update to RIM for Windows.
### Windows
* Added a way to send RIM's log files to Pneuma Solutions, introduced for Mac OS in version 3.1.29. Please only use this function if requested by a representative of Pneuma Solutions.
* RIM now plays a sound whenever it displays a notification.

## 3.1.30
### Mac
RIM will now request permission to display notifications, both on first run and for existing users updating from a previous version. As with most other permissions, granting this permission requires flipping a switch in System Settings. We've also added our own sound for these
notifications.
## 3.1.29
### Mac
* We believe the problem that some users have reported with requesting keyboard input monitoring permission on machines running Karabiner Elements is now fixed.
* The RIM About dialog now has a button to send logs. Please only use this if requested by Pneuma Solutions.
## 3.1.28
### Mac
When using RIM as a controller, it is now compatible with advanced keyboard customization tools such as Karabiner Elements.
## 3.1.27
### Mac
This is a minor update, with just two changes:
* Marked RIM as requiring macOS 13.0 (Ventura) or later.
* Fixed RIM so the virtual keyboard is only connected when RIM is actually running as a target. This means that the Keyboard Setup Assistant won't appear when using RIM as a controller. We're still looking into possible ways to avoid that dialog altogether.
## 3.1.26
Initial beta build of RIM for Mac OS.
## 3.1.24
* When connecting to a target machine with lower display resolution or a higher dots-per-inch (DPI) scale factor than the controller, RIM now scales the remote target display to fit the controller's screen, making the remote display easier to work with visually.

## 3.1.23
* Added support for prepaid hours.

## 3.1.22
* Fixed a bug that sometimes caused RIM on the target machine to get into a loop that prevented unattended connections.

## 3.1.21
* Added a new keyboard shortcut, Windows+Shift+M, while in a session window, to minimize the window and return the keyboard focus to the local (controller) machine.

## 3.1.20
* Added logging that will help us diagnose reports of unattended targets being intermittently disconnected from RIM.

## 3.1.19
* Fixed some corner cases in remote keyboard input handling. In particular, when running JAWS on the target machine, JAWS now correctly recognizes Pause and NumLock key presses from the controller. Please let us know if you find any regressions in keyboard input handling, particularly for non-US keyboard layouts.

## 3.1.18
* Fixed a problem that prevented RIM from updating itself on target machines that were on the Windows Sign-in screen with no active user session.

## 3.1.17
* Since the previous update, we've received reports of the Shift modifier being stuck on the target machine when running JAWS. We believe this update resolves that problem. Please let us know if you continue to have trouble with stuck modifiers.
* Fixed a bug that caused RIM to shut down NVDA on the target machine at the end of a session if NVDA was started on the target machine after enabling remote accessibility.

## 3.1.16
* When running JAWS on the target machine with Unified Keyboard Processing enabled, JAWS now reliably responds to keystrokes from the controller.
* Fixed an error that sporadically occurs when starting the remote accessibility add-on after installing or updating the NVDA add-on on the controller machine.

## 3.1.15
* When you connect to a target machine with no running screen reader, RIM will automatically enable remote accessibility if you are running a screen reader on the controller machine. If you're running a screen reader other than NVDA on the controller machine, RIM will even automatically shut down that screen reader and start NVDA if you have it installed.
* Fixed issues that prevented the remote accessibility module from using your local NVDA configuration settings such as keyboard layout and typing echo.

## 3.1.14
* The process of re-establishing a connection when there is a connectivity issue is now more robust.
* Fixed a problem that sometimes caused RIM's background update process to stop.
* If the controller is running an older version of RIM than the target, the menu no longer includes an option to update the target.
* If a screen reader or RIM's remote accessibility module is running on the target machine, you can now stop it through an option on the menu.

## 3.1.13
* Fixed a bug that caused users to get logged out of RIM after installing some Windows updates.

## 3.1.12
* By popular demand, RIM no longer prompts for a comment at the end of each session. You can still post comments on sessions in the RIM Dashboard. We may add a configurable option to prompt for a comment as a feature in the future.

## 3.1.11
* If the target machine is running at least this version of RIM, but hasn't yet updated to the latest version, the controller can now force the target machine to update its installation of RIM through a new option on the session menu.

## 3.1.10
* You can now optionally add a comment at the end of a RIM session. Session comments can be viewed in the RIM Dashboard.
* The Connection Details window is enhanced. The statistics are updated live as long as the window is open, and the window now includes information about the target machine.

## 3.1.9
* Fixed a problem that sometimes caused a RIM session to get stuck trying to reconnect.

## 3.1.8
* Fixed a problem that sometimes prevented the remote accessibility module from starting.

## 3.1.7
* When choosing a target machine for an unattended or prompted session, you can now search through your target machines. To do this, on the Provide Help screen, press "Choose machine" as before, tab to the "Search" field, enter the text to search for, then either press Enter or press the "Search" button.

## 3.1.6
* Fixed a problem that sometimes made it impossible to interrupt JAWS speech on the secure desktop.
## 3.1.5
* Fixed a visual display bug that caused the list of unattended target machines to overlap with the buttons below it.
## 3.1.4
* Enterprise customers can now deploy RIM using an MSI-based installer.
## 3.1.3
* Fixed a bug that could cause RIM to crash if the RIM menu is open when a session is reconnected.
## 3.1.2
* Adjusted the visual style to be more accessible to low-vision users.
* Added error messages if required fields are left empty.
## 3.1.1
* When you press the "RIM Dashboard" button in the Provide Help window, that window now stays open.
## 3.1.0
This release adds a complete management dashboard for controllers.
* All subscribers have access to the dashboard, with feature sets determined by subscription tier.
* Removed the in-app functions for renaming, deleting, and creating installers for unattended machines as this is now part of the dashboard
* Brought back the welcome page.
## 3.0.8
Fixed a bug that sometimes prevented remote screen output from working when a User Account Control prompt was displayed.
## 3.0.7
* This is a bug-fix update.
## 3.0.6
* Users with either a RIM Enterprise subscription or a RIM Pro subscription with the Enterprise add-on can now create fully silent pre-configured installers for unattended access. To run an installer in silent mode, whether it's the standard installer or a pre-configured installer from an enterprise account, use the /S command line switch (note the capitalization) when running the installer.
## 3.0.5
* This is a bug-fix update.
## 3.0.4
* This update restores compatibility with Windows 7.
## 3.0.3
* RIM no longer mistakenly shows the "Create an Installer for Unattended Access" button if you don't have a subscription.
## 3.0.2
* If you have purchased one or more RIM passes, you now have control over whether a particular session will use a RIM pass or the free tier, as well as which pass will be used. RIM also tells you how much time is left on your selected pass.
## 3.0.1
* This update introduces support for the new RIM personal passes, which let you use RIM for remote technical support or training for up to 24 hours for as little as $10. [Try a RIM pass today.](https://getrim.app/signup/pass)
* The button that used to be called "Create a Pre-Configured Target Installer" is now called "Create an Installer for Unattended Access".
* When renaming an unattended target machine, the existing name is now filled in and selected for easy editing.
## 3.0.0
This release concludes the RIM public beta. RIM pricing plans and restrictions on free usage are now in effect. For free accounts, RIM now displays a usage meter along with a purchase button.
## 0.12.2
Fixed a bug that prevented the new Windows+Shift+Backspace hotkey from working in some situations.
## 0.12.1
* The Control+Shift+Backspace hotkey is no longer active in RIM. The official hotkey is now Windows+Shift+Backspace. Windows+Shift+Escape also remains available during a session.
* RIM's new main hotkey, Windows+Shift+Backspace, is now active at all times on machines where RIM is installed, unless another application claims the hotkey first. When a RIM session is active on the controller, this hotkey opens the RIM menu if the session window is focused, or focuses the session window if it's in the background. On the target, this hotkey opens the RIM target menu while the session is active. On either side, if a session is not active, this hotkey opens the RIM window to start a new session.
* When requesting unattended access, RIM now reliably focuses the approval dialog on the target machine.
* Updated the remote accessibility module.
## 0.12.0
You can now create a pre-configured installer that will automatically register all machines on which it is installed as unattended targets in your RIM account.

To do this, use the new button called "Create a Pre-Configured Target Installer", on the "Provide Help" screen. You will then need to enter a base name for the target machine(s); RIM will automatically add the host name of each target machine to this base name. Once target machines are registered, you can rename them as with any unattended target. You can also set the expiration date of the installer, which must be between 7 and 30 days. Once RIM has created the installer, you'll get a link that you can either share directly with the target users, or download yourself so you can share the installer some other way.

Note that when a target user runs the pre-configured installer, it will first show them a confirmation dialog which explains what the installer will do. This dialog includes the name of the controller who created the installer. This confirmation step is designed to prevent abuse. A completely silent mode will be available for enterprise customers.

## 0.11.6
* RIM now has a new option for registering a machine for unattended access under your RIM account without having to start a remote session using a keyword. On the machine that you want to register, press the new button called "Register This Machine for Unattended Access", on the Receive Help screen. Then log into your RIM account if you haven't already done so on that machine, enter a name for the machine, and you're done. Note that we're still working on a way to customize the RIM installer, to enable mass deployment and make it as easy as possible to set up unattended access on machines that you don't already have access to.
* RIM now prevents you from trying to open an unattended connection to the same machine where you're running the controller.
* We're now experimenting with a third hotkey to open the RIM menu: Windows+Shift+Backspace. That means there are now three options: Windows+Shift+Escape, Windows+Shift+Backspace, and Control+Shift+Backspace. We haven't yet made a final decision on which hotkey or hotkeys to keep, but we will decide before the end of the public beta. We appreciate your feedback.
* Most options on the RIM menu now have single-letter keyboard shortcuts that you can press once you've opened the menu.
* This update introduces a more reliable solution to the intermittent problems that users have reported with JAWS not recognizing keyboard input from RIM. Please let us know if you continue to have problems with this scenario.
## 0.11.5
* This update introduces two new hotkeys. Windows+Shift+D disconnects the session when pressed on either side. For the controller, Windows+Shift+F flips the session.
* This update adds safeguards against keyboard modifiers becoming stuck on either machine.
* There's a new menu option, "Lock the Target Machine", which is equivalent to pressing Windows+L on the target.
* RIM now has an "About" window, where you can check the version number, contact Pneuma Solutions for support and feedback, read the manual, and view the version change log.
* RIM no longer prompts for feedback at the end of a session or when closing the "Provide Help" window.
<!-- end -->
## 0.11.4
This update fixes a few bugs in the reboot and reconnect process. We haven't yet diagnosed everything that has been reported, but we were able to find and fix a few issues in our own testing.
## 0.11.3
* RIM now updates itself in the background on all machines. RIM now includes the currently installed version number in the tooltip of its tray icon. This is the last update users will need to install manually, irrespective of machine configuration.
* If the target machine is rebooted, but not using RIM’s Reboot and Reconnect feature, RIM now asks the controller whether they want to reconnect to the target after the reboot. If the controller answers no, then the target won’t wait for a reconnect after the reboot.
<!-- end -->
## 0.11.2
* RIM now updates itself in the background on unattended target machines. This is the last update that you will need to install manually on your unattended targets.
* When updating before an interactive session, RIM no longer needs to go through User Account Control. This means that non-administrator users can update RIM once it has been installed for them by an administrator.
## 0.11.1
This is a bug-fix update. Please note that unattended targets still need to be updated manually by running the latest RIM installer. However, now you will be able to connect to an unattended target after the installation is done, without requiring someone to close the "Receive Help" window.
## 0.11.0
* The Reboot and Reconnect feature is now implemented. Using the new Reboot and Reconnect option on the controller’s RIM menu, you can do either a standard or emergency reboot, and automatically continue the session when the reboot is complete. RIM will also reconnect if the target machine reboots for some other reason, such as when an installer reboots the machine.
* RIM also automatically attempts to reconnect if the connection drops for any reason. This will help with unreliable Internet connections.
* When running an unattended session or using Reboot and Reconnect, you can now use RIM while the target machine is on the Windows Logon screen. Note that RIM will need to reconnect the session when the target machine transitions from the logon screen to the main desktop. This is a known limitation of the current implementation which we may address in a future update.
* RIM is now fully functional when the target user does not have administrator privileges on the target machine, as long as the Remote Incident Manager Host service is running on that machine. Note that administrator privileges are still required to install RIM updates. Also note that new versions of RIM still need to be manually installed on unattended targets. We are working on solutions to both of these problems.
<!-- end -->
## 0.10.10.0
If you've set up unattended access to one or more target machines, you can now create a shortcut to directly access any of these machines. Just press the "Create Shortcut" button under the list of unattended targets, and RIM will create a shortcut on your desktop.
## 0.10.9
RIM now works on a target machine that has no audio device. This, combined with the existing remote accessibility module, opens up access to servers and virtual machines that could previously not be accessed with a screen reader except through RDP and its very suboptimal audio output.
## 0.10.8
* If you haven’t yet pre-ordered the first year of your RIM Pro subscription, you can now easily do so using the new button on the “Provide Help” screen. We are also introducing new pricing options for adding extra controllers and concurrent channels to a RIM Pro subscription. You can add up to two additional controller users and two additional channels for $500 per year each. RIM continues to be free during the public beta, but if you pre-order your subscription now, you will have uninterrupted service when the public beta concludes on September 1.
* We are introducing Control+Shift+Backspace as an alternative hotkey for opening the RIM menu on both sides of the connection. We also still support Windows+Shift+Escape for now, but the plan is to standardize on Control+Shift+Backspace as the one hotkey for all stages of RIM.
* If you press the “Provide Help Instead” button on the “Receive Help” screen, RIM no longer sets this choice as the default until you have logged into your RIM account.
* Fixed a few JavaScript errors that occurred in rare cases.
<!-- end -->
## 0.10.7
you can now use the mouse wheel in a remote session.
## 0.10.6
Hopefully fixed all remaining issues causing the installation process to hang.
## 0.10.5
This version includes some changes under the hood. In particular, we've included updates to the installation and underlying packages to address issues causing the installation to hang.
## 0.10.4
* There is now an option on the RIM menu to send Control+Alt+Delete to the target machine.
* You can now open the RIM menu by right-clicking on the title bar of the session window. We plan to add the option of opening the RIM menu by clicking on the RIM icon at the left end of the title bar as well.
<!-- end -->
## 0.10.3
* The controller can now flip an unattended session.
* The controller can now rename an unattended target machine.
* Fixed a bug that sometimes caused the session to become unresponsive after copying to the clipboard.
* Fixed a bug that sometimes caused starting the remote accessibility module to fail with a JavaScript error.
<!-- end -->
## 0.10.2
Fixed a conflict between the RIM Client Support NVDA addon and the Dropbox addon.
## 0.10.1
* You can now pre-order the first year of your subscription to RIM Pro for $999. The link to pre-order will be available in the feedback window when you finish a remote session. Or you can follow the direct link here: [Pre-order RIM Pro.](https://getrim.app/signup/rim_preorder)
* If you have unattended target machines in your RIM account, the button to start an unattended session is now more reliably displayed on the “Provide Help” screen.
* When flipping a session, the original controller can now flip the session back, by opening the RIM menu with Windows+Shift+Escape.
<!-- end -->
