# Frequently Asked Questions
Here are answers to some common questions concerning RIM. When faced with an issue, please refer to this document whenever possible. If your question is not covered, please [Contact us.](https://pneumasolutions.com/contact/)
## Compatibility
### What Platform(s) are supported?
The initial release of the client is only going to target Windows, but Mac and other devices are definitely on our roadmap. Windows is by and large the easiest operating system to work with when developing a remote access infrastructure, so while it is entirely possible to support RIM on more platforms, the process of implementing support for said platforms may be more involved.
### Our company is still using Windows 7. Will RIM work under this configuration?
Yes, RIM supports Windows 7.
## Connection Information
### Generally speaking, how responsive is RIM?
The roundtrip latency during an RIM session is extremely minimal. Because we don't rely on a central service, most of the time your connections are direct from one computer to another - this is what is known as peer-to-peer. If your network configuration doesn't allow for peer-to-peer connections, we fall back to any number of relays located around the world rather than relying on one central server. Thus, even then your latency will still be farely minimal.
### Where are your relays located?
Currently, we offer relays in the following locations:
* U.S.
    * Virginia
    * California
* Teronto, Canada
* London, England
* Warsaw, Poland
* Bangalore, India
* Singapore
* Sidney, Australia
* Sao Paulo, Brazil
<!-- end -->

## General Session Troubleshooting
### The target machine to which I am connected doesn't respond properly to keyboard commands that work fine on my keyboard. What's going on?
This could be due to a conflict in keyboard layouts. On rare occasions, if a keyboard layout is different enough from your own it may confuse RIM. Should that occur, please contact us with a report containing information about the keyboard layout of both machines.
### After a computer is reimaged and has been reconfigured with the same computer name, is there anything that needs to be done to get RIM up and running again? 
Simply remove the machine from your account, reinstall RIM, then add the machine back into your account.

## Pricing and Payments
### So, getting help from a person over RIM is totally free, right?
You bet! The subscriptions and/or one-off payments are for individuals and organizations seeking to offer remote assistance. No need to worry about getting a subscription if you're the person receiving help. In fact, you do not even have to set up an account if you are merely receiving help.
### I don't really do remote assistance regularly, but I may be helping a friend or family member on occasion. Are there any options that don't involve a subscription?
Certainly! We do accommodate as many use cases as we can.
* Anyone can assist a user over RIM for free for up to 30 minutes a day. So if you need to help someone install some software, fix a problem real quick, or send over a few files, we've got you covered. These minutes don't have to be used in one sitting.
* There are, of course, going to be situations where a particular issue requires a little more time. Or maybe you're assisting someone learning a new piece of software and might be connecting on and off over the next few days. That's where our day passes and incident passes come in.
    * Incident passes allow you to connect to a single target as many times as is needed over a 24 hour period.
    * Day passes allow you to connect to multiple targets over a 24 hour period.
    * Packages of prepaid hours allow you to have a set number of hours available to be used entirely on your own time.
* You can accumulate several of these passes and hourly packages and use them whenever the time calls for them. If you have multiple day passes, for instance, you do not need to use them consecutively. Similarly, You don't need to use your prepaid hours in one session or 24 hour period.
<!-- end -->
### I purchased a package of prepaid hours. What happens to my free daily allotment?
Good news: Your free 30 minute daily allotment is not going anywhere! When you start a keyword-based session, RIM will start off by using your free 30 minute daily allotment. Your prepaid time will be used after your free 30 minutes is up.
### How long will my prepaid hours last? Are they tied in with my subscription?
Prepaid hours are entirely separate from your subscription. That being said, your prepaid hours will remain in your account for one (1) year past the date they were first used.
### How do I go about bringing RIM to the attention of my place of work?
We've assembled a [Self-Advocacy Kit](https://sak.getrim.app) (SAK). A packet of e-mail formatted letters you can send to appropriate individuals on behalf of yourself or an employee. For the record, RIM provides the same functionality as less accessible mainstream solutions. As such, RIM can replace an existing infrastructure, rather than be used alongside one. It is therefore considered a reasonable accessibility accommodation and should be provided to you by your organization. Accessibility isn't a favor, it's a right to inclusivity.
### What payment methods do you accept?
We process payments through Stripe, so we are able to directly accept Visa, Mastercard, Amex, or Discover. Additionally, Stripe can accept payments via Google Pay.
### How do these passes work? Does the clock start immediately upon payment, or on the day I initiate the session?
Passes only begin when the controller initiates the session. So if the target's machine fails on them requiring a trip to the shop and a same-day turnaround is not possible, you can simply hold off until the machine is back in good shape and your day pass will still be waiting for you.
### So this means these passes don't expire?
No. Rest assured that your accumulation of day passes will be waiting patiently for you to activate them whenever you're ready.
### What happens if I connect to another machine on the day an incident pass has been used?
That depends. If the machine is within your subscription, I.E. if you're accessing your home machine while on the road, then it's business as usual. Any other connections that aren't the initial target you connected to will work under the usual 30 minute allotment.
### I hold an active personal subscription. Would I still be able to assist a user outside the group of targets for up to 30 minutes, or via a pass?
Yes! Your 30 minute daily allotment is still present for any machine outside of your subscription. Additionally, acquiring a subscription does not replace any existing passes you may have.
### I have a personal subscription, and the target computer underwent a hardware upgrade. Will Rim count this as a machine switch?
Only if RIM needs to be reinstalled. So, while a hard drive upgrade or any other situation requiring a Windows reinstallation would be considered a machine switch, upgrading the ram would not.
### Our company bought the pro subscription, but we have two techs - one that does help-desk during the day, and a system maintenance tech that works in the evening. Would we be able to assign the evening sysadmin a controller seat?
Definitely. In situations where multiple technitions will be using RIM, we offer up to two (2) additional controller seats for $50 a month per seat - $500 a year per seat - to accompany the pro plan if needed. This will make it easier for multiple controllers at different workstations or offices to provide remote support.  
If you have multiple controller seats, you can purchase additional channels for them so that sessions can run simultaneously. Each additional channel is $50 a month, or $500 a year. 

## Security
### Are RIM sessions encrypted?
Yes. All sessions, be they direct peer-to-peer connections or connections using a relay, are encrypted end to end using Datagram Transport Layer Security (DTLS). This is the same technology seen in the HTTPS protocol that modern websites implement for security.
### Can Pneuma Solutions eavesdrop on sessions relayed by the public cloud?
No. Session key negotiation and encryption are performed end to end between the controller and the target. In other words, everything is encrypted before it even leaves your device. That way, the cloud service merely relays the data as is, making it impossible for the service to decipher the data.
### What measures have been taken to prevent remote code execution (RCE) vulnerabilities?
All RIM code which is exposed to input from the network is written in [memory-safe programming languages](https://www.memorysafety.org/docs/memory-safety/) including Rust and JavaScript.
### Is RIM HIPAA-compliant?
Yes. The best configuration in this case would be an on-premises deployment, so please [get in touch with us](https://pneumasolutions.com/contact/) if your use case depends on this.
### Do any ports need to be opened on the target or controller?
No and no.
### What connections would need to be allowed on a network in order for RIM to function?
When utilizing the public cloud, an https connection to <https://getrim.app> is required. In optimal cases this is enough for RIM to establish a peer-to-peer connection between the controller and the target. However, it helps to allow UDP connections through ports 19302 and 3478 (the standard STUN and TURN ports). This ensures that if a relay is being utilized, RIM will not have to fall back to a tcp connection on port 443.
### What background processes does RIM run, and are they light on system resources?
* rim-host-service.exe: target process
    * This is an always-on background process that runs by default as long as RIM is installed.
    * It is very light on system resources
    * It runs with maximum privileges for the purpose of elevating RIM when needed, I.E. when user account control or a similar secure screen appears during a session.
    * It downloads some components of RIM in the background so as to reduce installation time and file size.
    * It does not phone home for any other purpose
* Remote Incident Manager.exe: main executable
    * This process's background tasks depending on how the machine is configured.
        * Normally, Its purpose is to listen for and initiate automatic updates. It checks for updates every five minutes.
        * On unattended machines, it listens for and initiates unattended or prompted access connections requested by the controller.
    * Still fairly light on system resources
    * Phones home only with an anonymous machine ID. No personally identifiable information is ever transferred.
    *  Unattended access background processing can be shut down via the icon in the system tray for disabling unattended access. A controller deleting a machine from the unattended access group has the same result. However, the main process will still run in order to check for and download updates.
<!-- end -->
## Remote Accessibility Module
### Is there anything the target machine needs to configure for first-time use of the Remote Accessibility Module?
Not at all! There are no dialogue boxes, permission request screens or anything of the sort.
### Does the Remote Accessibility Module work on secure screens such as User Account Control?
Yes! Since the RIM host runs with elevated privileges, this allows us to leverage the Remote Accessibility Module for secure screens. Gone are the days of getting trapped in a user account control dialogue in the middle of a program installation!
### What is the minimum version of NVDA required for the client support addon?
The current minimum version required is 2021.3.
### Will the RIM Client Support addon run on a portable copy of NVDA?
Yes, and this includes secure screens since the RIM host process takes care of elevation.
### Can I use the Remote Accessibility Module with the Windows Store version of NVDA?
This is not possible due to the Windows Store version of NVDA not allowing the use of addons. You'll have to either use a portable version of NVDA, or have your IT install the standard version of NVDA on your machine.
## Unattended Sessions
### Are voice conversations supported during unattended sessions?
No. However, prompted sessions do support voice conversations.
### If I delete an unattended machine from my controller account, will it automatically revoke permission on the target?
Yes. Once an unattended target is removed, the change will be effective immediately. If the target machine is powered down or otherwise not connected to the internet, the change will be effective as soon as an internet connection is established on their machine.
### The target machine rebooted after installing updates and drivers, and it requires a password to log in. How does the session continue from here?
RIM will attempt to automatically reconnect the session if an installation triggers a reboot. You will also be able to Control+Alt+Delete into the login screen if the target machine requires that.
### I have multiple machines playing the part of the controller. Will the list of machines set up for unattended access populate across all machines?
Yes. The list of machines configured for unattended access is stored within your account, so it will populate automatically.
