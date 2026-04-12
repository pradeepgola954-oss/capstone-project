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

  # Step 2: Create Subnets

 ► First, I went to the VPC Dashboard and clicked on ‘Subnets’, then selected ‘Create subnet’.

 ► I selected my previously created VPC from the dropdown list.

 ► Then, I created four subnets across two Availability Zones to ensure high availability.

 ► For the first subnet, I named it ‘Public_Subnet_1A’, selected the Availability Zone ‘ap-south-1a’, and assigned the CIDR block 192.168.0.0/26.

 ► For the second subnet, I named it ‘Public_Subnet_1B’, used the same Availability Zone ‘ap-south-1a’, and assigned the CIDR block 192.168.0.64/26.

 ► Next, I created a third subnet named ‘Private_Subnet_1A’ in Availability Zone ‘ap-south-1b’ with CIDR block 192.168.0.128
/26.

 ► Finally, I created the fourth subnet ‘Private_Subnet_1B’ in ‘ap-south-1b’ with CIDR block 192.168.0.192/26.

 <img width="1920" height="1080" alt="Private-Subnet-1A" src="https://github.com/user-attachments/assets/f0ecca98-6684-4072-a532-988c0843af0e" />

<img width="1920" height="1080" alt="Private-Subnet-1B" src="https://github.com/user-attachments/assets/46153418-e67d-4cd7-a148-9a48ddb0ca3b" />

.
<img width="1920" height="1080" alt="Public-Subnet-1B" src="https://github.com/user-attachments/assets/add77e3a-c311-49a8-bf13-c039cf088877" />

<img width="1920" height="1020" alt="Public-Subnet-1A" src="https://github.com/user-attachments/assets/89df6495-80ee-4f01-8d40-ed6c27fe2139" />

► This setup ensures that I have both public and private subnets distributed across multiple Availability Zones, which helps in achieving high availability and better 

 <img width="1920" height="1080" alt="Four- Subnet" src="https://github.com/user-attachments/assets/208b198e-5bcd-48cd-8e3a-82360b91390e" />

 # Step 3: Set Up Internet Gateway

 In this step, I created and attached an Internet Gateway to my VPC to enable internet connectivity.

► First, I went to the VPC Dashboard and selected ‘Internet Gateways’, then clicked on ‘Create Internet Gateway’.

► I provided a name, for example ‘IGW-Ap-South-1’, and clicked on ‘Create’.

► After creating it, I selected the Internet Gateway, went to the ‘Actions’ menu, and clicked on ‘Attach to VPC’.

► Then, I selected my VPC from the list and clicked on ‘Attach’ to complete the process.

► This allows resources in the public subnet to communicate with the internet

<img width="1920" height="1080" alt="8-Create-Internet-Getway" src="https://github.com/user-attachments/assets/94c5cf7c-367d-4d90-ade3-1b37861a6207" />

<img width="1920" height="1080" alt="9-Attach four VPC" src="https://github.com/user-attachments/assets/993cddd7-f784-47a2-a52b-fd712b4c36c7" />

<img width="1920" height="1080" alt="10-Attach Internet Getway" src="https://github.com/user-attachments/assets/768d422f-60f6-4499-8953-41efbc431ff9" />

# Step 4: Create Route Tables

► First, I went to the VPC Dashboard and selected ‘Route Tables’, then clicked on ‘Create route table’.

► I provided a name, for example ‘Main RT’, and selected my VPC from the dropdown list, then clicked on ‘Create’.

► After creating the route table, I selected it and went to the ‘Routes’ section.

► I clicked on ‘Edit routes’ and added a new route with destination 0.0.0.0/0, which represents all internet traffic.

► For the target, I selected the Internet Gateway that I had created earlier.

► Finally, I clicked on ‘Save routes’ to apply the changes.

► This configuration allows resources in the public subnet to access the internet.

<img width="1920" height="1080" alt="11-RT-For- Public" src="https://github.com/user-attachments/assets/29a0dbd0-5253-483b-b6a1-952646513544" />

<img width="1920" height="1080" alt="13-RT-four Public Add- Route" src="https://github.com/user-attachments/assets/f781e49f-6739-40b5-bb59-663d571fc265" />

<img width="1920" height="1080" alt="14-RT-foue-Public-Add- internat-Getway" src="https://github.com/user-attachments/assets/27c5076b-6f88-46e5-9e02-c1a51da9281c" />







 

