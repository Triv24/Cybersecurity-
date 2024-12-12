## How intrusions compromise your system :

- In this section of the course, you learned that every network has inherent vulnerabilities and could become the target of a network attack.

- Attackers could have varying motivations for attacking your organization’s network.
- They may have financial, personal, or political motivations, or they may be a disgruntled employee or an activist who disagrees with the company's values and wants to harm an organization’s operations.
- Malicious actors can target any network.
- Security analysts must be constantly alert to potential vulnerabilities in their organization’s network and take quick action to mitigate them.

- In this reading, you’ll learn about `network interception attacks` and `backdoor attacks`, and the possible impacts these attacks could have on an organization.

### Network interception attacks :

- Network interception attacks work by intercepting network traffic and stealing valuable information or interfering with the transmission in some way.

- Malicious actors can use hardware or software tools to capture and inspect data in transit.
- This is referred to as packet sniffing.
- In addition to seeing information that they are not entitled to, malicious actors can also intercept network traffic and alter it.
- These attacks can cause damage to an organization’s network by inserting malicious code modifications or altering the message and interrupting network operations.
- For example, an attacker can intercept a bank transfer and change the account receiving the funds to one that the attacker controls.

- Later in this course you will learn more about malicious packet sniffing, and other types of network interception attacks: on-path attacks and replay attacks.

### Backdoor attacks :

- A backdoor attack is another type of attack you will need to be aware of as a security analyst.
- An organization may have a lot of security measures in place, including cameras, biometric scans and access codes to keep employees from entering and exiting without being seen.
- However, an employee might work around the security measures by finding a backdoor to the building that is not as heavily monitored, allowing them to sneak out for the afternoon without being seen. 

- In cybersecurity, backdoors are weaknesses intentionally left by programmers or system and network administrators that bypass normal access control mechanisms.
- Backdoors are intended to help programmers conduct troubleshooting or administrative tasks.
- However, backdoors can also be installed by attackers after they’ve compromised an organization to ensure they have persistent access.

- Once the hacker has entered an insecure network through a backdoor, they can cause extensive damage: installing malware, performing a denial of service (DoS) attack, stealing private information or changing other security settings that leaves the system vulnerable to other attacks.
> A DoS attack is an attack that targets a network or server and floods it with network traffic.

### Possible impacts on an organization :

As you’ve learned already, network attacks can have a significant negative impact on an organization. Let’s examine some potential consequences.

1. **Financial**:
   - When a system is taken offline with a DoS attack or some other tactic, they prevent a company from performing  tasks that generate revenue.
   - Depending on the size of an organization, interrupted operations can cost millions of dollars.
   - Reparation costs to rebuild software infrastructure and to pay large sums associated with potential ransomware can be financially difficult.
   - In addition, if a malicious actor gets access to the personal information of the company’s clients or customers, the company may face heavy litigation and settlement costs if customers seek legal recourse.

2. **Reputation**:
   - Attacks can also have a negative impact on the reputation of an organization.
   - If it becomes public knowledge that a company has experienced a cyber attack, the public may become concerned about the security practices of the organization.
   - They may stop trusting the company with their personal information and choose a competitor to fulfill their needs.

3. **Public safety**:
   - If an attack occurs on a government network, this can potentially impact the safety and welfare of the citizens of a country.
   - In recent years, defense agencies across the globe are investing heavily in combating cyber warfare tactics.
   - If a malicious actor gained access to a power grid, a public water system, or even a military defense communication system, the public could face physical harm due to a network intrusion attack.
  
# Read tcpdump logs :
- A network protocol analyzer, sometimes called a packet sniffer or a packet analyzer, is a tool designed to capture and analyze data traffic within a network.
- They are commonly used as investigative tools to monitor networks and identify suspicious activity.
- There are a wide variety of network protocol analyzers available, but some of the most common analyzers  include:
  1. SolarWinds NetFlow Traffic Analyzer
  2. ManageEngine OpManager
  3. Azure Network Watcher
  4. Wireshark
  5. tcpdump

- This reading will focus exclusively on tcpdump, though you can apply what you learn here to many of the other network protocol analyzers you'll use as a cybersecurity analyst to defend against any network intrusions. In an upcoming activity, you’ll review a tcpdump data traffic log and identify a DoS attack to practice these skills.

### **tcpdump**  :

- **tcpdump** is a command-line network protocol analyzer.
- It is popular, lightweight–meaning it uses little memory and has a low CPU usage–and uses the `open-source libpcap library`.
- tcpdump is text based, meaning all commands in tcpdump are executed in the terminal.
- It can also be installed on other Unix-based operating systems, such as macOS®.
- It is preinstalled on many Linux distributions.

