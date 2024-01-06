---
bioschemas:
  "@context": "https://schema.org"
  "@type": "LearningResource"
  "@id": "https://cloud-span.github.io/cloud-admin-guide-0-overview/"
  "http://purl.org/dc/terms/conformsTo":
  - "@type": CreativeWork
    "@id": "https://bioschemas.org/profiles/TrainingMaterial/1.0-RELEASE"
  about:
  - "@id": "http://edamontology.org/topic_3372"
  - "@id": "http://edamontology.org/topic_0769"
  abstract: "This course teaches how to automatically manage multiple Amazon Web Services (AWS) instances — each instance being a Linux virtual machine. Using Bash Shell scripts, we show how to create, stop, start and delete one or multiple instances with a single invocation of a script. The target audience of the course is anyone in charge of, or interested in, deploying and managing cloud resources. While the course is focused on AWS, and particularly Elastic Compute Cloud (EC2) instances, the scripts can be adapted for use with other cloud providers and other types of cloud services."
  author: ["Jorge Buenabad-Chavez", "Emma Rand", "Sarah Forrester", "Annabel Cansdale", "Evelyn Greeves"]
  contributor: ["James Chong", "Emma Barnes", "University of York", "Software Sustainability Institute"]
  educationalLevel: "Advanced"
  identifier: 10.5281/zenodo.7589272
  name: "Cloud-SPAN: Automated Management of AWS Instances"
  url: "https://cloud-span.github.io/cloud-admin-guide-0-overview/"
  inLanguage: "en"
  keywords: "cloud computing, AWS,  HPC, shell, command line tools, linux, elastic cloud compute"
  license: CC-BY 4.0
  timeRequired: "PT8H"
  mentions: ["Git for Windows", "Cloud-SPAN Genomics course", "Data Carpentries Genomics workshop"]
---
<h3 align="center">a Cloud-SPAN course</h3>

