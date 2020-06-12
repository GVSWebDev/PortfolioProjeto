---
title: "Making the Blog Accessible on the Web"
date: 2020-04-26T16:23:19-03:00
 

categories: []
tags: ['Atualizacoes']
author: "Team Maya"
 

---
Initially we registered for access to the AWS website, We started a virtual machine using EC2,

<div style = "text-align: center"> <img src = "https://cdn.discordapp.com/attachments/555568413674700800/704047870277582978/unknown.png"> </div>

 AWS, running the Amazon Linux 2 distribution.
 
 <div style = "text-align: center"> <img src = "https://cdn.discordapp.com/attachments/555568413674700800/704048067455746179/unknown.png"> </div>
 
***

 <div style = "text-align: center"> <img src = "https://cdn.discordapp.com/attachments/555568413674700800/704049341098098893/unknown.png"> </div>

We perform the updates of the VM's operating system (with the command: sudo yum update)

 <div style = "text-align: center"> <img style = "width: 60%" src = "https://cdn.discordapp.com/attachments/555568413674700800/704049568144293908/unknown.png"> </div>

and we installed the Apache service to create the blog Host on the web,

 <div style = "text-align: center"> <img style = "width: 60%" src = "https://cdn.discordapp.com/attachments/555568413674700800/704050113172996256/unknown.png"> </div>

 for that it was necessary to compile the blog.

In order to make the blog structure easier to access, we installed git so that we can clone, transfer files and version the blog.

 <div style = "text-align: center"> <img style = "width: 60%" src = "https://cdn.discordapp.com/attachments/555568413674700800/704050443441012896/unknown.png"> </div>

With the project properly cloned, we copy the compiled files to the Apache folder.

<div style = "text-align: center"> <img style = "width: 60%" src = https://cdn.discordapp.com/attachments/555568413674700800/704050961005543484/unknown.png> </div>

That done, we set up the machine’s firewall, with the firewall system already included on the AWS website,

<div style = "text-align: center"> <img src = https://cdn.discordapp.com/attachments/555568413674700800/704051343731720253/unknown.png> </div>

removing the need to download any other firewall application or configure directly within the VM. The AWS Firewall system allows you to easily create data entry and exit rules,

<div style = "text-align: center"> <img src = https://media.discordapp.net/attachments/555568413674700800/704051766005596190/unknown.png?width=1026&height=94> </div>

 so that the Apache service with our blog is accessible from an external network, we created a rule that allows connections on port 80 of the machine (port used by the Apache service).

 <div style = "text-align: center"> <img src = https://media.discordapp.net/attachments/555568413674700800/704052989068836884/unknown.png> </div>

After that our service was working normally, and when we type the VM's public IP into the browser (Image 11), the browser itself automatically redirects to the VM's port 80 by accessing Apache and displaying our compiled blog.

<div style = "text-align: center"> <img src =https://media.discordapp.net/attachments/555568413674700800/704053227880054934/unknown.png?width=1026&height=347 > </div>