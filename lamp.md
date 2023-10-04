---

title: "Create and Deploy a WordPress Website on the Cloud"

author:
- Nancy Uddin
meta: "LAMP"
permalink: /lamp/
---


Hosting a web application on the cloud ensures scalability, high availability, and cost-efficiency. 
In this lab, I will demonstrate the steps I took to host a WordPress website with a LAMP stack with AWS. AWS (Amazon Web Services) is a comprehensive and widely-used cloud computing platform offered by Amazon, providing a range of cloud services such as computing power, storage, databases, machine learning, and more to help businesses scale and innovate. 

**LAMP stack** is a popular foundation for web applications. 
**Linux** is the operating system (OS) on which the web server runs. 
**Apache** is the web server software that handles HTTP requests from clients (such as web browsers) and serves web content in response.
**MySQL** is a relational database management system (RDBMS) that stores and manages the structured data used by web applications.
**PHP** (Hypertext Preprocessor) is a server-side scripting language used for web development.

#### Launch a virtual computer with AWS

1. Launch an EC2 instance (virtual computer on the cloud). Enable SSH, HTTPS, and HTTP.
   <img width="814" alt="Screenshot 2023-10-04 at 2 03 02 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/a0a84890-4280-4847-bb3d-f03987dc9a54">
  </br> <br/>
  
2. Assign an Elastic IP so the IP address is static and the DNS server knows where the website is hosted.
<img width="805" alt="Screenshot 2023-10-04 at 2 04 14 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/bcbaa8f0-d62b-43d4-898b-8c4d07eda440">
</br>
3. Associate the Elastic IP to the EC2 instance.
   <img width="806" alt="Screenshot 2023-10-04 at 2 17 00 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/d4e438b5-45a6-4510-8017-ac5b102c1dd3">
</br>

#### Install and configure a web server and database management system

4. Connect instance with SSH and install and start Apache web server to EC2 instance with ```sudo apt-get install apache2```.
<img width="606" alt="Screenshot 2023-10-04 at 2 21 14 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/4b07bb63-d82b-4a2e-8c8a-5c40492f030b">
<img width="823" alt="Screenshot 2023-10-04 at 2 21 55 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/529204d1-aec1-4cd2-ab73-8d38950cad12">
</br>
5. Verify your web server by loading the Apache default page by typing in ```http/[Your Public IP address]```.
<img width="809" alt="Screenshot 2023-10-04 at 2 24 13 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/4745b172-188e-4421-b565-125218fe05d6">
</br>
6. WordPress is built on PHP so install PHP runtime on the instance.
   <img width="793" alt="Screenshot 2023-10-04 at 2 25 10 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/5f4a5648-57bb-425c-ba5f-b08a439d5ea2">
   </br>
7. Install the MySQL server for the database.
   <img width="631" alt="Screenshot 2023-10-04 at 2 26 04 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/3b515da7-0812-4518-9b2a-3fa04bffc75d">
   </br>
8. Log in to MySQL prompt with the root user.
   <img width="782" alt="Screenshot 2023-10-04 at 2 26 49 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/348d34da-1392-4c5f-a42a-c0e97c1be824">
   </br>
9. Change the authentication plugin to a MySQL native password to be able to log in to the MySQL server with your chosen password. 
<img width="817" alt="Screenshot 2023-10-04 at 2 27 45 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/caf6375d-ed3e-480b-afab-b3639dd06a83">
</br>
10. Create a user other than root and create a new database. Grant privileges to the user.
    <img width="770" alt="Screenshot 2023-10-04 at 2 28 49 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/6085a207-6f5e-437b-9f79-369df76fffc4">
</br>
#### Install WordPress

11. Download WordPress file from the WordPress site and download it in Terminal with ```wget```.  
<img width="799" alt="Screenshot 2023-10-04 at 2 30 59 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/b870ae0e-fe54-4d61-8451-014603b4c95c">
</br>
12. Unzip the downloaded file.
    <img width="575" alt="Screenshot 2023-10-04 at 2 31 28 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/bda4f0e4-15df-47a9-bb76-22a4ebd4b705">
    </br>
13. Move the folder to the document root of Apache.
<img width="790" alt="Screenshot 2023-10-04 at 2 31 58 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/9a07b8a6-a26d-4b32-a51b-8335d34b5261">
</br>
14. Enter WordPress site with ```http/[Your Public IP address]``` and configure the database.
<img width="817" alt="Screenshot 2023-10-04 at 2 33 15 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/8583f0b6-aa73-4aa0-b92f-3067c1f4aae1">
<img width="720" alt="Screenshot 2023-10-04 at 2 33 43 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/f3ed43bb-24dc-4a04-b2da-02600f798921">
<img width="814" alt="Screenshot 2023-10-04 at 2 33 59 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/cf52dc40-2c3b-41d0-828d-432f558d0d77">
</br>
15. The root path or the root directory serves the Apache to Default page. To serve Wordpress website at this root path of, modify the Apache configuration. In Terminal, ```cd etc apache 2``` and find a file that says ```000default.conf```. Open up a text editor such as nano editor and change this document root to ```/var/www/html/wordpress```. 
<img width="812" alt="Screenshot 2023-10-04 at 2 34 47 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/b0c6418f-cfc0-4390-a31d-7e305c2dbbfb">
</br>
#### Connect a domain name to the created site

16. I purchased a domain, but you can get a free one [online](https://www.forbes.com/advisor/business/free-domain-name/). Go to your domain DNS settings and add ‘A’ type record which points to your public IPV4 address. You can set the TTL to 60. 
<img width="782" alt="Screenshot 2023-10-04 at 2 37 44 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/ce1490f1-3d17-476f-bcc0-07178218cda0">
</br>
17. Add two new fields in the configuration file. The ServerName is going to be the ```domain name``` and ServerAlias is going to be ```www.[Sample website]```.
<img width="813" alt="Screenshot 2023-10-04 at 2 39 43 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/724094df-bcdb-4352-95d4-37bda5bd52b9">
</br>
18. Install Certbot to make it secure. 
<img width="819" alt="Screenshot 2023-10-04 at 2 40 22 PM" src="https://github.com/nancyuddin/nancyuddin.github.io/assets/119987538/89ce4431-fbeb-490f-8fe4-07e5033f333a">
</br>
**Congratulations you should now have a working WordPress site!**










