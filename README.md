# PROJECT: HONEYPOT

## INTRODUCTION
This project involves setting up a Windows 11 Pro virtual machine on Azure as a honeypot to monitor and analyze Remote Desktop Protocol (RDP) attacks.
By configuring a comprehensive logging and monitoring solution using Azure's Log Analytics Workspace and Sentinel, this project aims to map and visualize global RDP attack data. This setup not only provides valuable insights into the sources and methods of attacks but also helps me gain practical experience in deploying and managing cybersecurity defense strategies.

## OBJECTIVE
The primary objective of this project is to create a robust environment for detecting and analyzing RDP brute force attacks on a honeypot VM deployed in Azure.

## LINKS TO RESOURCES
- [VMWare Workstation Pro](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html)
- [Azure Account](https://azure.microsoft.com/en-us/free/)
- [Powershell Script](https://github.com/joshmadakor1/Sentinel-Lab/blob/main/Custom_Security_Log_Exporter.ps1)
   
## OVERVIEW OF TASK

- Deploy a Windows 11 Pro virtual machine on Azure and configure it with an inbound rule allowing all traffic, simulating an attractive target for attackers.
- Set up a Log Analytics Workspace to ingest custom logs that include geographic information such as latitude, longitude, state/province, and country.
- Utilize a custom PowerShell script to extract metadata from the Windows Event Viewer and forward it to a third-party API for geolocation data derivation.
- Configure Custom Fields in the Log Analytics Workspace to process and map the geo data in Azure Sentinel.
- Design and implement an Azure Sentinel workbook to visually display global RDP attack data on a world map, categorized by physical location and the magnitude of attacks.

## TASK BREAKDOWN

 #### CREATIING VIRTUAL MACHINE ON AZURE
 - Basics
<p align="center">
<img src="https://imgur.com/3og0yFj.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/ZZ1vFc1.jpg" height="90%", width="90%">
</p>

- Networking
<p align="center">
<img src="https://imgur.com/lDWBKcf.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/TsT1SSm.jpg" height="90%", width="90%">
</p>

- Delete Default Rule
<p align="center">
<img src="https://imgur.com/jedyJZv.jpg" height="90%", width="90%">
</p>

- Create new and add
<p align="center">
<img src="https://imgur.com/tNw5AWT.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/eb5Ixsu.jpg" height="90%", width="90%">
</p>

- Review Settings and Create.
<p align="center">
<img src="https://imgur.com/yijIs22.jpg" height="90%", width="90%">
</p>

#### LOG ANALYTICS WORKSPACE
Its purpose is to ingest the windows events logs.

- Create Log Analytics Workspace
<p align="center">
<img src="https://imgur.com/Lgh50Rw.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/dxDdpeH.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>


<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

<p align="center">
<img src=".jpg" height="90%", width="90%">
</p>

## CONCLUSION
By configuring a detailed logging and monitoring setup using Log Analytics Workspace and Azure Sentinel, valuable insights into global attack patterns were obtained. 
The project highlighted the geographical distribution and intensity of attacks, enhancing my practical skills and emphasizing the importance of proactive cybersecurity measures.




