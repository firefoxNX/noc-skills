NOC Engineering at HubSpot
==========================

At [HubSpot](http://hubspot.com/ "HubSpot"), we're building software that will change the way that the world does marketing, and we need your help to do it.  HubSpot's Product Development team spends their days hacking on dozens of products that make marketing a delight instead of a drag, for marketers and for potential customers.

As a NOC Engineer, you'll have ownership of our entire infrastructure outside of normal working hours.  You'll be responsible for triaging anything that goes wrong with the system; fixing it if you're able; and for issues beyond your scope escalating to the appropriate Product team while documenting their response.  You'll be expected to learn a variety of technologies and methods, to quickly pick up new skills, and to apply your new skills and abilities as new problems arise.

More than anything, you'll be expected to apply your exceptional level of judgment and creativity, together with problem-solving skills, to keep our thousands of customers happy and satisfied with our software -- even when they're asleep.

This is a position that is designed with the idea that you'll grow out of it, and into a full-time role on HubSpot's TechOps, SRE, or Software Development teams.  For a candidate who is self-directed and intelligent, it's an opportunity to learn within the context of a world-class engineering team at one of Boston's best companies.


Skills Evaluation
=================
This skills evaluation is designed to give us a sense of a couple of things:
1. Your familiarity and comfort with Amazon Web Services (which we use extensively), with Git, and with the Linux command line
2. Your understanding of how different layers of a web service interact
3. Your ability to diagnose problems with code with which you are unfamiliar
4. Your ability to solve problems given limited information and context

This is not a test of what you already know how to do, it's a test of your ability to do things that you don't necessarily already know (but might).  Using Google, using documentation from around the web, or any other reference source you choose to use is perfectly fine.  We do ask that you keep rough track of the reference sources that you use, as we're likely to ask about these in an interview.

### Instructions
1. Create a fork of this GitHub Repository into your own GitHub account
2. If you do not have an Amazon Web Services account, you can create one on [the Amazon website](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html).  Note that this skills test can be completed using Amazon's [Free Usage Tier](http://aws.amazon.com/free/).
3. Launch an instance of the EC2 AMI xxxxxxxxx in Amazon's US-East region.  You will need to launch this instance with a security group that allows access from any IP address on port 8000.  You should launch this instance as a Micro Instance (t1.micro).  This will allow you to take advantage of the Free Usage Tier.
4. The expected state of the instance once it has completed launching is:
    * There will be a python django application that is listening for connections on port 8000.  This application resides in /usr/share/hubspot/NocSkillsWeb, and has a startup script at /etc/init.d/NocSkillsWeb.
    * There will be a Java application that is listening for connections on port 24080.  This application has a
    * There will be an instance of MongoDB that is listening for connections on port 27017.
    * A connection to http://<instance public ip>:8000/list will return a list of items.
5. Verify that all applications are running, and are listening on the appropriate ports.  If any of them are not, please start them up.
6. Once all applications are running, verify that the applications are working as expected.
7. If any applications are not working as expected, create a GitHub issue _on your own fork of this repository_ that documents what the problem is.

### Bonus Points
If possible, please also attempt to fix any problems that you have found.  All of the application code is located in this repository.  You should do the following:
1. Create a fix for the problem(s) that you have found.
2. Submit a pull request with the fix.