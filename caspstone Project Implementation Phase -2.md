<img width="3846" height="4425" alt="Final_Dia_CloudFolks_Capstone_1" src="https://github.com/user-attachments/assets/ae353b52-cd7a-49d7-93cd-1c3de9c23fe8" />


# Step 2: Create the Security Group

► First, I went to the VPC Dashboard in the AWS Management Console and clicked on ‘Security Groups’, then selected ‘Create security group’.

► Then, I gave a name to my security group as ‘EFS-SG Project-1’ so that it can be easily identified.

► After that, I added a description like ‘Secure-EFS-SG Project-1’ to describe its purpose.

► I selected the VPC ‘My Project VPC’ where this security group will be used.

► In the Inbound Rules section, I selected ‘All traffic’ as the type and allowed the source as 0.0.0.0/0 (Anywhere) to allow all incoming traffic (for testing purpose)

► Finally, I clicked on ‘Create security group’ to complete the setup.


<img width="1920" height="1080" alt="1-EFS-SG- Project-1" src="https://github.com/user-attachments/assets/05e0da30-c12b-4d2c-8a33-87ee0b98b0db" />
      


<img width="1920" height="1080" alt="2-EFS-SG- Project-1" src="https://github.com/user-attachments/assets/dbd9821e-3228-4ebe-82f9-4f45e00638dc" />

# Step 3: Elastic File System (EFS)

► I opened Amazon EFS from the AWS Management Console.

► Then, I clicked on Create file system to start the setup.

► I provided a name like “EFS-File-System” for easy identification.

► After that, I selected my existing VPC (My-Project-VPC).

► I kept the recommended settings as default.

► Finally, I proceeded to the next step.

<img width="1920" height="1080" alt="3-EFS-File-System" src="https://github.com/user-attachments/assets/2de2057b-c591-4383-a432-5e8bdd1b98a2" />

<img width="1920" height="1080" alt="4-EFS-File-System" src="https://github.com/user-attachments/assets/8485ff21-d5f2-4225-a347-51850587cd97" />

<img width="1920" height="1080" alt="5-EFS-File-System" src="https://github.com/user-attachments/assets/9e65e378-d118-42b8-9020-2732167f3d02" />

<img width="1920" height="1080" alt="6- EFS-File System" src="https://github.com/user-attachments/assets/d77a68c6-353d-4475-ba68-d7d62706066e" />


# Step 4: Launch EC2 Instance

► I opened the AWS Console and navigated to the EC2 Dashboard, then clicked on Launch Instance.

► I entered the instance name (e.g., Web-Server-AMI and EFS) and selected the Amazon Linux AMI.

► I chose the instance type (t3.micro) and selected or created a key pair for SSH access.

► In the network settings, I configured a security group allowing HTTP and SSH traffic, and keet the storage settings as default.

► I reviewed the configuration in the Summary section and clicked on Launch Instance.

<img width="1920" height="1080" alt="7-Web-Server-AMI and EFS" src="https://github.com/user-attachments/assets/6ae314ba-566e-4131-aa09-cec210814aec" />

<img width="1920" height="1080" alt="8-Web-Server-AMI and EFS" src="https://github.com/user-attachments/assets/f70c92fb-4254-4633-a26e-d0e7d823cb10" />

<img width="1920" height="1080" alt="9-Web-Server-AMI and EFS" src="https://github.com/user-attachments/assets/dc1c59eb-f317-4bf0-873a-ba714db0121e" />

 # Step 4: Application Deployment
 
  CodeDeployment: Steps to deploy the application code to the EC2 instances.
  
 <img width="1920" height="1080" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/69909c1e-de4d-4ce2-83a6-d38d18a766d4" />
 
 <img width="1920" height="1080" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/69772fce-d5d0-455c-8db0-30fadfc59bdd" />
 
 <img width="1920" height="1080" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/aa9fcef2-ef32-44a5-a683-ad5ba49d8048" />
 
# Step 5: Create AMI (Machine Image)

► Select the instance → Click Actions → Image and templates → Create Image.

► Enter an image name (e.g., AMI - Image for web-server-Project-1).

► Add an optional description for better identification.

► Choose whether to enable Reboot instance.

► Verify storage (EBS volumes) settings.

► Click Create Image to start the AMI creation process.

<img width="1920" height="1080" alt="10-AMI - Image for web-server-Project-1" src="https://github.com/user-attachments/assets/aa1e9cdb-d238-48ba-8b2f-b7b10f31ac63" />

<img width="1920" height="1080" alt="11-AMI - Image for web-server-Project-1" src="https://github.com/user-attachments/assets/66d98da5-a9b7-467b-8ac2-441ffd800054" />

<img width="1920" height="1080" alt="12-AMI-Image for WEB-Server-Project-1" src="https://github.com/user-attachments/assets/89c0706f-23a5-45f5-9dbe-0f73d9e90849" />






 










