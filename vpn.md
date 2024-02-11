---

title: "Setup a VPN Server Using OpenVPN on AWS"

author:
- Nancy Uddin
meta: "vpn"
permalink: /vpn/
---
  ## Setup a VPN Server Using OpenVPN on AWS

### Storytime: When I was visiting Istanbul, there was an alleged terrorist attack and the Turkish government responded by restricting social media platforms. I was cut off from communication with my family back home in New York City. My solution was to launch a **Virtual Private Network (VPN)** on cloud infrastructure. VPNs are cybersecurity tools that encrypt your internet connection. It helps to protect your privacy and security when you're online. I was able to call my mother on Whatsapp and let her know I was alright. Applying cybersecurity theory to real life saved me. 

Follow the steps below to learn how to launch your own VPN on AWS. 

1. Launch and name an EC2 instance.
2. Select OpenVPN from AWS Marketplace AMI.
3. Select t2.micro, which has the Free tier eligible plan.
4. Create a new key pair (optional).
5. Create a username and password by connecting to the server.
6. After the terminal window opens, press 'yes' for the agreement. Continue pressing 'enter' to confirm all default settings. Enter password. No need to specify activation key, just hit enter.
7. You have successfully created a username and password!
8. Configure VPN settings in the admin panel by copying the admin URL and entering it in a new tab in your internet browser. Press advanced and proceed to the site. 