[Cloud-SPAN](https://cloud-span.york.ac.uk) is a project run by the Biology Department at the University of York with the aim to training researchers in the experimental design and analysis of 'omics data using cloud-based High Performance Computing (HPC) resources.

This course teaches how to automatically manage multiple Amazon Web Services (AWS) instances --- each instance being a Linux virtual machine. Using Bash Shell scripts, we show how to create, configure, stop, start and delete one or multiple instances with a single invocation of a script. 

We use the scripts to manage multiple instances for training. When running a workshop, instances are created with 'omics data and software required for the workshop. Each student is granted exclusive access to one instance through the use of an encrypted login key. 

To create, configure, .. or delete instances, the scripts require only the names of the instances. The login keys, IP addresses, and domain names used by the instances are created or deleted automatically. Creating over 30 instances takes 10-15 minutes.

The target audience of the course is anyone interested in deploying and managing cloud resources for training. While the course is focused on AWS, and particularly Elastic Compute Cloud (EC2) instances, the scripts can be adapted for use with other cloud providers and other types of cloud services.

The course is designed for 4-6 hours of self-study, depending on the number of related topics you decide to explore further.

> ## Getting Started
>
> The course assumes that learners have **no** prior experience with the AWS concepts and tools covered in the course.
>
> However, learners are expected to have experience with both the Linux/Unix **terminal** and **Bash shell programming** --- the terminal is also known as the **shell** and the **command line interface** or CLI. **Windows users** need to install and configure the Git Bash terminal and **Mac users** need to install or update the Bash shell as instructed in the [Setup](./setup) section; see also the [Workshops Organisation](#workshops-organisation) below.
>
> Learners are also expected to use a laptop or destop computer. Tablets and mobile phones are not suitable for taking the course, as you will be using the keyboard to type commands to the terminal or to edit text files.
>
{: .prereq}

# Background
"*Cloud computing is the on-demand availability \[through the Internet\] of computer system resources \[such as\] data storage and computing power ... \[that\] relies on a "pay-as-you-go" model ..."\[[Wikipedia](https://en.wikipedia.org/wiki/Cloud_computing)\].* That means that we can **rent** as many computing resources as we need, whenever we need them, and pay only for the time we use them. 

The main advantage of Cloud computing is that we don't have to commit too much time and money in managing the IT resources needed to try out a new idea or experiment. Or as is the case of the Cloud-SPAN and similar projects, running hands-on training workshops by providing a properly configured instance (virtual machine) to each participant without having to handle nor invest in hardware resources nor physical space. Instead, an instance in the cloud is first configured with all the data and software tools required by a workshop. This instance is then configured as a template, or Amazon Machine Image (AMI) in AWS terminology. Finally, a number of instances is created from the AMI and configured individually as to domain name, IP address and access login key. Once the course is over, the instances are deleted to stop incurring costs. The AMI is typically preserved to serve as the starting point either (1) to create new instances for a new run of the workshop, or (2) to create a new AMI with updated data or software or both, through creating an instance, updating the data or software, and creating an AMI out of the instance.

Despite such convenience, managing multiple instances through a Graphical User Interface (GUI), such as the AWS Console, is really cumbersome and error-prone. Hence we developed the scripts, and through their use we have noted a few best practices to manage multiple instances that are covered in the course.

# Course Overview

| Lesson                     | Overview |
| -------------------------- | ---------|
| 1. [Setting Up Your Cloud and Terminal Environments](https://cloud-span.github.io/cloud-admin-guide-1-setting-work-environments/) | Learn how to create and configure your AWS account for daily work, and how to install and configure the scripts in your Terminal environment to use your AWS account.|
| 2. [Managing AWS Instances](https://cloud-span.github.io/cloud-admin-guide-2-managing-aws-instances/) | Learn how to configure your AWS account to provide AWS instances with access based on domain names and login keys, how to run the scripts to deploy and manage AWS instances for a workshop, how to create and manage AMIs, and the organisation and workings of the scripts. |

# Workshops Organisation
Online and in-person workshops of this course are delivered in 2 - 2.5 hours and are focused on the **configuration** and **use** of the scripts, covering **only** the episodes indicated below:

Lesson 1: Setting Up Your Cloud and Terminal Environments:\
1.1. Create Your AWS Account\
1.2. Configure Your AWS Account\
1.3. Configure Your Terminal Environment  --- **workshop**\
1.4. Configure Your AWS CloudShell Environment

Lesson 2: Managing AWS Instances:\
2.1. Configure Instances Internet Access\
2.2. Instances Management Tasks Using the Scripts --- **workshop**\
2.3. AMIs Management     --- **workshop**\
2.4. The Scripts Design  --- **workshop**

### Attending a workshop with no AWS account --- using a Cloud-SPAN AWS account
You can attend a workshop without having to create and configure an AWS account (Episodes 1.1 and 1.2). However, as an AWS account is needed to create and manage AWS instances with the scripts, as a workshop attendee, an AWS Linux instance will be made available to you (at no cost by the Cloud-SPAN team) wherein you will **configure** the terminal environment (Episode 1.3) and **run** the scripts (to create and manage AWS instances) **using** a **Cloud-SPAN AWS account** (which is already configured as to those aspects covered in Episode 2.1). To login to your Linux instance you will use the (secure shell) `ssh` program, and hence, prior to the workshop you need have installed `ssh` on your (Linux or Mac) computer -- **Windows users** can install Git Bash as that will also install `ssh` on their computer, see the [Setup](./setup) section. You will receive instructions to login to your Linux instance at the worshop.

### Attending a workshop using your AWS account
You can attend a workshop and use **your AWS account** (or the AWS account of your institution) to configure and run the scripts. You need to **complete** the following episodes **before** the workshop (contact the [Cloud-SPAN team](https://cloud-span.york.ac.uk/contact) if you need assistance):

1.1. Create Your AWS Account\
1.2. Configure Your AWS Account\
2.1. Configure Instances Internet Access

At the workshop, you will configure the scripts to use your AWS account and run the scripts on your computer, which you can do using either a Git Bash terminal, a Linux terminal, a Mac terminal or the AWS CloudShell terminal. **Windows users** need to install Git Bash and **Mac users** need to install or update the Bash shell on their computer prior to the workshop, see details in the [Setup](./setup) section, the introduction to Lesson 1, [Setting Up Your Cloud and Terminal Environments](https://cloud-span.github.io/cloud-admin-guide-1-setting-work-environments/), and in these episodes:

1.3. Configure Your Terminal Environment --- Git Bash, Linux and Mac terminals\
1.4. Configure Your AWS CloudShell Environment
