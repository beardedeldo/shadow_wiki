PART 1: 

1) If you have loopback on your router/modem, enable it. Keep in mind loopback won't work on your router/modem if you have CTF (Cut-Through Forwarding) enabled. If you can't disable it to allow loopback, follow option 2 instead.

2) If you don't have loopback follow the steps below on the machine you are going to play the game on.

2.1) Open Device Manager
2.2) Select Network Adapters
2.3) Open Action menu
2.4) Select Add legacy hardware, click Next
2.5) Select Install the hardware that I manually select from a list (Advanced), click Next
2.6) Select Network adapters, click Next
2.7) Select Microsoft in the left pane
2.8) Select Microsoft KM-TEST Loopback Adapter in the right pane, click Next:
2.9) Click Next and Finish until the installation is done
2.10) Type "Network Connections" in windows search bar and click "View network connections"
2.11) Right click on "Microsoft KM-TEST Loopback Adapter" (it's under descriptions not main name) and click properties
2.12) Scroll down to "Internet Protocol Version 4" and double click it
2.13) In the window that opened press "Use the following IP address" and enter your PUBLIC IP not 192.168 one
2.14) Click "Subnet mask", it'll automatically put some stuff (255.255.255.0) in leave it like that
2.15) Click ok and close

PART 2: 

If your Game and Server is going to run on the same PC, ignore steps below you should be able to connect now, otherwise keep reading.
Separate PCs introduce another problem, what you need to do is UDP forwarding from your Game machine to Server machine. Steps below are to be followed on your Game machine.

1) Download this forwarding software https://aluigi.altervista.org/mytoolz/sudppipe.zip
2) Open a terminal and enter the command below (change path) then you should be able to connect.
"C:\sudppipe\sudppipe.exe" your_server_pc_local_ip 2001 2001
You need to run that program every time you are going to be playing and it needs to stay on

If it breaks: 
- Log into modem and find IPv4 Address for the Server 
- Open file location of the loopback shortcut, right-click, properties, open file location. 
- Open with notepad the batch file and update the IP address. 
