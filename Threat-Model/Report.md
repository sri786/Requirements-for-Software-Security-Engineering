Pi-hole Threat Model
====================

R3tr0 evaluated the open source software Pi-hole utilizing the Microsoft Threat modeling tool 2016 and the previous [misuse cases](https://www.lucidchart.com/invitations/accept/03df13bf-2fe3-4b3c-a4bb-1493b038bd23) which allowed the group to identify the threat model against the Pi-hole process. Retr0 developed a level 1 DFD which supports all threats identified within the previous misuse cases within Lucid Chart located [here.](https://www.lucidchart.com/invitations/accept/03df13bf-2fe3-4b3c-a4bb-1493b038bd23)

R3tr0 analyzed this diagram and by utilizing the STRIDE model we have identified the following threats as outlined below. 

Spoofing
--------

**1.** Spoofing of Source Data Store Blacklist  [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	Blacklist may be spoofed by an attacker and this may lead to incorrect data delivered to Network Traffic Result. Consider using a standard authentication mechanism to identify the source data store.
Justification:	<no mitigation provided>

**7.** Spoofing of Destination Data Store Blacklist  [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	Blacklist may be spoofed by an attacker and this may lead to data being written to the attacker's target instead of Blacklist. Consider using a standard authentication mechanism to identify the destination data store.
Justification:	<no mitigation provided>

**8.** Spoofing of Destination Data Store Whitelist   [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	Whitelist  may be spoofed by an attacker and this may lead to data being written to the attacker's target instead of Whitelist . Consider using a standard authentication mechanism to identify the destination data store.
Justification:	<no mitigation provided>

**10.** Spoofing of Destination Data Store DNS log  [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	DNS log may be spoofed by an attacker and this may lead to data being written to the attacker's target instead of DNS log. Consider using a standard authentication mechanism to identify the destination data store.
Justification:	<no mitigation provided>

**15.** Spoofing the User External Entity  [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	User may be spoofed by an attacker and this may lead to unauthorized access to Pi-hole. Consider using a standard authentication mechanism to identify the external entity.
Justification:	<no mitigation provided>

**17.** Spoofing the Pi-hole Process  [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	Pi-hole may be spoofed by an attacker and this may lead to information disclosure by User. Consider using a standard authentication mechanism to identify the destination process.
Justification:	<no mitigation provided>

**27.** Spoofing of Source Data Store DNS log  [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	DNS log may be spoofed by an attacker and this may lead to incorrect data delivered to Pi-hole. Consider using a standard authentication mechanism to identify the source data store.
Justification:	<no mitigation provided>

**28.** Spoofing of the User External Destination Entity  [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	User may be spoofed by an attacker and this may lead to data being sent to the attacker's target instead of User. Consider using a standard authentication mechanism to identify the external entity.
Justification:	<no mitigation provided>

**31.** Spoofing of Source Data Store Whitelist   [State: Not Started]  [Priority: High] 

Category:	Spoofing
Description:	Whitelist  may be spoofed by an attacker and this may lead to incorrect data delivered to Network Traffic Result. Consider using a standard authentication mechanism to identify the source data store.
Justification:	<no mitigation provided>


Tampering
---------

**11.** The DNS log Data Store Could Be Corrupted  [State: Not Started]  [Priority: High] 

Category:	Tampering
Description:	Data flowing across DNS Query may be tampered with by an attacker. This may lead to corruption of DNS log. Ensure the integrity of the data flow to the data store.
Justification:	<no mitigation provided>

**18.** Potential Lack of Input Validation for Pi-hole  [State: Not Started]  [Priority: High] 

Category:	Tampering
Description:	Data flowing across Input Data Flow may be tampered with by an attacker. This may lead to a denial of service attack against Pi-hole or an elevation of privilege attack against Pi-hole or an information disclosure by Pi-hole. Failure to verify that input is as expected is a root cause of a very large number of exploitable issues. Consider all paths and the way they handle data. Verify that all input is verified for correctness using an approved list input validation approach.
Justification:	<no mitigation provided>

Repudiation
-----------

**3.** External Entity Network Traffic Result Potentially Denies Receiving Data  [State: Not Started]  [Priority: High] 

Category:	Repudiation
Description:	Network Traffic Result claims that it did not receive data from a process on the other side of the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.
Justification:	<no mitigation provided>

**12.** Data Store Denies DNS log Potentially Writing Data  [State: Not Started]  [Priority: High] 

Category:	Repudiation
Description:	DNS log claims that it did not write data received from an entity on the other side of the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.
Justification:	<no mitigation provided>

**19.** Potential Data Repudiation by Pi-hole  [State: Not Started]  [Priority: High] 

Category:	Repudiation
Description:	Pi-hole claims that it did not receive data from a source outside the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.
Justification:	<no mitigation provided>

**29.** External Entity User Potentially Denies Receiving Data  [State: Not Started]  [Priority: High] 

Category:	Repudiation
Description:	User claims that it did not receive data from a process on the other side of the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.
Justification:	<no mitigation provided>

**33.** External Entity Network Traffic Result Potentially Denies Receiving Data  [State: Not Started]  [Priority: High] 

Category:	Repudiation
Description:	Network Traffic Result claims that it did not receive data from a process on the other side of the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.
Justification:	<no mitigation provided>

Information Disclosure
-----------------------

**2.** Weak Access Control for a Resource  [State: Not Started]  [Priority: High] 

Category:	Information Disclosure
Description:	Improper data protection of Blacklist can allow an attacker to read information not intended for disclosure. Review authorization settings.
Justification:	<no mitigation provided>

**20.** Data Flow Sniffing  [State: Not Started]  [Priority: High] 

Category:	Information Disclosure
Description:	Data flowing across Input Data Flow may be sniffed by an attacker. Depending on what type of data an attacker can read, it may be used to attack other parts of the system or simply be a disclosure of information leading to compliance violations. Consider encrypting the data flow.
Justification:	<no mitigation provided>

**26.** Weak Access Control for a Resource  [State: Not Started]  [Priority: High] 

Category:	Information Disclosure
Description:	Improper data protection of DNS log can allow an attacker to read information not intended for disclosure. Review authorization settings.
Justification:	<no mitigation provided>

**32.** Weak Access Control for a Resource  [State: Not Started]  [Priority: High] 

Category:	Information Disclosure
Description:	Improper data protection of Whitelist  can allow an attacker to read information not intended for disclosure. Review authorization settings.
Justification:	<no mitigation provided>

Denial of Service
------------------

**4.** Data Flow Block Traffic Is Potentially Interrupted  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	An external agent interrupts data flowing across a trust boundary in either direction.
Justification:	<no mitigation provided>

**5.** Data Store Inaccessible  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	An external agent prevents access to a data store on the other side of the trust boundary.
Justification:	<no mitigation provided>

**6.** Potential Excessive Resource Consumption for Pi-hole or Blacklist  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	Does Pi-hole or Blacklist take explicit steps to control resource consumption? Resource consumption attacks can be hard to deal with, and there are times that it makes sense to let the OS do the job. Be careful that your resource requests don't deadlock, and that they do timeout.
Justification:	<no mitigation provided>

**9.** Potential Excessive Resource Consumption for Pi-hole or Whitelist   [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	Does Pi-hole or Whitelist  take explicit steps to control resource consumption? Resource consumption attacks can be hard to deal with, and there are times that it makes sense to let the OS do the job. Be careful that your resource requests don't deadlock, and that they do timeout.
Justification:	<no mitigation provided>

**13.** Data Flow DNS Query Is Potentially Interrupted  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	An external agent interrupts data flowing across a trust boundary in either direction.
Justification:	<no mitigation provided>

**14.** Data Store Inaccessible  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	An external agent prevents access to a data store on the other side of the trust boundary.
Justification:	<no mitigation provided>
          
**21.** Potential Process Crash or Stop for Pi-hole  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	Pi-hole crashes, halts, stops or runs slowly; in all cases violating an availability metric.
Justification:	<no mitigation provided>

**22.** Data Flow Input Data Flow Is Potentially Interrupted  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	An external agent interrupts data flowing across a trust boundary in either direction.
Justification:	<no mitigation provided>

**30.** Data Flow Output Data Flow Is Potentially Interrupted  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	An external agent interrupts data flowing across a trust boundary in either direction.
Justification:	<no mitigation provided>

**34.** Data Flow Pass Traffic Is Potentially Interrupted  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	An external agent interrupts data flowing across a trust boundary in either direction.
Justification:	<no mitigation provided>

**35.** Data Store Inaccessible  [State: Not Started]  [Priority: High] 

Category:	Denial Of Service
Description:	An external agent prevents access to a data store on the other side of the trust boundary.
Justification:	<no mitigation provided>

Elevation of Privilege
----------------------

**16.** Elevation Using Impersonation  [State: Not Started]  [Priority: High] 

Category:	Elevation Of Privilege
Description:	Pi-hole may be able to impersonate the context of User in order to gain additional privilege.
Justification:	<no mitigation provided>

**23.** Pi-hole May be Subject to Elevation of Privilege Using Remote Code Execution  [State: Not Started]  [Priority: High] 

Category:	Elevation Of Privilege
Description:	User may be able to remotely execute code for Pi-hole.
Justification:	<no mitigation provided>

**24.** Elevation by Changing the Execution Flow in Pi-hole  [State: Not Started]  [Priority: High] 

Category:	Elevation Of Privilege
Description:	An attacker may pass data into Pi-hole in order to change the flow of program execution within Pi-hole to the attacker's choosing.
Justification:	<no mitigation provided>

**25.** Cross Site Request Forgery  [State: Not Started]  [Priority: High] 

Category:	Elevation Of Privilege
Description:	Cross-site request forgery (CSRF or XSRF) is a type of attack in which an attacker forces a user's browser to make a forged request to a vulnerable site by exploiting an existing trust relationship between the browser and the vulnerable web site.  In a simple scenario, a user is logged in to web site A using a cookie as a credential.  The other browses to web site B.  Web site B returns a page with a hidden form that posts to web site A.  Since the browser will carry the user's cookie to web site A, web site B now can take any action on web site A, for example, adding an admin to an account.  The attack can be used to exploit any requests that the browser automatically authenticates, e.g. by session cookie, integrated authentication, IP whitelisting, …  The attack can be carried out in many ways such as by luring the victim to a site under control of the attacker, getting the user to click a link in a phishing email, or hacking a reputable web site that the victim will visit. The issue can only be resolved on the server side by requiring that all authenticated state-changing requests include an additional piece of secret payload (canary or CSRF token) which is known only to the legitimate web site and the browser and which is protected in transit through SSL/TLS. See the Forgery Protection property on the flow stencil for a list of mitigations.
Justification:	<no mitigation provided>



Current threat model 
====================
<p align="center">
<img src="https://user-images.githubusercontent.com/30883926/32418624-24d1885c-c233-11e7-9a2f-fc308bb050e2.jpg">
</p>



<body><h1 class="title" tabindex="0">Threat Modeling Report</h1><span tabindex="0">
          Created on 11/8/2017 5:30:00 PM</span><p tabindex="0"><strong>Threat Model Name: Pi-hole Threat Model</strong></p><p tabindex="0"><strong>Owner: R3tr0 </strong></p><p tabindex="0"><strong>Reviewer: Michael Galde </strong></p><p tabindex="0"><strong>Contributors: Carmel, Olivier, Srikanth </strong></p><p tabindex="0"><strong>Description: A review of the Pi-hole threat model</strong></p><p tabindex="0"><strong>Assumptions: We assume a clean insall on a Raspberry Pi ** Add More Here **</strong></p><p tabindex="0"><strong>External Dependencies: </strong></p><br /><h3 tabindex="0">Threat Model Summary:</h3><table><tr tabindex="0" role="row"><td>Not Started</td><td>35</td></tr><tr tabindex="0" role="row"><td>Not Applicable</td><td>0</td></tr><tr tabindex="0" role="row"><td>Needs Investigation</td><td>0</td></tr><tr tabindex="0" role="row"><td>Mitigation Implemented</td><td>0</td></tr><tr tabindex="0" role="row"><td>Total</td><td>35</td></tr><tr tabindex="0" role="row"><td>Total Migrated</td><td>0</td></tr></table><p class="bugtrack" /><hr /><h2 tabindex="0">

Diagram: Pi-hole overview</h2>
<img src="https://user-images.githubusercontent.com/30883926/32421596-e1c10984-c25f-11e7-8ac2-ead95c84d45d.png"/><h3 tabindex="0">Pi-hole overview Summary:
          </h3><table><tr tabindex="0" role="row"><td>Not Started</td><td>35</td></tr><tr tabindex="0" role="row"><td>Not Applicable</td><td>0</td></tr><tr tabindex="0" role="row"><td>Needs Investigation</td><td>0</td></tr><tr tabindex="0" role="row"><td>Mitigation Implemented</td><td>0</td></tr><tr tabindex="0" role="row"><td>Total</td><td>35</td></tr><tr tabindex="0" role="row"><td>Total Migrated</td><td>0</td></tr></table><h3 tabindex="0">


Interaction: Block Traffic</h3><img src="https://user-images.githubusercontent.com/30883926/32421706-9f656cbe-c260-11e7-88d5-4e72f2336214.png"/><div class="threat"><h4 tabindex="0" id="&#xA;          t1"><span>1. Spoofing of Source Data Store Blacklist</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Blacklist may be spoofed by an attacker and this may lead to incorrect data delivered to Network Traffic Result. Consider using a standard authentication mechanism to identify the source data store.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td>

<td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t2"><span>2. Weak Access Control for a Resource</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Information Disclosure</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Improper data protection of Blacklist can allow an attacker to read information not intended for disclosure. Review authorization settings.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t3"><span>3. External Entity Network Traffic Result Potentially Denies Receiving Data</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Repudiation</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Network Traffic Result claims that it did not receive data from a process on the other side of the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t4"><span>4. Data Flow Block Traffic Is Potentially Interrupted</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An external agent interrupts data flowing across a trust boundary in either direction.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t5"><span>5. Data Store Inaccessible</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An external agent prevents access to a data store on the other side of the trust boundary.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><br /><h3 tabindex="0">
      
Interaction: Compare Check</h3><img src="https://user-images.githubusercontent.com/30883926/32421766-0b3f6eb2-c261-11e7-8e4a-a2c0e337effd.png"/><div class="threat"><h4 tabindex="0" id="&#xA;          t6"><span>6. Potential Excessive Resource Consumption for Pi-hole or Blacklist</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Does Pi-hole or Blacklist take explicit steps to control resource consumption? Resource consumption attacks can be hard to deal with, and there are times that it makes sense to let the OS do the job. Be careful that your resource requests don't deadlock, and that they do timeout.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t7"><span>7. Spoofing of Destination Data Store Blacklist</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Blacklist may be spoofed by an attacker and this may lead to data being written to the attacker's target instead of Blacklist. Consider using a standard authentication mechanism to identify the destination data store.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><br /><h3 tabindex="0">

Interaction: Compare Check</h3><img src="https://user-images.githubusercontent.com/30883926/32421811-59743824-c261-11e7-8f98-250d5a629bcc.png"/><div class="threat"><h4 tabindex="0" id="&#xA;          t8"><span>8. Spoofing of Destination Data Store Whitelist </span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Whitelist  may be spoofed by an attacker and this may lead to data being written to the attacker's target instead of Whitelist . Consider using a standard authentication mechanism to identify the destination data store.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t9"><span>9. Potential Excessive Resource Consumption for Pi-hole or Whitelist </span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Does Pi-hole or Whitelist  take explicit steps to control resource consumption? Resource consumption attacks can be hard to deal with, and there are times that it makes sense to let the OS do the job. Be careful that your resource requests don't deadlock, and that they do timeout.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><br /><h3 tabindex="0">
      Interaction: DNS Query</h3><img tabindex="0" src="https://user-images.githubusercontent.com/30883926/32421845-9e8404b2-c261-11e7-9bb9-985dfeb545b0.png"/><div class="threat"><h4 tabindex="0" id="&#xA;          t10"><span>10. Spoofing of Destination Data Store DNS log</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">DNS log may be spoofed by an attacker and this may lead to data being written to the attacker's target instead of DNS log. Consider using a standard authentication mechanism to identify the destination data store.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t11"><span>11. The DNS log Data Store Could Be Corrupted</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Tampering</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Data flowing across DNS Query may be tampered with by an attacker. This may lead to corruption of DNS log. Ensure the integrity of the data flow to the data store.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t12"><span>12. Data Store Denies DNS log Potentially Writing Data</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Repudiation</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">DNS log claims that it did not write data received from an entity on the other side of the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t13"><span>13. Data Flow DNS Query Is Potentially Interrupted</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An external agent interrupts data flowing across a trust boundary in either direction.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t14"><span>14. Data Store Inaccessible</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An external agent prevents access to a data store on the other side of the trust boundary.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><br /><h3 tabindex="0">
     
Interaction: Input Data Flow</h3><img src="https://user-images.githubusercontent.com/30883926/32421938-784c6d38-c262-11e7-9860-f4c48b1f09e0.png"/> <div class="threat"><h4 tabindex="0" id="&#xA;          t15"><span>15. Spoofing the User External Entity</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">User may be spoofed by an attacker and this may lead to unauthorized access to Pi-hole. Consider using a standard authentication mechanism to identify the external entity.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t16"><span>16. Elevation Using Impersonation</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Elevation Of Privilege</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Pi-hole may be able to impersonate the context of User in order to gain additional privilege.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t17"><span>17. Spoofing the Pi-hole Process</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Pi-hole may be spoofed by an attacker and this may lead to information disclosure by User. Consider using a standard authentication mechanism to identify the destination process.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t18"><span>18. Potential Lack of Input Validation for Pi-hole</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Tampering</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Data flowing across Input Data Flow may be tampered with by an attacker. This may lead to a denial of service attack against Pi-hole or an elevation of privilege attack against Pi-hole or an information disclosure by Pi-hole. Failure to verify that input is as expected is a root cause of a very large number of exploitable issues. Consider all paths and the way they handle data. Verify that all input is verified for correctness using an approved list input validation approach.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t19"><span>19. Potential Data Repudiation by Pi-hole</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Repudiation</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Pi-hole claims that it did not receive data from a source outside the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t20"><span>20. Data Flow Sniffing</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Information Disclosure</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Data flowing across Input Data Flow may be sniffed by an attacker. Depending on what type of data an attacker can read, it may be used to attack other parts of the system or simply be a disclosure of information leading to compliance violations. Consider encrypting the data flow.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t21"><span>21. Potential Process Crash or Stop for Pi-hole</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Pi-hole crashes, halts, stops or runs slowly; in all cases violating an availability metric.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t22"><span>22. Data Flow Input Data Flow Is Potentially Interrupted</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An external agent interrupts data flowing across a trust boundary in either direction.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t23"><span>23. Pi-hole May be Subject to Elevation of Privilege Using Remote Code Execution</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Elevation Of Privilege</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">User may be able to remotely execute code for Pi-hole.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t24"><span>24. Elevation by Changing the Execution Flow in Pi-hole</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Elevation Of Privilege</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An attacker may pass data into Pi-hole in order to change the flow of program execution within Pi-hole to the attacker's choosing.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t25"><span>25. Cross Site Request Forgery</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Elevation Of Privilege</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Cross-site request forgery (CSRF or XSRF) is a type of attack in which an attacker forces a user's browser to make a forged request to a vulnerable site by exploiting an existing trust relationship between the browser and the vulnerable web site.  In a simple scenario, a user is logged in to web site A using a cookie as a credential.  The other browses to web site B.  Web site B returns a page with a hidden form that posts to web site A.  Since the browser will carry the user's cookie to web site A, web site B now can take any action on web site A, for example, adding an admin to an account.  The attack can be used to exploit any requests that the browser automatically authenticates, e.g. by session cookie, integrated authentication, IP whitelisting, …  The attack can be carried out in many ways such as by luring the victim to a site under control of the attacker, getting the user to click a link in a phishing email, or hacking a reputable web site that the victim will visit. The issue can only be resolved on the server side by requiring that all authenticated state-changing requests include an additional piece of secret payload (canary or CSRF token) which is known only to the legitimate web site and the browser and which is protected in transit through SSL/TLS. See the Forgery Protection property on the flow stencil for a list of mitigations.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><br /><h3 tabindex="0">

Interaction: InputData Flow</h3><img src="https://user-images.githubusercontent.com/30883926/32421921-3a9b7fba-c262-11e7-8b6b-3413df8ac2ae.png"/><div class="threat"><h4 tabindex="0" id="&#xA;          t26"><span>26. Weak Access Control for a Resource</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Information Disclosure</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Improper data protection of DNS log can allow an attacker to read information not intended for disclosure. Review authorization settings.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t27"><span>27. Spoofing of Source Data Store DNS log</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">DNS log may be spoofed by an attacker and this may lead to incorrect data delivered to Pi-hole. Consider using a standard authentication mechanism to identify the source data store.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><br /><h3 tabindex="0">

Interaction: Output Data Flow</h3><img src="https://user-images.githubusercontent.com/30883926/32421976-ce31cf36-c262-11e7-8cdf-7f984d382c75.png"/><div class="threat"><h4 tabindex="0" id="&#xA;          t28"><span>28. Spoofing of the User External Destination Entity</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">User may be spoofed by an attacker and this may lead to data being sent to the attacker's target instead of User. Consider using a standard authentication mechanism to identify the external entity.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t29"><span>29. External Entity User Potentially Denies Receiving Data</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Repudiation</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">User claims that it did not receive data from a process on the other side of the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t30"><span>30. Data Flow Output Data Flow Is Potentially Interrupted</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An external agent interrupts data flowing across a trust boundary in either direction.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><br /><h3 tabindex="0">

Interaction: Pass Traffic</h3><img tabindex="0" src="https://user-images.githubusercontent.com/30883926/32421991-f4ee7d90-c262-11e7-94a4-5a5573eae9d8.png"/><div class="threat"><h4 tabindex="0" id="&#xA;          t31"><span>31. Spoofing of Source Data Store Whitelist </span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Spoofing</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Whitelist  may be spoofed by an attacker and this may lead to incorrect data delivered to Network Traffic Result. Consider using a standard authentication mechanism to identify the source data store.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t32"><span>32. Weak Access Control for a Resource</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Information Disclosure</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Improper data protection of Whitelist  can allow an attacker to read information not intended for disclosure. Review authorization settings.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t33"><span>33. External Entity Network Traffic Result Potentially Denies Receiving Data</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Repudiation</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">Network Traffic Result claims that it did not receive data from a process on the other side of the trust boundary. Consider using logging or auditing to record the source, time, and summary of the received data.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t34"><span>34. Data Flow Pass Traffic Is Potentially Interrupted</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An external agent interrupts data flowing across a trust boundary in either direction.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><div class="threat"><h4 tabindex="0" id="&#xA;          t35"><span>35. Data Store Inaccessible</span> 
        [State: Not Started] 
        [Priority: High] 
        </h4><table role="grid"><tr><td id="threat-title-category" role="rowheader" tabindex="0"><strong>Category:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-category">Denial Of Service</td></tr><tr><td id="threat-title-description" role="rowheader" tabindex="0"><strong>Description:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-description">An external agent prevents access to a data store on the other side of the trust boundary.</td></tr><tr><td id="threat-title-justification" role="rowheader" tabindex="0"><strong>Justification:</strong></td><td class="infotd" tabindex="0" role="gridcell" headers="threat-title-justification">&lt;no mitigation provided&gt;</td></tr></table></div><br /></body></html>
