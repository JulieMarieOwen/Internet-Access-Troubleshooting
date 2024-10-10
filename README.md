<h1>Help Desk Ticket: Internet Access Troubleshooting</h1>

<h2>Description</h2>
A user had the following issue:<br>
Hope you're all good. I've got a bit of a snag with my computer – the internet's playing hard to get. When I try to open my browser, it's just giving me a blank page like it's on a break or something.
I've checked the Wi-Fi, and it seems fine, but my computer's not on the same page, if you catch my drift. This has been going on for a while, and it's starting to cramp my style at work. Not really a tech whiz, so I'm not sure if it's a router hiccup or a computer glitch.
If you could give it a look and help me get back online, that would be awesome. I've got work to do, and the internet's kind of essential for that. Appreciate the assist!

<h2>Troubleshooting Process</h2>

- <b>Theory 1: Network Configuration issue: Ran the ipconfig command in the command line interface; Ipv4 and Default Gateway were correct</b>

- <b>Theory 2: Tested Network Connectivity: Pinged default gateway in command line interface and 4 packets were sent and received with 0 loss; pinged the IP address for Google.com (8.8.8.8), and 4 packets were sent and received with 0 loss; pinged domain name google.com and “ping request could not find host google.com. I checked the preferred DNS servers and changed them to 8.8.8.8. and 8.8.4.4 for Google. The internet then started working.</b>

<h2>Resolution</h2>

- <b> Resolution (Internal): The issue was due to a non-functional DNS server setting. I changed the preferred DNS servers to 8.8.8.8. and 8.8.4.4 which then resolved the issue. By changing the preferred DNS server to a reliable one, the computer was then able to resolve domain names correctly which then restored the internet connection.
- <b> Resolution (Client-Facing): The computer wasn’t able to connect to the internet because it wasn’t able to locate websites by their names (ex. Google.com). I fixed the service that allows your computer to look up websites by their name and now your internet is up and working!

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
