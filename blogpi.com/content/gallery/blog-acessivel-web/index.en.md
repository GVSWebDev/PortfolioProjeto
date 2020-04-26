---
title: "Making the Blog Accessible on the Web"
date: 2020-04-26T16:23:19-03:00
 

categories: []
tags: ['Atualizacoes']
author: "Team Maya"
 

---

Initially, we registered for access to the AWS website. We started a virtual machine using EC2 (Image 1), from AWS, running the Amazon Linux 2 distribution (Images 2 and 3). We performed the updates of the VM's operating system (with the command: sudo yum update) (Image 4) and installed the Apache service to create the blog Host on the Web (Image 5), for this it was necessary to compile the blog.

In order to make the blog structure easier to access, we installed git so that we can clone, transfer files and version the blog (Image 6).
With the project properly cloned, we copy the compiled files to the Apache folder (Image 7).

Once this is done, we configure the machine's firewall, with the firewall system already included on the AWS website (Image 8), removing the need to download any other firewall application or configure directly inside the VM. The AWS Firewall system allows you to easily create data entry and exit rules (Image 9), so that the Apache service with our blog is accessible from an external network, we created a rule that allows connections on port 80 of the machine ( port used by the Apache service) (Image 10).

After that our service was working normally, and when we type the VM's public IP into the browser (Image 11), the browser itself automatically redirects to the VM's port 80 by accessing Apache and displaying our compiled blog (Image 12).