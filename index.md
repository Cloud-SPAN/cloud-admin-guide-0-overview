---
---
<h3 align="center">a Cloud-SPAN course</h3>

[Cloud-SPAN](https://cloud-span.york.ac.uk) is a project run by the Biology Department at the University of York with the aim to training researchers in the experimental design and analysis of 'omics data using cloud-based High Performance Computing (HPC) resources.

This course teaches how to manage Amazon Web Services (AWS) instances --- each instance being a Linux virtual machine. Using Bash Shell scripts, it is shown how to configure, create, stop, start, and delete, one or multiple instances with a single invokation of a script. 

We manage multiple instances with the scripts within the Cloud-SPAN project for hands-on training purposes. When running a workshop, a number of instances are configured with relevant 'omics data and software analysis tools. Each student is granted exclusive access to such an instance through the use of encrypted login keys. 

The login key, the domain name, and the IP address of each instance are created on demand on
creating the corresponding instance, and deleted when the corresponding instance is deleted. The scripts receive as input only the names of the instances to be created, deleted, etc. The scripts keep track in local files of the resources' AWS resourceIDs, which are needed to interact with AWS to, for example, delete and instance and associated resources (domain name, etc.). Creating over 30 instances takes 10-15 minutes.

The target audience of the course is anyone in charge of, or interested in, deploying and managing cloud resources. While the course is focused on AWS, and particularly Elactic Compute Cloud (EC2) instances, the scripts can be adapted for use with other cloud providers and other types of cloud services.

The course is designed for 6-8 hours of self-study.

> ## Getting Started
>
> The course assumes that learners have **no** prior experience with the AWS concepts and tools covered in the course.
>
> However, learners are expected to have good experience with (1) the Linux command line interface (CLI) and (2) Bash shell programming.
>
> Learners are also expected to use a Linux laptop or destop machine. Tablets and mobile phones are not suitable for taking the course, as you will be using the keyboard to type to the CLI or editing scripts most of the time.
>
{: .prereq}

## Background
"*Cloud computing is the on-demand availability \[through the Internet\] of computer system resources \[such as\] data storage and computing power ... \[that\] relies on a "pay-as-you-go" model ..."\[[Wikipedia](https://en.wikipedia.org/wiki/Cloud_computing)\].* That means we can **rent** as many computing resources as we need, whenever we need them, and pay only for the time we use them. 

The main advantage of Cloud computing is that we don't have to commit too much time and money in managing the IT resources needed to try out a new idea or experiment. Or, as is the case of the Cloud-SPAN and similar projects, running hands-on training workshops by providing a properly configured instance (virtual machine) to each participant without having to handle nor invest in hardware resources nor physical space. Instead, an instance in the cloud is first configured with all the data and software tools required by a workshop. This instance is then configured as a template, or Amazon Machine Image (AMI) in AWS terminology. Finally, a number of instances is created from the AMI and configured individually as to domain name, IP address and accessing login key. Once the course is over, the replicas are deleted to stop incurring costs. The AMI is typically preserved to serve as the starting point either to create new virtual machines for a new run of the previous workshop or to create a virtual machine to configure with other data and software and as an AMI for a new workshop.

Despite such convenience, managing multiple instances through a Graphical User Interface (GUI), such as the Amazon Web Services (AWS) Console, is really cumbersome and error-prone. Hence we developed the scripts, and through their use we have noted a few best practices to manage multiple instances that are covered in the course.

We are aware of other approaches to manage cloud resources, particularly Infrastructure as Code (IaC) with AWS CloudFormation and Terraform .... Ansible ...

The two main reasons for our script-based approach are (1) the steep learning curve of Terraform and Ansible, ...; and (2) the infrastructure we are managing, multiple instances, does not change much over time, and thus using Terraform and Ansible are overkill to a good extent.

# Course Overview

| Lesson                     | Overview |
| -------------------------- | ---------|
| [Setting the work environment](https://cloud-span.github.io/cloud-admin-guide-1-setting-work-environments/) | Learn how to set up your working environment, your AWS account and your shell terminal configuration, to be able to run the scripts. (UNDER CONSTRUCTION)|
| [Managing AWS instances](https://cloud-span.github.io/cloud-admin-guide-2-managing-aws-instances/) | Learn some best practices to deploy and manage AWS instances for a course, for testing software configurations, for creating new AMIs. (UNDER CONSTRUCTION) |
| [Managing AMIs, Scripts, etc](https://cloud-span.github.io/cloud-admin-guide-3-managing-amis-scripts-etc/) |  Learn the blurry bits of the scripts, how to control changes to the scripts with GitHub, the Cloud-SPAN AMIs, when and how to create and control AMI versions, updating an AMI Linux and software tools, and more. (UNDER CONSTRUCTION) |

