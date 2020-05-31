---
title: "Registrando e Configurando o Domínio"
date: 2020-05-30T20:25:43-03:00


categories: []
tags: ['Atualizacoes']
author: "Gabriel Vilela Serra"

---

The most challenging part of registering a domain is choosing the name ... So many creative possibilities, interesting combinations, and funny ones too. We contemplate acquiring names like ronaldinho.soccer, maya.team, teammata.wtf, among many others. In the end, we chose teammaya.codes, which matches the purpose of the site, and even sounds good. One of the main reasons that led to this choice was the fact that I got the Student package from GitHub, which gave me a 100% discount on the first domain from the provider Name.com. A good initiative from GitHub!

After "buying" the domain, I had to find out how to configure DNS. At first, I just went through the features offered by the Name.com Dashboard, until I arrived at one called "URL Forwarding", which served to redirect the domain to another URL. The first thing I did was make the domain redirect to the IP of our website. But it was not that simple apparently, because the domain still returned an error saying that it was not possible to resolve the Hostname. I kept looking, and found the DNS Records configuration panel. Some domain providers already set up "factory", but there was nothing pre-configured there. The good thing is that the site itself had a certain documentation that specified what each thing did in a very simple way to understand. There, I learned that I needed to make DNS records type A, to connect the domain to our website. I made 2 records, one for all subdomains, and another for general use, all pointing to the IP of our site.

I also took advantage and went to configure the MX records for redirecting emails, as specified in the activity. At first, I tried to do something straight with Gmail, using G Suite, until I found out it was paid. Then I looked for an alternative for Amazon. I discovered the Amazon Simple Email Service (SES) service that promised to redirect emails. For that, I needed to verify that I owned the domain by adding a TXT Record with a certain code that they provided. This process would take up to 72 hours to complete, so I did what was asked and left it at that. But curious, I still continued to research about the functionality of the Name.com Dashboard. So, I found an email redirection service for themselves! It was enough to put the email address to which they would be redirected to. In a matter of minutes, the website was already working with the correct domain, and emails were already being successfully redirected to the test email I previously configured. Success!