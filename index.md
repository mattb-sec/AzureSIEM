# Introduction

When it comes to cloud computing, one of the most ubiquitous names is Microsoft's cloud platform, Azure. In this lab, I set out to get a better understanding of Azure and how it is used to provide security solutions. To do so, I will be creating a virtual machine on Azure that has port 3389 open. 

For background, port 3389 serves the Remote Desktop Protocol or RDP which allows users to remote into a computer and control it from their own machine. While this is convenient for team members and those who are authorized to use the computer, this is also a glaring security vulnerability. All an attacker needs to breach a machine with RDP enabled is the machine's public IP address and its credentials. This vulnerability is so bad, that I have even heard that enabling RDP on a crucial machine is a fireable offense! This threat is only catalyzed if the user implemented a weak password for the machine. In our case, this is what we want because it gives us a chance to create a version of Azure's built-in Security Information and Event Management (SIEM) tool, Sentinel, and test it out.

There are two parts to this lab, but in this first part, the objective is to create an intentionally vulnerable virtual machine and use it to test the robustness and response efficacy of a SIEM tool I will configure.

# Setting Up Azure and the Virtual Machine

The entirety of this lab will be conducted using a trial version of Azure. To begin, I have to set up my account so I can start using Azure's services. I enter my information and am ready to get started.

Once I am taken to the homepage, it is now time to create my virtual machine. For this lab, I will be creating a virtual machine with a preset configuration.

- _Figure 1_: The "create" menu for Azure's virtual machine. As mentioned, I will be selecting the option to create an Azure VM with preset configuration.

<p align="center">
  <img width="384" height="384" src="assets/fig1.png">
</p>

The next step is to configure the recommended defaults for my VM. I will be going with the Production workload environment and the General Purpose (D-series) workload type. This is the standard, basic format of an Azure VM which is just what I need. This will then take me to the virtual machine creation portal.

Before I can start configuring my virtual machine, the first thing I need is a name for my resource group. This resource group will act as the container for all the things I will be creating. Being as creative as I am, I opted to go with the name, MattGroup. Therefore, my VM, SIEM, and threat intelligence system will all answer to MattGroup. 

The next step is to fill out the instance details. For the virtual machine name, I let my creativity shine once again and go for the name "MattsVM". Next is the region. Interestingly, I have found that Azure only offers its free services to regions where their cloud computing services are in low demand. There were no services available in the United States, so that makes me Australian now, mate.

