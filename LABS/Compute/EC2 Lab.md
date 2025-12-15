# **Overview**

This lab delivered essential practical experience with Amazon EC2 
(Elastic Compute Cloud), AWS's core scalable computing service. 
I focused on the full operational cycle of EC2 instances: launching, 
configuration, securing, monitoring, and scaling, which solidified my 
understanding of cloud infrastructure behavior.
This lab involved deploying a web server on EC2 with proper security and scalability.

___

__**To establish the foundation, I launched an EC2 instance based on the Amazon Linux 
2023 AMI (a t3.micro named "Web Server"). This instance was configured with termination 
protection and fully automated using a User Data script to install Apache and 
successfully deploy a basic web page upon startup.**__

<img width="1258" height="402" alt="image" src="https://github.com/user-attachments/assets/7278eb7a-3fe4-4016-8e8f-2d9da5933df8" />
<img width="772" height="273" alt="image" src="https://github.com/user-attachments/assets/83ed2333-91aa-4f03-80a4-71460424105e" />
<img width="765" height="262" alt="image" src="https://github.com/user-attachments/assets/473c9309-0069-4df8-b15e-d9f38086857e" />
<img width="769" height="298" alt="image" src="https://github.com/user-attachments/assets/b60e2f30-b9b6-4eea-a6a2-c457c1c6d889" />
<img width="775" height="303" alt="image" src="https://github.com/user-attachments/assets/fdaa84fe-e3ca-449b-b427-4dad4c3ba9db" />

___

__**Once the instance was running, I focused on monitoring and diagnostic procedures.**__

  - I checked System and Instance Reachability using Status Checks to confirm the health of the underlying host and the operating system/application layer.

  - I reviewed Amazon CloudWatch metrics to gain performance insights into CPU utilization, network traffic, and disk I/O.

  - The instance screenshot was to simulate console access for visual troubleshooting.

<img width="764" height="240" alt="image" src="https://github.com/user-attachments/assets/06cc76a9-7403-4a49-b5fe-09f9b0c66771" />
<img width="770" height="217" alt="image" src="https://github.com/user-attachments/assets/b2776855-89f2-4113-80ce-45c867bae3ca" />
<img width="771" height="170" alt="image" src="https://github.com/user-attachments/assets/6ab68e0e-2a74-4d75-a35b-891c9b8e9036" />
<img width="640" height="481" alt="image" src="https://github.com/user-attachments/assets/da631f33-d2f8-448f-8b0b-7e928f7be2e3" />

___

__**Browser access to my instance failed because the associated security group was blocking 
HTTP traffic. After I modified the security group to permit inbound traffic on port 80, 
I was able to successfully access the web server, confirming the automation script's 
correct deployment of the webpage.**__

<img width="767" height="241" alt="image" src="https://github.com/user-attachments/assets/0f32b9ee-4528-4eef-beb2-0eaf0cb68e9a" />
<img width="754" height="547" alt="image" src="https://github.com/user-attachments/assets/aa60f3a7-c9c7-4232-aee6-08fdf4e8d2e6" />
<img width="750" height="99" alt="image" src="https://github.com/user-attachments/assets/7a55a5b3-4927-4dd5-aa5f-70b33471e3de" />
<img width="761" height="210" alt="image" src="https://github.com/user-attachments/assets/ac90d9c0-8ef5-4ffd-becc-545e85ef7bd0" />
<img width="768" height="182" alt="image" src="https://github.com/user-attachments/assets/fe535208-c3e2-4fb9-bdfe-f3e9c4eafeb0" />
<img width="338" height="52" alt="image" src="https://github.com/user-attachments/assets/fb1caa29-0359-420b-8792-acbd0efc6f60" />

___

__**I executed a dynamic scaling procedure on the instance. This step successfully illustrates
how EC2 resources can be modified on-demand to align with evolving application requirements. This involved:**__

  - Stopping the instance.

  - Resizing the type from a t3.micro to a t3.small, effectively doubling the available memory.

  - Increasing the root EBS volume size from 8 GiB to 10 GiB.

  - Restarting the instance.

