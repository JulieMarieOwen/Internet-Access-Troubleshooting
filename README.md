<h1>Help Desk Ticket: Internet Access Troubleshooting</h1>

<h2>Description</h2>
A user had the following issue:<br>
I need to use Skype for a meeting. I powered my computer on and launched Skype, but it just hangs there with that spinning thing spinning forever. Or, it will say “Unable to sign in, please check your internet connection”. It never did this before. Please help.

<h2>Troubleshooting Process</h2>

I confirmed what the user reported and also checked the internet browser to confirm there is no internet connection to this computer.

- <b>Theory 1: There is an internet connection issue.
both verified an internet connection issue. I went into Device Manager and looked at the network adapter – it said that the device was working properly.
I right-clicked on the adapter in device manager and checked the driver and it appears that the best driver for the device is already installed.
When I attempted to access Settings > Network and Internet, the window crashed (I tried multiple times)
I opened the Command Prompt as the administrator and ran sfc/ scannow. This did not fix the crashing issue.
I went into Command Line interface as admin and ran “ipconfig”. I saw that the IP address is an APIPA address (169.254.191.253)
When I attempted to release the IP address via Command Line, I received the message “An error occurred while releasing interface Ethernet: The RPC server is unavailable.”
I went to Windows Key > Run and typed in “services.msc” and I checked the DHCP client – it was not running.
I then went back to using the command line as administrator and used the command “ipconfig /release” and “ipconfig /renew” and this time it renewed the IP address.
I then check to make sure that the browser and Skype were connecting to the internet. Everything appeared to be working as expected.
I went back to Settings > Network and Internet, and the window no longer crashed.</b>

<h2>Resolution</h2>

- <b> Resolution (Internal): The DHCP client was not turning on; once I set this to run automatically and started the service, I was then able to release the current APIPA IP address and get a new one. Once that was done, the internet connection was back up and running and the user could then login to Skype.
- <b> Resolution (Client-Facing): There was a setting on your computer that needed to be turned on so that it would then have an address to access the network, internet, and log into Skype. I have turned it on, so you should be all set!

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
