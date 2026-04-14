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

