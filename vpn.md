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
<img width="613" alt="Screenshot 2024-02-11 at 1 45 02 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/f2dd79e5-e6db-4329-8e38-8c2fd563b11a">
 
4. Create a new key pair (optional).
<img width="608" alt="Screenshot 2024-02-11 at 1 45 59 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/1d33a01d-add2-49b8-9852-da606d7c7f8c">
 
5. Create a username and password by connecting to the server.
<img width="610" alt="Screenshot 2024-02-11 at 1 46 34 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/241b7941-199d-4816-9c9d-491dcec4a5fa">

6. After the terminal window opens, press 'yes' for the agreement. Continue pressing 'enter' to confirm all default settings. Enter password. No need to specify activation key, just hit 'enter'.
<img width="622" alt="Screenshot 2024-02-11 at 1 47 19 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/be5ddf33-00c6-4ce0-9def-548f041db438">

7. You have successfully created a username and password!
<img width="593" alt="Screenshot 2024-02-11 at 1 47 54 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/722c453c-3951-41fc-b53b-bd4bdf917676">
   
8. Configure VPN settings in the admin panel by copying the Admin URL and entering it in a new tab in your internet browser. Press advanced and proceed to the site.
<img width="610" alt="Screenshot 2024-02-11 at 1 48 39 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/e4ca594e-ce32-4a45-b6df-e038fb4b3306">

9. Enter the username and password you just created. Accept the license agreement once logged in.
<img width="512" alt="Screenshot 2024-02-11 at 1 49 13 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/232f9733-14f5-465b-be19-b3a4cf7ce02a">
   
10. Go to the VPN settings.
<img width="632" alt="Screenshot 2024-02-11 at 1 50 07 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/dce86ded-01c1-448b-ba95-aa5eab5749ca">

11. Scroll down to routing section and toggle 'yes' for 'Should client Internet traffic be routed through the VPN?'.
<img width="626" alt="Screenshot 2024-02-11 at 1 50 48 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/3bdace18-0ade-436f-8c91-109f71394237">

12. Enable 'yes' for 'Have clients use specific DNS servers'.
<img width="617" alt="Screenshot 2024-02-11 at 1 51 27 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/3f74db28-0510-4892-9e7c-5f65371cce81">

13. Enter Google for fast response and save settings.
<img width="619" alt="Screenshot 2024-02-11 at 1 52 07 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/52268240-9fe7-48af-8a41-7e40071f9bbb">

14. Click 'Update Running Server'. You will have successfully configured VPN settings!
<img width="592" alt="Screenshot 2024-02-11 at 1 52 32 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/8e3a9639-3bda-41eb-ac9a-7f8419a10399">

15. Download and install the [OpenVPN app] (https://openvpn.net/client/) on your device.
<img width="620" alt="Screenshot 2024-02-11 at 1 53 04 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/8ad38c0c-c58e-4adb-a355-5de6a307154c">

16. To import profile, go back to terminal and paste the Client address.
<img width="612" alt="Screenshot 2024-02-11 at 1 53 36 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/b2002fdf-eb4a-4229-9a2e-38a2514bcb63">

17. Click 'accept'.
<img width="612" alt="Screenshot 2024-02-11 at 1 53 59 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/6d143c8a-bd49-4672-83ff-c64819aa5f7f">

18. Enter the username and password you set. You can also change the profile name if you prefer.
<img width="328" alt="Screenshot 2024-02-11 at 1 54 53 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/1f84af3b-ec80-46bb-b2ee-de5787fca386">

19. Click toggle and enter the password.
    
<img width="495" alt="Screenshot 2024-02-11 at 1 55 21 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/e5bbfb05-77e7-45b6-84f9-0225fbc6a60e">

20. You should have a working VPN!

<img width="406" alt="Screenshot 2024-02-11 at 1 55 54 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/96b7f446-2cc2-4f03-93a6-908269af172a">

21. To check and see if it is working, you can Google "What is my IP?". It should match with your Public IP.
    
<img width="403" alt="Screenshot 2024-02-11 at 1 56 20 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/600b8a02-7b91-4585-93a7-de36d3f59c58">

