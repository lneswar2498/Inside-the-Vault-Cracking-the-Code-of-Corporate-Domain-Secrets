# Inside-the-Vault-Cracking-the-Code-of-Corporate-Domain-Secrets
Hands-on Active Directory security assessment using Kali Linux, Nmap, LDAP, Metasploit, and Sysinternals in a Windows Server lab environment.


Project Overview
=================

In this project, I created a Windows Active Directory lab environment and performed different security assessment activities to understand how a corporate domain works and what information can be discovered during a security assessment.

I used Windows Server 2022 as the domain controller and Kali Linux as the security testing machine.

The project involved setting up Active Directory, creating domain users, scanning network services, enumerating SMB and LDAP information, exploring domain objects, and performing controlled security testing using Metasploit.

I also explored Windows system information using Sysinternals tools and analyzed a test payload using VirusTotal.

The main purpose of this project was to gain hands-on experience with Active Directory security, network enumeration, and common techniques used during penetration testing.

Tools and Technologies Used

Windows Server 2022

Kali Linux

Oracle VirtualBox

Active Directory Domain Services (AD DS)

Nmap

Enum4linux

LDAPSearch

LDAPDomainDump

Metasploit Framework

Sysinternals AD Explorer

Sysinternals PsList

Sysinternals PsLoggedOn

Python HTTP Server

VirusTotal

Project Implementation

STEP-1:- Setting Up the Lab Environment

I started by preparing my Windows Server 2022 virtual machine and Kali Linux machine in VirtualBox.

Windows Server was used as the target domain environment, while Kali Linux was used to perform the security assessment.

I checked the network connectivity and prepared the virtual machines for the practical exercises.

STEP-2:- Installing Active Directory Domain Services

After preparing Windows Server, I opened Server Manager and selected Add Roles and Features.

I installed Active Directory Domain Services (AD DS) and promoted the server to a domain controller.

This allowed me to create and manage a Windows domain environment similar to what organizations use for centralized user and computer management.

STEP-3:- Creating and Managing Domain Users

Once the domain controller was configured, I opened Active Directory Users and Computers.

I created a test user account, assigned a password, and verified that the account appeared in the domain.

This helped me understand how domain administrators create and manage user accounts.

STEP-4:- Performing Initial Network Scanning

After configuring the domain environment, I moved to Kali Linux and performed an initial network scan using Nmap.

The scan helped me identify the services running on the Windows Server machine.

I observed services associated with Active Directory, including DNS, Kerberos, LDAP, and SMB.

This gave me an initial understanding of the target machine's network exposure.

STEP-5:- Enumerating SMB Shares

Next, I used Nmap's SMB enumeration capabilities to identify shared resources available on the Windows machine.

I examined the discovered shares and their reported access information.

This step helped me understand how SMB services expose shared resources and why organizations need appropriate access controls.

STEP-6:- Identifying Operating System and SMB Information

I performed additional Nmap scans to gather operating system and SMB-related information.

I focused on identifying the Windows Server version, SMB service details, and the services available on port 445.

This helped me understand how network enumeration provides information about a target system before further security testing.

STEP-7:- Enumerating the Target Using Enum4linux

I used Enum4linux from Kali Linux to gather additional information about the Windows domain environment.

The tool was used to inspect SMB-related information and identify details exposed by the target.

This helped me understand the importance of limiting unnecessary information disclosure.

STEP-8:- Exploring Metasploit Enumeration Modules

After completing the initial scans, I opened the Metasploit Framework.

I explored auxiliary scanning modules related to SMB and Kerberos enumeration.

I configured the required module options and ran them against the Windows Server lab machine.

This helped me understand how Metasploit can be used for reconnaissance and security assessment, not only exploitation.

STEP-9:- Performing LDAP Enumeration

Next, I used LDAPSearch to query the Active Directory environment.

I examined directory information and performed searches related to domain objects and user accounts.

This helped me understand how LDAP is used to organize and retrieve information from Active Directory.

STEP-10:- Checking Domain User Information

I performed additional LDAP queries and Kerberos-based username enumeration.

The objective was to identify user accounts present in the lab domain and understand how account information can be discovered.

This demonstrated why organizations should monitor authentication-related activity and protect directory information.

STEP-11:- Generating Active Directory Reports Using LDAPDomainDump

I used LDAPDomainDump to collect directory information from the lab environment.

The tool generated reports containing details about domain users, computers, groups, and other Active Directory objects.

I then opened the generated HTML reports to examine the information in a more readable format.

This helped me understand how directory enumeration results can be organized for analysis and reporting.

STEP-12:- Exploring Active Directory Using AD Explorer

Next, I used Microsoft Sysinternals AD Explorer to examine the Active Directory environment.

I worked with the connection settings and explored how the tool can be used to inspect directory objects and their properties.

This helped me become more familiar with Active Directory administration and analysis tools.

STEP-13:- Checking Windows Processes and Logged-In Users

I explored two Sysinternals utilities:

PsList: Used to view running processes and their related information.

PsLoggedOn: Used to identify logged-on user information.

These tools helped me understand how Windows process and session information can support system administration and security investigations.

STEP-14:- Exploring Controlled Security Testing with Metasploit

In the next part of the project, I worked with Metasploit's multi-handler and a test executable in the isolated lab.

I configured the testing environment and examined the behavior of a reverse connection during the exercise.

This helped me understand how remote sessions can be established and why endpoint monitoring and security controls are important.

STEP-15:- Examining System Information and Credential Exposure

After establishing the lab session, I explored system information available through the testing framework.

I examined operating system details, network configuration, and the exposure of credential-related information in the controlled environment.

This demonstrated the security risks that can arise when an attacker obtains elevated access to a Windows system.

STEP-16:- Analyzing the Test Executable Using VirusTotal

After the practical testing, I submitted the test executable to VirusTotal for security analysis.

I reviewed the detection results and the graphical analysis provided by the platform.

This helped me understand how security products identify suspicious files and how detection results can be interpreted during malware analysis.

Project Outcome

Through this project, I gained practical experience with Windows Active Directory and the tools used during network and domain security assessments.

I learned how to configure a domain controller, create domain accounts, discover network services, enumerate directory information, and inspect Windows system activities.

The controlled security testing exercises also helped me understand the importance of access controls, endpoint protection, credential security, and security monitoring.
