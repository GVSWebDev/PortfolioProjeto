---
title: "Gamer Lamp"
date: 2020-05-31T16:23:19-03:00
 

categories: []
tags: ['Projetos Pessoais']
author: "Joao Larini"
 

---

In 2017 I started a course to learn more about computer hardware and servers and their uses / configuration. At the end of the course I had to do a
conclusion work using all subjects taught. My decision was to make a lamp / lamp be connected remotely by cell phone or computer.
For this I used a micro computer called Raspberry PI,

 <div style="text-align:center"><img src="https://cdn.discordapp.com/attachments/612109572471128066/720779625034153984/web1.jpg" ></div>

 it has several buses identical to a normal computer (USB, Ethernet,
etc.) and uses a micro SD as storage. To set it up initially, I downloaded the Raspbian system iso, a variation of the Debian distribution
made especially for the Raspberry PI, as the processing power of the micro computer is relatively low (700MHz processor and 512MB of RAM)
this distro is lighter in order to run more easily on its limited hardware. Using the Rufus program to record the iso on the micro SD and
make it "bootable". 

 <div style="text-align:center"><img src="https://cdn.discordapp.com/attachments/612109572471128066/720783049322922085/web2.jpg" ></div>

After that I started to theorize the physical part of the project, the Raspberry PI has pins (same as the pins on the motherboard for
configuration of the computer's front panel) for power output, to be able to turn the lamp on or off I used a relay connected to the
pins 5 Volts and Ground, 

 <div style="text-align:center"><img style="width:60%" src=https://cdn.discordapp.com/attachments/612109572471128066/720783063545544855/web3.jpg ></div>

the relay will work as a switch (just like the ones used at home to turn on the lights), a wire will come out of the socket, will be intercepted
by the relay that will let the current pass when activated, but instead of being physically activated (press the switch with your hand to turn on the light)
it lets the current pass or does not receive the current from the raspberry pins. 

 <div style="text-align:center"><img src=https://cdn.discordapp.com/attachments/612109572471128066/720783097922191481/web4.jpg ></div>

Next step is to configure the activation of the Raspberry pins,
by default the pins do not provide power, they are in state 0, to change their state to 1 (activated) I programmed some python scripts that change the pin status, from that part the lights are already on / off when the scripts are executed, a script changes the pin state to 1, making the relay
be activated and let the current flow from the socket to the lamp and turning on the light. The other script leaves the pin status at 0 to reverse the process and
turn off the lights. From there I started working on the remote part, installed the Apache application on the raspberry that hosts web pages, and programmed a page
PHP with two buttons, one of the buttons will execute the script to turn on the lamp and the other to turn off. I used a USB network adapter to connect the
Raspberry to my local network, done that just be on the same network as him with another device and enter its internal IP address (192.168.0.X) that
Apache does the service of showing the page with the buttons, when clicking on the buttons the scripts are executed and the lamp turns on and off normally.