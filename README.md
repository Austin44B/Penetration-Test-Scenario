# Catching a Reverse Shell :

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/c6cbce54-401a-4281-b376-cc595a29974b)

Nmap is a open-source network scanning and security auditing tool allowing the ability to discover hosts, services, and open ports on a network, providing valuable information for network mapping and  vulnerability assessment. 

The "-F" Switch is used to perform a *fast scan*

-sV = Nmap switch that will try to determine the versions of services running on the target ports. This can be helpful in identifying specific software and their versions, which can be crucial for understanding potential vulnerabilities and their associated risks.

-oN = Nmap switch that is used to specify the normal output file to which Nmap will write the scan results. With this switch, you can save the scan results to a text file in a human-readable format.

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/6309728d-944c-4161-8206-b3920b6ebfc0)

<img width="444" alt="image" src="https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/45fb5318-e709-409e-80c2-999106bd8eff">

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/b63c4bfa-2daa-45d3-b434-0be4e4572b86)

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/4dba2f2f-90af-4b35-9b06-0779df966ff4)

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/6e9ff7b5-c014-4a15-8be4-25bbcd1115af)

Cross refrence vulnerabilties using [Xploit Database](https://www.exploit-db.com/)

https://httpd.apache.org/security/vulnerabilities_24.html

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/85909d4c-f5f2-4e85-83d1-a6eeefc48017)

Dirb = is a web content scanner and directory brute-forcing tool, designed to discover hidden directories and files on a web server by performing dictionary-based attacks.

tee = splits output stream to display it and save it to a file at the same time

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/da95309b-d73e-4950-8966-2d588112a354)

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/731925de-e648-466b-9c2d-fd3869abcc33)

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/a95def08-89df-4722-b831-fd797f26efe5)

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/321bba49-2743-4113-810e-a24db4774035)

Let's now set up a port forward to catch a reverse shell

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/29c9db21-4786-4f1c-b8f6-85dac2109104)

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/a6357c16-e0e8-492a-96c8-f192b78385e3)

Nc = Netcat, Used for port scanning, transferring files, and setting up network connections

-l = Listens for incoming connections on a specified port

-v = enables verbose mode, which provides more detailed output, such as connection status and data transfer information

-p = specify the port number to listen for incoming connections

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/f3563c6d-e27e-4d07-9fe6-5da26f07648b)

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/5076082c-c59a-4d76-a2ba-9b8cf5943049)

![image](https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/a435781e-5de8-4cef-bf90-db95b0b9f122)

#
#
#

# Now Let's Upgrade/harden our shell :

Validate what version of python is running on the machine.

<img width="182" alt="image" src="https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/73777d2f-4f33-4cb8-8bf7-3d0207c019e6">

Now lets perform a "PTY shell upgrade" by using a simple python script that calls a pty module to spawn a new interactive shell with more capabilities than the default shell.

<img width="645" alt="image" src="https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/6409065a-5045-4fc8-9460-c37e6f0f0554">

Now let's [resolve "unknown terminal type"](https://techtitbits.com/2010/10/resolving-unknown-unknown-terminal-type-error/) by following the linked guide, so that our attack box parimeters match our target box

<img width="962" alt="image" src="https://github.com/Austin44B/Penetration-Test-Scenario/assets/134319619/f7a5ac6d-a031-46d6-89ab-2aff9bb04001">


## and Escalate privilegs :
