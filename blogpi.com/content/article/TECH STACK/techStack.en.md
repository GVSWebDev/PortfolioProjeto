---
title: "Tools Used"
date: 2020-02-03T22:25:57-03:00
tags: ['Tech Stack']
author: "Team Maya"
excludeFromIndex: true
---
### Static Gen: Hugo

<div style="text-align:center"><img src="https://cdn.discordapp.com/attachments/191299120336601097/720826865664655390/hugo-logo-wide.png" ></div>

To start building the blog, we selected a Static Gen (Static Site Generator) called Hugo, its function is to serve as the basis for a customizable theme.
Together with Hugo, we installed a theme called Billburry, the theme deals with the visual part of the blog, while Hugo with the code part. Hugo has a server
internal, using it we can generate a "preview" with the changes we made to the theme, after making considerable changes, we send the changes to our
repository on GitHub.


### Versioning: GitHub
<div style="text-align:center"><img style="width:60%" src="https://www.somagnews.com/wp-content/uploads/2020/04/75-e1586981465263.png" ></div>

GitHub is a platform in order to version projects, it is possible to create repositories and store files (of projects for example) in them. Main
reason for using GitHub for us was the possibility for all of us to work on the same project and facilitate the joining of our progress. If someone does
some modification in any file, everyone in the group will also have this modification, since the local files are linked to the repository.


### Virtualization: Amazon AWS

<div style="text-align:center"><img src= https://cuponomia-a.akamaihd.net/img/stores/original/amazon-636994893639686000.png ></div>

The Amazon AWS service has several features, we used the EC2 Manager system, this system will "run" a virtual machine with an operating system
of our choice. We use the Amazon EC2 operating system (a Linux distribution from Amazon itself). The EC2 Manager itself has a control panel outside the
virtual machine, through it we configure the firewall to have access to the machine outside the local network. After that we installed an application called Apache to "host" the blog.


### Accommodation: Apache

<div style="text-align:center"><img style="width:60%" src= https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Apache_HTTP_server_logo_%282016%29.svg/1200px-Apache_HTTP_server_logo_%282016%29.svg.png></div>

Apache allows access to HTML page outside the network, this means that with our blog configured in the Apache folder, accessing the machine's IP will automatically
redirect access to the Apache service access our blog via the internet.


### Domain: Name.com

<div style="text-align:center"><img style="width:60%" src= https://i.imgur.com/2Gx95at.png ></div>

The last step was the DNS configuration, using the Name.com website, we acquired a domain called teammaya.codes. After that, in the site settings, we configure
redirection, making sure that when typing teammaya.codes in the search bar, you are redirected to the server and automatically, due to the presence of
Apache, view the blog.