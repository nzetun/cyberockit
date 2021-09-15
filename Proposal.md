# Team 2 : *Cyberockit*
*University of Nebraska Omaha, Fall 2021*

## Project Proposal 
The proposed project is an open-source software called Home-Assistant which is a home automation software used to control connected smart devices like lights, locks, security cameras, fire alarms, sprinklers, and other types of machinery. It includes an application called Supervisor which is used to install, upgrade and apply add-ons to the main Home Assistant application.

### [Home-Assistant Core](https://github.com/home-assistant/core.git)
### [Home-Assistant Supervisor](https://github.com/home-assistant/supervisor.git)
### [Team Cyberockit Repo](https://github.com/megharris/cyberockit.git)


* Home Assistant (hereafter referred to as HA)
* Home Assistant Core (hereafter referred to as Core)
* Home Assistant Supervisor (hereafter referred to as Supervisor)

## Hypothetical Working Environment
We anticipate that the user of this product is a small business, locally owned and operated. In a specific scenario, we will observe the possibility of this small business being a manufacturer and wholesaler of competitive vehicles. Therefore, the inventory and equipment on site are likely costly. Due to the detrimental effect of loss of equipment and inventory, the security of the Core and Supervisor softwares needs to be hack-proof.

As social media is frequently used as an advertising tool, customers and vendors are not the only parties aware of the value of items held by the business. Adversaries and attackers may consist of those who will try to exploit any lower and medium level openings to gain access to the main system. It is highly unlikely for the supervisor system to face high-level threats.

## Systems Engineering View Diagram

*A view of Home Assistant and its Architecture*

![Home Assistant](https://github.com/megharris/cyberockit/blob/main/images/Home%20Assistant.png) ![HA Architecture](https://github.com/megharris/cyberockit/blob/main/images/HA%20Architecture.png)

**Systems Engineering View**
![Systems Engineering View](https://github.com/megharris/cyberockit/blob/main/images/SEview.png)

### Security Needs
* Supervisor needs to block up small attack scopes found within the system by using a superior hashing algorithm like sha256 instead of sha1 or md5. It will be more secure and harder to penetrate for low and medium level attackers.

* Code snippets that are vulnerable to XSS (Cross-Site Scripting) attacks must be adjusted to prevent such attacks. It is common for nefarious actors to take advantage of this simple security flaw to gain access to this type of system. Supervisor users are vulnerable as long as these threats exist.


### Security Threats
If Core or Supervisor are hacked the entire HA will become compromised. An attacker can take advantage of a single opportunity during a system upgrade or install an add-on to gain access to the main system. 

* If the user's home system has been compromised, a thief or attacker may be able to gain physical access to the business location.
* If the user application is compromised, the attacker may be able to gain access to confidential data such as bank accounts, vendor and customer information, and other proprietary information maintained on connected devices.
* As a small business, the owner might store personal and professional information on the same devices, therefore compromising his or her personal information as well.
* Although theft is a major threat, damage to or lose of data can also be detrimental to the organization. Malware and/or ransomware can be transferred to any of the many connected devices. 
* Remote access, which uses port forwarding, poses another vulnerability as an access point for adversaries.

### Security Features
* Use two-factor authentication during irregular software upgrades or during the installation of new add-ons.
* Use VLAN to separate devices from providing information to the wrong servers.
* Enable IP ban: Bans IP address which tries to login with wrong password multiple times.
* A VPN and a firewall can prevent exploitation of port forwarding.

## Team Motivation
Given the rise of home automation products, the HA is a particularly fascinating one. Helping to integrate IoT devices from most of the major Home Automation device manufacturers, while putting individual security and flexibility first is necessary for today’s market. Most can relate to having some smart technology controlling a function in their home or workspace. The Supervisor software is particularly interesting in the way it manages the entire system while facilitating updates and providing a unique add-on experience.

We are interested in Core and Supervisor because of the roles they play in HA, and for the potential security concerns. We are excited to focus on the context of a small business user of Core and Supervisor, one that may rely heavily on the stable function of the software to manage the functionality and security of their workspace. In the small business context, Core and Supervisor have an important role in keeping information and building functions updated and secure. Some of our team members currently hold professional positions where building automation is an important aspect of the job and having a central controller of function is incredibly useful but risks must be taken into consideration: loss of machine control, financial security (if a point of sale system is integrated), community safety (if a needed stable environment is compromised). Supervisor has fascinating implications in the small business world and we are excited to explore it.


## Project Description

### What is it: HA is a home automation controller that works with all the IoT devices in a home or business. It is a container-based system that runs Core on the main device and the other devices on its network. Supervisor is a container that allows a user to install add-ons.

### Contributors: *Pascal Vizeli, Joakim Sorensen, Franck Nijhof, Paulus Schoutsen, Stefan Agner, Fabian Affolter, Bram Kragten, Martin Hjelmare, Mike Degatano, Casper Klein, Fredrik Erlandsson, Sergio Oller, Jorim Tielemans, Aidan Timson, Maximilian Bosing, Christian Schroter, Tod Schmidt, Ville Skytta, Philip Allgaier, Sean Mooney, Sergey Morozik, Halasz David, David McNett, William Johansson, Greg Rapp, Iulian Onofrei, Matheson Steplock, Justin Weberg, Michal Dinth, Curtis Gibby, Florian Jacob, Wouter Schoot, Nolan Darilek, Simon Holzmayer, Alastair D’Silva, Klaudiusz Staniek, Luca Simonetti, and Matt White.*

### Activity: Controls and monitors IoT devices on a network and can also monitor usage rates and levels of various items (eg. gas, water and power).

### Use: HA operating system powers the HA Server program, which is the backbone of the HA system. HA is controlled by using Supervisor which manages Core which includes both pre-installed and optional add-on applications. Core also comes in a Docker container version.
 
Upon installing Supervisor, the user can install the add-on programs they wish in an app-store-like menu. These apps can do anything from control lights based on motion detection to run an SQL server.

### Languages Used:
1) **Python**
2) **Docker**

