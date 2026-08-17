<img width="1917" height="1030" alt="cc lab2 ss3" src="https://github.com/user-attachments/assets/8a23990f-58a4-48e4-9978-eefec640b2c5" /><img width="1912" height="986" alt="cc lab2 ss1" src="https://github.com/user-attachments/assets/6a25c7d9-e66b-4961-8cc6-c9591f482d14" /><img width="1917" height="1030" alt="cc lab2 ss3" src="https://github.com/user-attachments/assets/99f2a341-9a0c-4b10-a69e-d699d498e565" /># EXPERIMENT 2 : BUILD YOUR VPC AND LAUNCH A WEB SERVER (AWS)

## Author

* **Name**: __RUSHMITHA  R__
* **Register Number**: __212224040281__
* **Date of Submission**: __17/08/2026__

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

First, I created a VPC in Amazon Web Services. I gave it a CIDR block of 10.0.0.0/16. This VPC acts as my private network where all my resources will be created.

Next, I created a public subnet inside the VPC with CIDR 10.0.1.0/24. I enabled auto-assign public IP so that any instance launched in this subnet will automatically get a public IP address.

After that, I created an Internet Gateway and attached it to my VPC. This allows my VPC to communicate with the internet.

Then, I created a route table and added a default route (0.0.0.0/0) pointing to the Internet Gateway. I associated this route table with my public subnet. This step ensures that traffic from my subnet can reach the internet.

Next, I created a security group which acts as a virtual firewall. I allowed inbound traffic for SSH on port 22 and HTTP on port 80.

After completing the network setup, I launched an EC2 instance using Amazon Linux 2 AMI with instance type t2.micro. I selected my VPC, public subnet, created security group, and key pair.

Finally, I connected to the EC2 instance using SSH and installed the Apache web server. I started the service and created a simple HTML page. Then I copied the public IP address of the instance and opened it in a web browser. The webpage was displayed successfully.

So, this is how I created a VPC, launched an EC2 instance, and hosted a simple web server in AWS.




## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1912" height="986" alt="cc lab2 ss1" src="https://github.com/user-attachments/assets/88e7f567-6087-4bb6-a19b-3077b2c118ca" />


### Screenshot 2: EC2 Instance Running

<img width="1917" height="982" alt="cc lab2 ss2" src="https://github.com/user-attachments/assets/b3e2d945-6172-4802-8e9d-65aea98da27a" />

![Uploading cc lab2 ss3.png…]()


### Screenshot 3: Web Server Output in Browser



<img width="1496" height="862" alt="cc la2 ss4" src="https://github.com/user-attachments/assets/c1173d61-362c-4269-b46d-f0b5c37bd2f2" />




## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
