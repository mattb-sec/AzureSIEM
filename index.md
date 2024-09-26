# Introduction

When it comes to cloud computing, one of the most ubiquitous names is Microsoft's cloud platform, Azure. In this lab, I set out to get a better understanding of Azure and how it is used to provide security solutions. To do so, I will be creating a virtual machine on Azure that has port 3389 open. 

For background, port 3389 serves the Remote Desktop Protocol or RDP which allows users to remote into a computer and control it from their own machine. While this is convenient for team members and those who are authorized to use the computer, this is also a glaring security vulnerability. All an attacker needs to breach a machine with RDP enabled is the machine's public IP address and its credentials. This threat is only catalyzed if the user implemented a weak password for the machine. In our case, this is what we want because it gives us a chance to create a version of Azure's built-in Security Information and Event Management (SIEM) tool, Sentinel, and test it out.

The objective here is top create an intentionally vulnerable virtual machine and use it to test the robustness and response efficacy of a SIEM tool I will configure.

# Setting Up Azure