### Platform:
It can be on a full desktop or a small computer, like a Raspberry Pi. HA is an application and Supervisor is the heartbeat.

## License Summary & Contribution Agreement
Per the Github page, HA is running on an Apache License 2.0, which covers commercial use, modification, distribution, patent use, and private use. The limitations of this license are trademark use, liability, and warranty.

Making contributions to HA can come in many forms: writing blog posts or commenting on various social media platforms, helping other users with issues or answering questions; writing code and posting a fork in the repository. Improving the front end of HA has been heavily worked by looking at past pull requests. Writing documentation for the project and translation of new and current documentation is also accepted by the project.

To contribute code to the program it is a standard approach: fork the repository, write new code, test to ensure that the changes work, and then create a pull request against the dev branch. The pull request will then be reviewed and accepted or denied by the project leads.

The contributor agreement for submitting new code states that any new code must be valid under Open Source/Apache 2.0 Licensing. The proposed code must also be submitted through the proper contribution steps outlined in the previous paragraph. All members, contributors and leaders will also review contributions for harassment, and unacceptable behaviour; neither of which will be tolerated.

## Security Related History

### Known Vulnerabilities:
Firefox tracking protection needs to be disabled in order to view the Web UI of certain add-ons including but not limited to Node-Red, File Editor, Portainer, SQLite Web, etc. Port forwarding allows users to access HA remotely and creates additional points of access for nefarious actors.

### Security Related Engineering Decisions:
Currently, a username and password are required to set up a profile for HA use (authentication). Single sign-on has also been enabled for add-ons. There is a password reset feature as well if the user is unable to log in with an invalid password. These are measures that prevent unauthorized access to user devices and data. HA uses certificates, logging, authentication (mentioned previously), and authorization controls as security measures. The HA Supervisor also maintains a policy that any security vulnerabilities should be reported to a specific email address (security@home-assistant.io) and not be made public. The security policy requests reporters of security vulnerabilities/violations to be validated by HA prior to making the information publicly available. 

## Teamwork Reflection
Our team struggled to identify a project that had security-related issues that we could identify. We discussed searching through projects for a specific topic (originally we looked into exam proctoring software) but unfortunately, that was a time-consuming and ineffective process. Ultimately, we found that Codetriage.com was useful in finding a project that was interesting to our team and was also in need of security measures. Additionally, we found that it was difficult to identify if the security measures that currently exist in the software were originally built into the design or if they were added on at another time. Ultimately, the timing of the creation of the security measures is difficult for us to determine. We have realized that a code review with the technical members of the team is necessary after identifying the project tasks and prior to developing solutions.

Going forward, we plan to identify the project needs, evaluate the code (technical), and then divide the project tasks among the team members. We are also continuing to evaluate the methods of communication between team members to ensure that we

### Documentation Sources:

* *The main Github page for the project.* : https://github.com/home-assistant

* *Main Openhub page for the project.* : https://www.openhub.net/p/home-assistant
 
* *A handy video about the general installation of Home Assistant.* : https://www.youtube.com/watch?v=HPYK0uVj4Z8

* *The Home Assistant website, which contains release notes, downloads, documentation, and blog posts about the software.* : https://www.home-assistant.io/

* *The Home Assistant security website.* : https://www.home-assistant.io/security/

* *The Team Cyberockit repository.* : https://github.com/megharris/cyberockit.git
