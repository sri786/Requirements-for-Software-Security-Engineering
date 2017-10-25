Open Source Project:  Pi-hole
Authors:              Michael Galde, Carmel Waka, Olivier Avande, Srikanth Vadla
Team Name:            R3tr0

Our group "R3tr0" focused on the software security aspect for the open source project Pi-hole and have developed the following five assurance claims

Assurance Claims
-----------------
Claim 1: The Pi-hole user interface has no exploitable HTTP weakness.
The Pi-hole makes use of lighhtpd software package due to its minimal framework and the ease of which the system can be configured.

Claim 2: Pi-hole attack surface is minimized
The attack surface of the Pi-hole software is minimized by utilizing best practices approaches to software development and community involvement.

Claim 3: The Pi-Hole minimizes the possibility of device compromised during patching
and some details about this claim are

Claim 4: <  Will edit this>
and some details about this claim are

Claim 5: The Pi-hole DNS server is adequately safe from denial of service attacks**
The Pi-hole system uses dnsmasq as the underlying dns server to provide ad filtering. It is lightweight and requires minimal resources.
Like all dns services, it is exposed to denial of service. However, using the appropriate configuration it can be adequately secured.

Security Requirements
---------------------
The development of assurance cases for each and every assurance claim allowed us to develop misuse cases to address each assurance claim. The misuse cases as they relate to the assurance claims can be found on lucid chart located https://www.lucidchart.com/invitations/accept/03df13bf-2fe3-4b3c-a4bb-1493b038bd23. The development within these misuse cases allowed this team to develop the following security requirements.
Web admin interface must have a username and password set up by default with no default credentials
Web portal must be deployed with basic login authentication
Pi-hole must utilize input validation
Web portal must include account lockout policies
Whitelist mist utilize ACL
A user must be able to conduct a update of the software
Configuration implements least privilege access
Implements strong encryption from Pi-hole to user
Logs all security information
Disable user accounts with consecutive failed attempts
Utilize encryption with storage
Must include backup and recovery options
Applies recent security patches to dependent packages
Log all DNS query attempts

Open Source Project Pi-hole Documentation review
------------------------------------------------
This project can be found at https://pi-hole.net

The Pi-hole service is both a local DNS server and a web portal and the securing of these various functions is key for consumers who wish to place the devices on there internal network. Comparing the first assurance claim which is that the Pi-hole has no exploitable HTTP weakness the group took a look at what features were utilized to enable this feature. The web interface was first established in version 2.1 as a default service. The Pi-hole team decided to utilize Lighttpd as the web service as it is advertised as a secure service. Lighttpd encourages its open source community to review its product and to recommend changes for stability and security. Pi-hole pushes out updates from Lighttpd and also encourages its community to review the Pi-hole platform as well. These two sources of review allow Pi-hole to provide a web portal service with a minimized attack surface.

Follow up with Review OSS project documentation for alignment of security requirements with advertised features. Summarize your observations
Feature 1 compared to advertised features
Feature 2 compared to advertised features
Feature 3 compared to advertised features
feature 4 compared to advertised features
feature 5 compared to advertised features

Follow up with Review OSS project documentation for security related configuration and installation issues. Summarize your observations.

Conclusion








  

  



  


  






## Delete everything below this area before turn in!!

## Don't forget to push your changes up

Requirements for Software Security Engineering: 2-3 page report that describes the following:
List of final assurance claims
Describe the security requirements for the project captured using misuse case diagrams. Include links to Lucidchart mis-use cases.
Review OSS project documentation for alignment of security requirements with advertised features. Summarize your observations
Review OSS project documentation for security related configuration and installation issues. Summarize your observations.


Current assurance claims:
Claim 1: Pi-hole **admin interface** has no exploitable HTTP weaknesses
Claim 2: Pi-hole attack surface is minimized
Claim 3: The Pi-hole standard input validation minimizes the possibility of device compromise
Claim 4: Pi-Hole authentication mechanism is secure from brute force attacks
Claim 5: Pi-hole DNS is adequately safe from denial of service attack

Final Assurance claims
Claim 1: The Pi-hole user interface has no exploitable HTTP weakness
Claim 2: The Pi-hole software is designed to minimize the attack surface of the system
Claim 3: The Pi-Hole minimizes the possibility of device compromised during patching
Claim 4:
Claim 5: The Pi-hole DNS server is adequately safe from denial of service attack






Removed

While researching this open source project we discovered the following security requirements while simulating the following misuse requirements.
The first identified security requirements involved securing the Pi-hole software from general malicious threat actors. These threat actors are sometimes identified as script kiddies or unfocused threat actors who may or may not know the attack surface area. Pi-hole accomplishes this by limiting the amount of services identified outside of the networked environment. The Pi-hole software utilizes lighttpd as its web client which is marketed as a secure web platform by utilizing few resources outside of the application.
**Functional Security Requirements**
**DNS request monitoring**
The pi-hole system as a whole should have the ability to log all dns query attempts in a manner that allows the user to detect anomalous traffic. The interface for this
should be user-friendly and intuitive to allow log analysis.
**IP address blacklisting**
The pi-hole system should provide user the ability to blacklist suspicious IP address source that are suspected to be carrying a Denial of service attack
**Support for DNSSEC**
DNSSEC is a mechanism that allow DNS request validation. Each DNS transactions is signed. It mitigates DNS cache poisoning that can be a form of Denial of Service.








## Delete everything above this for final turn in
