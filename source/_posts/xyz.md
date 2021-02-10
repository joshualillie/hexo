---
title: XYZ
date: 2021-02-09 19:29:12
tags:
---
### We Have DNS
My cheap ass didn't want to pay another $15 to renew joshlillie.com for another year, especially since I have a track record of abandoning these sites/blogs a few weeks or even days after I get them fired back up. But my quest to get a serverless blog set up at least halfway correctly made a domain name necessary. There's probably thousands of reasons not to run a website straight out of an S3 bucket or even with just the CloudFront domain name... but I'm not even going to bother with that discussion. Suffice to say that those names look like crap.

<img src="/images/godaddy-head.png" style="float:left;"> For my purposes, I stumbled upon a pretty sweet nugget. There is a domain called XYZ and GoDaddy offers domain names in this root domain for $1 a year. I did a little bit of research and couldn't find a reason not to use one other than nobody uses them. Good for me! Seems like an untapped resource. I grabbled a few names and now we are off! The verification process in AWS Cert Manager was very easy. So now, joshlillie.com has moved to joshlillie.xyz. It's really rather appropriate for an age where shitty reboots are all the rage.

So far this site has cost me $0.00, as opposed to the $50/month it was costing me to run an EC2 instance nonstop. Pretty saweeet. 🤘