# Change Log
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