- tcpdump provides a brief packet analysis and converts key information about network traffic into formats easily read by humans.
- It prints information about each packet directly into your terminal.
- tcpdump also displays the source IP address, destination IP addresses, and the port numbers being used in the communications.

#### Interpreting output :

- tcpdump prints the output of the command as the sniffed packets in the command line, and optionally to a log file, after a command is executed.
- The output of a packet capture contains many pieces of important information about the network traffic.

![image](https://github.com/user-attachments/assets/8df63956-7bcc-4ce5-813c-85a23a767d6c)

##### Some information you receive from a packet capture includes : 

- **Timestamp**: The output begins with the timestamp, formatted as hours, minutes, seconds, and fractions of a second.  

- **Source IP**: The packet’s origin is provided by its source IP address.

- **Source port**: This port number is where the packet originated.

- **Destination IP**: The destination IP address is where the packet is being transmitted to.

- **Destination port**: This port number is where the packet is being transmitted to.

#### Common uses :

- tcpdump and other network protocol analyzers are commonly used to capture and view network communications and to collect statistics about the network, such as troubleshooting network performance issues.
  
- They can also be used to:
  - Establish a baseline for network traffic patterns and network utilization metrics.
  - Detect and identify malicious traffic  
  - Create customized alerts to send the right notifications when network issues or security threats arise.
  - Locate unauthorized instant messaging (IM), traffic, or wireless access points.

However, attackers can also use network protocol analyzers maliciously to gain information about a specific network. 
- For example, attackers can capture data packets that contain sensitive information, such as account usernames and passwords.
- As a cybersecurity analyst, It’s important to understand the purpose and uses of network protocol analyzers.
  
> Note: By default, tcpdump will attempt to resolve host addresses to hostnames.
> It'll also replace port numbers with commonly associated services that use these ports.

# Real-life DDoS attack :

Previously, you were introduced to Denial of Service (DoS) attacks. You also learned that volumetric distributed DoS (DDoS) attacks overwhelm a network by sending unwanted data packets in such large quantities that the servers become unable to service normal users. This can be detrimental to an organization. When systems fail, organizations cannot meet their customers' needs. They often lose money, and in some cases, incur other losses. An organization’s reputation may also suffer if news of a successful DDoS attack reaches consumers, who then question the security of the organization.

In this reading you’ll learn about a 2016 DDoS attack against DNS servers that caused major outages at multiple organizations that have millions of daily users.

### A DDoS targeting a widely used DNS server :

- In previous videos, you learned about the function of a DNS server.
- DNS servers translate website domain names into the IP address of the system that contains the information for the website.
- For instance, if a user were to type in a website URL, a DNS server would translate that into a numeric IP address that directs network traffic to the location of the website’s server. 

- On the day of the DDoS attack we are studying, many large companies were using a DNS service provider.
- The service provider was hosting the DNS system for these companies.
- This meant that when internet users typed in the URL of the website they wanted to access, their devices would be directed to the right place.
- On October 21, 2016, the service provider was the victim of a DDoS attack.

### Leading up to the attack :

- Before the attack on the service provider, a group of university students created a botnet with the intention to attack various gaming servers and networks.
- A botnet is a collection of computers infected by malware that are under the control of a single threat actor, known as the “bot-herder."
- Each computer in the botnet can be remotely controlled to send a data packet to a target system.
- In a botnet attack, cyber criminals instruct all the bots on the botnet to send data packets to the target system at the same time, resulting in a DDoS attack.

- The group of university students posted the code for the botnet online so that it would be accessible to thousands of internet users and authorities wouldn’t be able to trace the botnet back to the students.
- In doing so, they made it possible for other malicious actors to learn the code to the botnet and control it remotely.
- This included the cyber criminals who attacked the DNS service provider.

### The day of attack :

- At 7:00 a.m. on the day of the attack, the botnet sent tens of millions of DNS requests to the service provider.
- This overwhelmed the system and the DNS service shut down.
- This meant that all of the websites that used the service provider could not be reached.
- When users tried to access various websites that used the service provider, they were not directed to the website they typed in their browser.
- Outages for each web service occurred all over North America and Europe. 

- The service provider’s systems were restored after only two hours of downtime.
- Although the cyber criminals sent subsequent waves of botnet attacks, the DNS company was prepared and able to mitigate the impact.

