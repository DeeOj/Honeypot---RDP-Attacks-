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