<img width="764" height="98" alt="image" src="https://github.com/user-attachments/assets/0c8416d7-ccea-4e18-b944-53db90ca19b7" />
<img width="767" height="255" alt="image" src="https://github.com/user-attachments/assets/e37d7a19-a6d3-4bac-96b4-aac1d4e6ef4e" />
<img width="766" height="284" alt="image" src="https://github.com/user-attachments/assets/bfe5304b-5dd2-4a80-88d2-9a83c117f71e" />
<img width="773" height="280" alt="image" src="https://github.com/user-attachments/assets/13da9832-0c6b-4e77-bc2e-cc662379209d" />
<img width="767" height="293" alt="image" src="https://github.com/user-attachments/assets/9b1b1eab-e7e3-4432-863f-0c4702b0da7c" />
<img width="762" height="412" alt="image" src="https://github.com/user-attachments/assets/5b627a5d-1fad-42a7-94c2-e8556281234f" />
<img width="768" height="94" alt="image" src="https://github.com/user-attachments/assets/077205fb-0c4f-49c5-a80c-73c193784ec7" />
<img width="763" height="213" alt="image" src="https://github.com/user-attachments/assets/251b681f-35a9-4566-a1b4-63c6478b7ac2" />
<img width="762" height="182" alt="image" src="https://github.com/user-attachments/assets/2da6c4a8-8ed0-4ee5-90d7-8652b3abb745" />
<img width="431" height="257" alt="image" src="https://github.com/user-attachments/assets/1dc8f30d-cdd5-4a99-bef8-ec2043ce7801" />
<img width="766" height="115" alt="image" src="https://github.com/user-attachments/assets/1d4b9d0a-67a5-4917-858d-8fc472f48590" />
<img width="767" height="100" alt="image" src="https://github.com/user-attachments/assets/f8635a2c-7496-482e-8f54-b75885b031f9" />
<img width="673" height="82" alt="image" src="https://github.com/user-attachments/assets/b2279a6b-82f1-46aa-868d-b3efa1f94e99" />

___

__**Termination protection testing was performed by attempting to terminate the instance. 
The initial attempt was blocked, confirming the safeguard's functionality. 
The protection was then disabled, allowing for successful instance termination. 
This process highlighted the value of such safeguards in a production environment.**__

<img width="763" height="103" alt="image" src="https://github.com/user-attachments/assets/1aea4471-12be-477b-8d1b-35a723acb0b7" />
<img width="767" height="251" alt="image" src="https://github.com/user-attachments/assets/c2bd6887-e227-4a50-b703-614317811693" />
<img width="766" height="105" alt="image" src="https://github.com/user-attachments/assets/84c3b751-caec-45fb-b9a7-c90d7a2aeed8" />
<img width="763" height="265" alt="image" src="https://github.com/user-attachments/assets/429bdce1-2a08-4f4f-b3bf-03c205de7816" />
<img width="772" height="235" alt="image" src="https://github.com/user-attachments/assets/f1afe330-e1bf-4a1f-8f87-c8a110b29095" />
<img width="764" height="114" alt="image" src="https://github.com/user-attachments/assets/84627ed0-43cb-4203-94f2-4ca442602643" />
<img width="767" height="249" alt="image" src="https://github.com/user-attachments/assets/0a6533b7-7e35-4354-ab37-97ab6da19aa2" />
<img width="765" height="111" alt="image" src="https://github.com/user-attachments/assets/2a614c8a-9f9f-4778-801f-28a8386f0c5f" />

___

# __**What I Learned**__

I successfully completed the EC2 lab, gaining direct, end-to-end experience in essential cloud operations. This involved:

  - Automating a secure web server deployment.

  - Configuring security groups for effective network traffic management.

  - Setting up CloudWatch for instance health and performance monitoring.

  - Practicing dynamic resource scaling for compute and storage.

  - Implementing termination protection and other safeguards.

This project significantly strengthened my foundational skills in AWS cloud infrastructure management and the practical construction of scalable applications.







