
**Use Case**

Sherri owns a small hazardous material processing company. The business serves multiple clients around her region and she has a warehouse space that is 
integral to the company function. The company’s focus is on environmental protection. One of their main functions is picking up waste from high quantity 
generators and neutralizing large quantities of hazardous chemicals, before shipping it to chemical processing plant. Given the cost saving of using a 
free open source product like Home Assistant, Sherri wants to set up her warehouse to have automatic temperature control and better physical security 
with cameras and automatic locks. Sherri buys various IoT locks, cameras and a thermostat system for monitoring and maintaining the temperature of the 
space, while having a centralized user interface through Home Assistant. She uses Home Assistant Supervisor to manage the add-ons for the IoT devices 
she uses. She sets up multiple users for her employees to access the software. She also sets up an alert on her Home Assistant UI if the temperature
falls outside the threshold settings.

**Misuse Case**

Sherri is discussing her new Home Assistant setup with her sister at the hardware store. They are talking about the temperature needed to maintain the 
chemicals being stored in the warehouse and about how Home Assistant has helped improve security. Frank, an arsonist and amateur hacker overhears the 
conversation and decides to research Home Assistant, and look up the small business address. Frank wants to steal Sherri’s credentials to access her Home 
Assistant on his device. On a particularly hot day in late July, after observing everyone leave, he uses a password attack to log in to her Home Assistant. 
He quickly changes the set temperature of the warehouse area to its highest setting. Frank’s plan is to increase the temperature in the warehouse to a 
point where one of the ignitable chemicals in storage heats to its flashpoint. At this temperature, one of the small bottles ignites and it quickly spreads 
to other ignitable chemicals. Frank watches the warehouse go up in flames. Some of the other chemicals that weren’t burned off leach into the groundwater 
and contaminate the region.

**Prevention and Security Requirement**

This misuse case could be prevented by password protected login and two-factor authentication. The assumption is that Frank would potentially be able to 
use remote access or actually be near the premises to set up access on his own device. Secure monitoring and an alert system on Sherri’s UI might prevent 
Frank from being able to change the temperature and threshold settings. If Frank was able to turn off an alert set up by Sherri somehow there would need 
to be a reminder that the alert wasn’t on.

<br>

![Use-Misuse Case Sample drawio](https://user-images.githubusercontent.com/63809979/134379865-2a5a295f-e974-4912-aff4-0a4d8b1c86fe.png)
