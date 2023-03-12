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

To create, configure, .. or delete instances, the scripts require only the names of the instances. Login keys, IP addresses, and domain names used by the instances are created or deleted automatically. Creating over 30 instances takes 10-15 minutes.

The target audience of the course is anyone interested in deploying and managing cloud resources for training. While the course is focused on AWS, and particularly Elastic Compute Cloud (EC2) instances, the scripts can be adapted for use with other cloud providers and other types of cloud services.

The course is designed for 4-6 hours of self-study, depending on the number of related topics you decide to explore further.

> ## Getting Started
>
> The course assumes that learners have **no** prior experience with the AWS concepts and tools covered in the course.
>
> However, learners are expected to have experience with both the Linux terminal /command line interface (CLI) and Bash shell programming. Instructions are also provided to install and configure the Git Bash terminal on Windows computers and Mac terminals running the Bash shell or the Zsh shell.
>
> Learners are also expected to use a laptop or destop computer. Tablets and mobile phones are not suitable for taking the course, as you will be using the keyboard to type commands to the terminal or to edit text files.
>
{: .prereq}

## Background
"*Cloud computing is the on-demand availability \[through the Internet\] of computer system resources \[such as\] data storage and computing power ... \[that\] relies on a "pay-as-you-go" model ..."\[[Wikipedia](https://en.wikipedia.org/wiki/Cloud_computing)\].* That means that we can **rent** as many computing resources as we need, whenever we need them, and pay only for the time we use them. 

The main advantage of Cloud computing is that we don't have to commit too much time and money in managing the IT resources needed to try out a new idea or experiment. Or as is the case of the Cloud-SPAN and similar projects, running hands-on training workshops by providing a properly configured instance (virtual machine) to each participant without having to handle nor invest in hardware resources nor physical space. Instead, an instance in the cloud is first configured with all the data and software tools required by a workshop. This instance is then configured as a template, or Amazon Machine Image (AMI) in AWS terminology. Finally, a number of instances is created from the AMI and configured individually as to domain name, IP address and access login key. Once the course is over, the instances are deleted to stop incurring costs. The AMI is typically preserved to serve as the starting point either (1) to create new instances for a new run of the workshop, or (2) to create a new AMI with updated data or software or both, through creating an instance, updating the data or software, and creating an AMI out of the instance.

Despite such convenience, managing multiple instances through a Graphical User Interface (GUI), such as the AWS Console, is really cumbersome and error-prone. Hence we developed the scripts, and through their use we have noted a few best practices to manage multiple instances that are covered in the course.

# Course Overview

| Lesson                     | Overview |
| -------------------------- | ---------|
| [Setting Up Your Cloud and Terminal Environments](https://cloud-span.github.io/cloud-admin-guide-1-setting-work-environments/) | Learn how to set up your AWS account and your Linux environment to run the scripts.|
| [Managing AWS Instances](https://cloud-span.github.io/cloud-admin-guide-2-managing-aws-instances/) | Learn how to configure your AWS account and the scripts to deploy and manage AWS instances for a workshop, how to create new AMIs, and the workings of the scripts. |


