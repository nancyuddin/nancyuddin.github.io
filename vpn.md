---

title: "Setup a VPN Server Using OpenVPN on AWS"

author:
- Nancy Uddin
meta: "vpn"
permalink: /vpn/
---
 

Storytime: When I was visiting Istanbul, there was an alleged terrorist attack and the Turkish government responded by restricting social media platforms. I was cut off from communication with my family back home in New York City. My solution was to launch a **Virtual Private Network (VPN)** on cloud infrastructure. VPNs are cybersecurity tools that encrypt your internet connection. It helps to protect your privacy and security when you're online. I was able to call my mother on Whatsapp and let her know I was alright. Applying cybersecurity theory to real life saved me. 

Follow the steps below to learn how to launch your own VPN on AWS. 

1. Log into AWS. Launch and name an EC2 instance.
   <img width="622" alt="Screenshot 2024-02-11 at 1 41 39 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/cbc872f6-5d5f-4d5d-a2e0-1d6054b0873d">

2. Select OpenVPN from AWS Marketplace AMI.
<img width="614" alt="Screenshot 2024-02-11 at 1 42 18 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/4ceb24f8-763c-4ff0-8de0-745aebd6d8fd">

   
3. Select t2.micro, which has the Free tier eligible plan.
5. Create a new key pair (optional).
6. Create a username and password by connecting to the server.
7. After the terminal window opens, press 'yes' for the agreement. Continue pressing 'enter' to confirm all default settings. Enter password. No need to specify activation key, just hit 'enter'.
8. You have successfully created a username and password!
9. Configure VPN settings in the admin panel by copying the Admin URL and entering it in a new tab in your internet browser. Press advanced and proceed to the site.
10. Enter the username and password you just created. Accept the license agreement once logged in.
11. Go to the VPN settings.
12. Scroll down to routing section and toggle 'yes' for 'Should client Internet traffic be routed through the VPN?'.
13. Enable 'yes' for 'Have clients use specific DNS servers'.
14. Enter Google for fast response and save settings.
15. Click 'Update Running Server'. You will have successfully configured VPN settings!
16. Download and install the [OpenVPN app] (https://openvpn.net/client/) on your device.
17. To import profile, go back to terminal and paste the Client address.
18. Click 'accept'.
19. Enter the username and password you set. You can also change the profile name if you prefer.
20. Click toggle and enter the password.
21. You should have a working VPN!
22. To check and see if it is working, you can Google "What is my IP?". It should match with your Public IP. 

