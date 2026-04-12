# Resilient and Scalable Web Application Deployment on AWS
This project is about building a secure, scalable, and highly available web application on AWS.
The architecture is designed in a way that the application can handle high traffic and still work without downtime.
It uses multiple AWS services and Availability Zones to ensure better performance and reliability.
# Project Objectives
# • High Availability:
The application runs in multiple Availability Zones so it stays available even if one zone fails.
# • Scalability:
Auto Scaling is used to automatically increase or decrease servers based on user traffic.
# • Security:
Security Groups and proper network settings are used to keep the application safe.
# • Resilience:
The system can handle failures and traffic spikes without manual intervention.
# Virtual Private Cloud (VPC)
<img width="3658" height="2625" alt="VPC" src="https://github.com/user-attachments/assets/ed23bffe-db95-43c7-bc84-2afcbb0c70ce" />
 # Step 1: Create the VPC

 ► First, I went to the VPC Dashboard in the AWS Management Console and clicked on ‘Create VPC’. 

 ► Then, I gave a name to my VPC, for example ‘My Project VPC’, so that I can easily identify it.

 ► After that, I defined the IPv4 CIDR block as 192.168.0.0/24. This range provides private IP addresses for the resources inside my VPC.

 ► I did not select IPv6 because it was not required for my project.

 ► For tenancy, I selected ‘Default’, which means instances will run on shared hardware, helping to reduce cost.

 ► Finally, I clicked on ‘Create VPC’ to complete the setup.

<img width="1920" height="1080" alt="VPC-Project-1" src="https://github.com/user-attachments/assets/ee10d987-0845-4750-9ad7-74e64fbd3131" />

<img width="1920" height="1080" alt="VPC Project-2" src="https://github.com/user-attachments/assets/a247ba76-3f9d-41a4-82f5-6693ded90eb0" />


