---

title: "Setup a VPN Server Using OpenVPN on AWS"

author:
- Nancy Uddin
meta: "vpn"
permalink: /vpn/
---
 

Storytime: When I was visiting Istanbul, there was an alleged terrorist attack and the Turkish government responded by restricting social media platforms. I was cut off from communication with my family back home in New York City. My solution was to launch a **Virtual Private Network (VPN)** on cloud infrastructure. VPNs are cybersecurity tools that encrypt your internet connection. It helps to protect your privacy and security when you're online. I was able to call my mother on Whatsapp and let her know I was alright. Applying cybersecurity theory to real life saved me. 

Follow the steps below to learn how to launch your own VPN on AWS. 

1. Launch and name an EC2 instance.
2. Select OpenVPN from AWS Marketplace AMI.
3. Select t2.micro, which has the Free tier eligible plan.
4. Create a new key pair (optional).
5. Create a username and password by connecting to the server.
6. After the terminal window opens, press 'yes' for the agreement. Continue pressing 'enter' to confirm all default settings. Enter password. No need to specify activation key, just hit 'enter'.
7. You have successfully created a username and password!
8. Configure VPN settings in the admin panel by copying the Admin URL and entering it in a new tab in your internet browser. Press advanced and proceed to the site.
9. Enter the username and password you just created. Accept the license agreement once logged in.
10. Go to the VPN settings.
11. Scroll down to routing section and toggle 'yes' for 'Should client Internet traffic be routed through the VPN?'.
12. Enable 'yes' for 'Have clients use specific DNS servers'.
13. Enter Google for fast response and save settings.
14. Click 'Update Running Server'. You will have successfully configured VPN settings!
15. Download and install the [OpenVPN app] (https://openvpn.net/client/) on your device.
16. To import profile, go back to terminal and paste the Client address.
17. Click 'accept'.
18. Enter the username and password you set. You can also change the profile name if you prefer.
19. Click toggle and enter the password.
20. You should have a working VPN!
21. To check and see if it is working, you can Google "What is my IP?". It should match with your Public IP. 

