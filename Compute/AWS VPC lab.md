# __**Building a VPC and launching a Web Server**__

__**Overview**__

This lab details the architecture and implementation of a highly customized 
AWS VPC, demonstrating the configuration of dual subnets (public/private), 
network security via security groups, controlled traffic flow with route 
tables, and the final deployment of a live EC2 web server.
___

__**I created a Virtual Private Cloud (VPC) usng the following configurations:**__

  - VPC CIDR: 10.0.0.0/16
  - Subnets: 2 Public, 2 Private across 2 AZs
  - Internet Gateway: Enabled for public access
  - NAT Gateway: Enabled for private subnet internet access

<img width="760" height="285" alt="image" src="https://github.com/user-attachments/assets/fd71141f-3fd9-460c-8e72-4ad47f0f7505" />

___

__**The Subnets Configured and their Configuration**__

<img width="584" height="230" alt="image" src="https://github.com/user-attachments/assets/ec2d3256-2240-4768-a4df-3fdf898c601c" />
<img width="766" height="310" alt="image" src="https://github.com/user-attachments/assets/a3bf6617-ae71-4fb9-a461-24ef78a63b0e" />

___

__**The Route Tables were Configurated as both Public and Private Route Tables 
with both being 0.0.0.0/0 routes. Public being an Internet Gateway and Private 
being a NAT Gateway.**__

<img width="753" height="356" alt="image" src="https://github.com/user-attachments/assets/66bb6628-1863-429f-b49d-8df30f596f58" />
<img width="766" height="348" alt="image" src="https://github.com/user-attachments/assets/946d1c6f-8ebf-434f-a990-32611e563567" />

___

__**Security Group information was filled with the following information:**__

  - Name: Web Security Group
  - Inbound Rule: HTTP (Port 80) from anywhere (0.0.0.0/0)

<img width="768" height="285" alt="image" src="https://github.com/user-attachments/assets/2c0e6308-a51c-4cea-b4af-4b5e7529b90f" />

___

__**The following information made EC2 Instance & Web Server applicable to launch an instance:**__

  - Instance Type: t3.micro
  - AMI: Amazon Linux 2
  - User Data Script: Installs Apache web server and PHP, downloads lab files

        #!/bin/bash
        yum install -y httpd mysql php
        wget https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-100-RESTRT-1/267-lab-NF-build-vpc-web-server/s3/lab-app.zip
        unzip lab-app.zip -d /var/www/html/
        chkconfig httpd on
        service httpd start

<img width="759" height="282" alt="image" src="https://github.com/user-attachments/assets/332ccc5d-9b58-4313-8c10-626900963b3a" />
<img width="765" height="290" alt="image" src="https://github.com/user-attachments/assets/d2cb47c6-3de8-4ceb-b918-7980f9b25888" />
<img width="760" height="283" alt="image" src="https://github.com/user-attachments/assets/8474246b-eb2a-42ea-9fd0-231c0d1138cd" />
<img width="758" height="291" alt="image" src="https://github.com/user-attachments/assets/7b095288-119d-492f-be15-14e59fe7a0b3" />
<img width="759" height="298" alt="image" src="https://github.com/user-attachments/assets/156caf7f-e6b3-4b63-a512-8b783ddac3cc" />

___

__**I launched the instance. When the status checks reached 2/2, I copied the Public IPv4 DNS. I then opened it in my browser and saw the success page.**__

<img width="763" height="124" alt="image" src="https://github.com/user-attachments/assets/b3505e3c-7496-411d-9d27-1a3dd49a713b" />
<img width="764" height="102" alt="image" src="https://github.com/user-attachments/assets/8f47fe17-70e9-4ed6-9d0a-5400bcf7b559" />
<img width="765" height="303" alt="image" src="https://github.com/user-attachments/assets/b1d4b146-6ab6-4ad0-907f-fa1abcc2f5c0" />

___

# __**What I learned**__
 I learnt to successfully design, built, and secure a highly available, multi-tiered web application environment within an Amazon Web Services (AWS) Virtual Private Cloud (VPC).

