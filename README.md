# Build-a-Virtual-Private-Cloud
In this project, I will demonstrate how to build and configure a Virtual Private Cloud (VPC) from scratch in AWS, including setting up networking components like subnets and internet connectivity. I’m doing this project to learn the fundamentals of AWS networking, how resources communicate securely within a VPC, and how to design a basic cloud network architecture.
<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** sabastinemc@gmail.com  
**Email:** sabastinemc@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/triumphant_silver_zany_torea/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will demonstrate how to build and configure a Virtual Private Cloud (VPC) from scratch in AWS, including setting up networking components like subnets and internet connectivity. I’m doing this project to learn the fundamentals of AWS networking, how resources communicate securely within a VPC, and how to design a basic cloud network architecture.

### What is Amazon VPC?

Amazon VPC is a Virtual Private Cloud that lets you create a logically isolated network within the AWS cloud, where you can launch and manage resources like EC2 instances, databases, and load balancers.
It is useful because it gives you full control over your network environment, including IP addressing, subnets, routing, and security, allowing you to securely connect resources and control how they communicate with each other and the internet.

In today's project, I used Amazon VPC to create a private, isolated network in AWS, set up a public subnet, and attach an internet gateway, allowing my resources to communicate securely within the VPC and access the internet when needed.

### Personal reflection

This project took me approximately 20 minutes to complete, including creating the VPC, setting up subnets, and attaching an internet gateway.

One thing I didn't expect in this project was how much detail and control AWS gives you over networking, like defining CIDR blocks, subnets, and internet gateways, even for a simple setup, which really showed me the power and flexibility of VPCs.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will access the Amazon VPC console and create a new VPC because a VPC provides a private, isolated network where I can securely launch and manage AWS resources and control how they communicate.

### How VPCs work

VPCs are virtual networks in AWS that let you launch and manage resources in a logically isolated environment, giving you control over IP addressing, subnets, routing, and security within the cloud.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because AWS automatically creates a default VPC to allow users to quickly launch resources and connect services without needing to manually set up networking from the start, making it easier for beginners to use services like EC2 right away.

![Image](http://learn.nextwork.org/triumphant_silver_zany_torea/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is a range of IP addresses that determines how many resources can be created within the VPC and how they are addressed and communicate with each other.

---

## Subnets

### What I did in this step

In this step, I will create a subnet within my VPC because subnets allow me to divide the VPC into smaller, organized network segments where I can place and manage AWS resources more effectively.

### Creating and configuring subnets

Subnets are smaller network segments within a VPC that divide the IP address range into organized sections where resources can be placed and managed. There are already subnets existing in my account, one for every Availability Zone in the Region, because AWS automatically creates them as part of the default VPC setup.

### Public vs private subnets

The difference between public and private subnets are whether or not they have direct access to the internet. Public subnets allow resources to communicate with the internet, while private subnets do not.
For a subnet to be considered public, it has to be connected to an internet gateway and have a route that allows traffic to flow to and from the internet.

![Image](http://learn.nextwork.org/triumphant_silver_zany_torea/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 address. This setting makes sure any EC2 instance launched in that subnet will instantly get a public IP address, so that I won't have to create one manually

---

## Internet gateways

### What I did in this step

In this step, I will create and attach an Internet Gateway to my VPC because it enables resources in the VPC (such as those in a public subnet) to communicate with the internet, allowing inbound and outbound internet traffic.

### Setting up internet gateways

Internet gateways are tools that connect your city (VPC) and the outside world (internet). 

Attaching an internet gateway to a VPC means the VPC can send and receive traffic from the internet, allowing resources in public subnets to be accessible online.
If I missed this step, resources in the VPC would not be able to communicate with the internet, meaning instances in the subnet would remain private and unreachable from external networks.

![Image](http://learn.nextwork.org/triumphant_silver_zany_torea/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will use AWS CloudShell and the AWS CLI to create a VPC, subnet, and internet gateway because it allows me to automate infrastructure setup, work faster than using the console, and gain hands-on experience with command-line tools used in real-world cloud environments.

### Exploring CloudShell and CLI

VPC resources could also be created with CloudShell, which is a browser-based, preconfigured terminal in the AWS Console that lets you run AWS CLI commands without installing anything locally.
CLI is the Command Line Interface, a tool that allows you to interact with AWS services by typing commands instead of using the graphical console, making it faster and more efficient for automation and scripting.

### Debugging my setup

To set up a VPC or a subnet, you can use the AWS CLI commands such as aws ec2 create-vpc or aws ec2 create-subnet. I ran into an error because some required parameters were missing or incorrectly specified, such as the CIDR block or the VPC ID. Make sure to avoid errors by including all mandatory arguments, using the correct syntax, and verifying that the values (like CIDR ranges and Availability Zones) are valid and do not overlap with existing resources.

![Image](http://learn.nextwork.org/triumphant_silver_zany_torea/uploads/aws-networks-vpc_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands in CloudShell is faster setup, automation, and the ability to repeat tasks easily. An advantage of using the Console is a visual interface that makes it easier to understand and verify resources, especially for beginners. Overall, I preferred using the Console for learning and visualization, but CloudShell is great for speed and automation once you know what you’re doing.

---

---

