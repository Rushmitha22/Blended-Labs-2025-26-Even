# Lab 3 - Introduction to Amazon Elastic Compute Cloud (EC2) 

## Author

* **Name**: __RUSHMITHA R__
* **Register Number**: __212224040281__
* **Date of Submission**: __17/08/2026__

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)


1. The EC2 Dashboard was accessed through the AWS Management Console to explore the Amazon EBS volume types.

2. A new EBS volume was created by selecting the volume type, size, and the same Availability Zone as the EC2 instance.

3. The created EBS volume was attached to the running EC2 instance as an additional block device.

4. The attached volume was formatted using the ext4 file system and mounted to a directory in the EC2 instance.

5. .Sample data was stored in the mounted volume, and after rebooting the instance, data persistence was verified successfully

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1917" height="1022" alt="Screenshot 2026-08-17 135245" src="https://github.com/user-attachments/assets/7d1e6e3d-9f2f-4779-b4c6-e89550063027" />

<img width="1911" height="1023" alt="Screenshot 2026-08-17 135221" src="https://github.com/user-attachments/assets/2ab56a98-925f-422b-bee1-77f3a0dcc2e9" />


---

### Screenshot 2: SSH Connection to Instance

<img width="1118" height="752" alt="image" src="https://github.com/user-attachments/assets/08a31ca6-da51-4ecd-a27d-a53849f5b015" />


---

### Screenshot 3: Instance Monitoring / Status

<img width="1917" height="957" alt="Screenshot 2026-08-17 140415" src="https://github.com/user-attachments/assets/394ccbf7-1da9-47ba-85a6-d8da6c787657" />

<img width="1916" height="1022" alt="Screenshot 2026-08-17 135729" src="https://github.com/user-attachments/assets/7894f4dc-c9e4-4dd8-b48a-e1e4e7f40476" />


---

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
