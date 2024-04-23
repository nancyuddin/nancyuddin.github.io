---

title: "Exploring Low Code Tools to Build a Creative Web Application on Google Cloud"

author:
- Nancy Uddin
meta: "ifimustdie"
permalink: /ifimustdie/
---
## Inspiration
I was raised in a community where discussions about death were often avoided, leaving me unprepared for the impact of my father's passing. Navigating this experience was both traumatic and cathartic because it inspired me to build *If I Must Die,* a virtual death conscious web application. *If I Must Die,* aims to destigmatize conversations about grief and experiences related to dying or the loss of a loved one. The questions in the activity aim to encourage deep introspection, emotional intelligence, and meaningful conversations about death and its connection to our lives. They can prompt individuals to confront, reflect, and engage with their mortality in deliberate and innovative ways.

## Cloud Architecture Steps

I set up an [Apache web server on a Linux VM](https://cloud.google.com/compute/docs/tutorials/basic-webserver-apache) and accessed it via SSH to edit the code. Despite lacking prior coding experience, I utilized [Google AI Studio](https://ai.google.dev/aistudio/?utm_source=aistudio.google.com&utm_medium=referral&utm_campaign=logged_out), a low-code tool, to assist in development. By describing my vision for [*If I Must Die,*](http://ifmustdie.com/) Google AI generated code for me to test and refine. I leveraged my understanding of Linux commands and file paths to organize the site effectively. Finally, I purchased a domain from GoDaddy and configured DNS settings using the DNS API on Google Cloud.

## Security

Multi-factor authentication (MFA) enhances security by requiring users to provide two or more verification factors to access an account. I set up MFA In Google Cloud by enabling it in the IAM & Admin section of the Google Cloud Console and following the prompts to link a second factor, such as a mobile device, to the account for authentication. A firewall is a network security system that monitors and controls incoming and outgoing traffic based on predetermined security rules. I defined firewall rules in the VPC Network section of the Google Cloud Console to allow HTTPS/HTTP requests to and from the virtual machine instance.

## Challenges

Optimizing resources while ensuring availability and performance presented me with challenges.I experimented with solutions like Google Cloud Storage to maintain instance availability while reducing costs and tinkered with configuring network load balancers. I faced extensive troubleshooting due to configuration issues or inconsistent CSS availability. 

## My Learnings

Ultimately, using Google AI to catapult my first creative web application and enhance my cloud computing skills has shown me AI’s potential to close the tech gap. It has become not so much how much you know, but how much you can learn with new technologies, the open source community, and the process of troubleshooting with persistence and care. I am excited to unveil a minimum viable product; as I iterate and evolve, I envision shaping *If I Must Die,* into a comprehensive death education resource for my community. 

