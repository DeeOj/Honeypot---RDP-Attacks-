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
- [API key](https://app.ipgeolocation.io/login)
   
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

#### ENABLE GATHERING OF VM LOGS IN SECURITY CENTER

- Open Defender for Cloud
<p align="center">
<img src="https://imgur.com/6EY1NAf.jpg" height="90%", width="90%">
</p>

- Environment Settings
<p align="center">
<img src="https://imgur.com/xYW9ANr.jpg" height="90%", width="90%">
</p>

- Turnoff SQL Servers
<p align="center">
<img src="https://imgur.com/c7ZQlC3.jpg" height="90%", width="90%">
</p>

- Set Data COllections to All events
<p align="center">
<img src="https://imgur.com/A2Knnz6.jpg" height="90%", width="90%">
</p>

#### CONNECTING LOG ANALYTICS TO VIRTUAL MACHINE

- Select the workspace and head to machine to connect.

<p align="center">
<img src="https://imgur.com/dm6czBq.jpg" height="90%", width="90%">
</p>

#### MICROSOFT SENTINEL SETUP

- Create Microsoft Sentinel
<p align="center">
<img src="https://imgur.com/BJ98DKH.jpg" height="90%", width="90%">
</p>

- Select the log analytics workspace and add it.
<p align="center">
<img src="https://imgur.com/KKLOg2O.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/D0KGU6V.jpg" height="90%", width="90%">
</p>

#### LOGIN INTO THE VM WITH REMOTE DESKTOP

- Copy the IP address of the VM created.
  
<p align="center">
<img src="https://imgur.com/6yUgFpE.jpg" height="90%", width="90%">
</p>

- Remote Desktop on Local Computer
  
<p align="center">
<img src="https://imgur.com/3IhHZ3y.jpg" height="90%", width="90%">
</p>

- Sign in as "another user"
  
<p align="center">
<img src="https://imgur.com/XfCfsn0.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/1aQu4L5.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/sgaY9Xc.jpg" height="90%", width="90%">
</p>

- Observing Event Viewer 
  
<p align="center">
<img src="https://imgur.com/qrHQncY.jpg" height="90%", width="90%">
</p>

- Pinging the VM from my computer. <br/>
  Request Timed out, therefore its firewall will be turned off to make it susceptible to ICMP echo requests, making it discoverable on the internet.
  
<p align="center">
<img src="https://imgur.com/RoMajD7.jpg" height="90%", width="90%">
</p>

- Turning off Firewall
<p align="center">
<img src="https://imgur.com/MlUsG2G.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/UqsxJO5.jpg" height="90%", width="90%">
</p>

- Virtual machine is now responsive to pings.
  
<p align="center">
<img src="https://imgur.com/33by0iS.jpg" height="90%", width="90%">
</p>

#### DOWNLOAD POWERSHELL SCRIPT ON VM.
This will look through the event log viewed earlier, grab the events of people who failed to login into the VM and gets the geodata from them, subsequently creating a new log file.

- Link to script provided earlier.
<p align="center">
<img src="https://imgur.com/HHCjWn0.jpg" height="90%", width="90%">
</p>

- Open script with Powershell ISE
<p align="center">
<img src="https://imgur.com/5BcHNPs.jpg" height="90%", width="90%">
</p>

- Register and Get an API key
  
<p align="center">
<img src="https://imgur.com/vGUmUsm.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/vGUmUsm.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/rQuwnoz.jpg" height="90%", width="90%">
</p>

- Replace Key in the Script
<p align="center">
<img src="https://imgur.com/Wu0NPgv.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/olqFDuQ.jpg" height="90%", width="90%">
</p>

- Run the script

<p align="center">
<img src="https://imgur.com/mgIOBHg.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/mhlCdm9.jpg" height="90%", width="90%">
</p>

- A look at entries at this stage
  
<p align="center">
<img src="https://imgur.com/bnjPZpU.jpg" height="90%", width="90%">
</p>

#### CREATE CUSTOM LOG IN THE LOG ANALYTICS WORKSPACE 

<p align="center">
<img src="https://imgur.com/7Q5AlDN.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/uOuBYcQ.jpg" height="90%", width="90%">
</p>

- Copy the contents of the text file from VM and safe in a text file on the local computer. Then upload the file.
  
<p align="center">
<img src="https://imgur.com/OqCkndh.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/yOjJnDl.jpg" height="90%", width="90%">
</p>

- Specify the path and the name of the file on the VM
  
<p align="center">
<img src="https://imgur.com/GbGsWb7.jpg" height="90%", width="90%">
</p>

- Name it.
  
<p align="center">
<img src="https://imgur.com/39Fmor1.jpg" height="90%", width="90%">
</p>

- Review and Create
  
<p align="center">
<img src="https://imgur.com/Kkj2fIf.jpg" height="90%", width="90%">
</p>

- A look at the virtual machine's Event Viewer from Log analytics workspace.
  
<p align="center">
<img src="https://imgur.com/C9683N0.jpg" height="90%", width="90%">
</p>

- And now, some entries from the customed logs.

<p align="center">
<img src="https://imgur.com/2IKFFol.jpg" height="90%", width="90%">
</p>

- Extracting fields from raw custom log data. <br/>
  Utilized a querry log at this juncture.
  
<p align="center">
<img src="https://imgur.com/VTPdZuD.jpg" height="90%", width="90%">
</p>

#### MAP SETUP IN SENTINEL

- Create a workbook.
  
<p align="center">
<img src="https://imgur.com/Fh7Dt8Q.jpg" height="90%", width="90%">
</p>

- Remove these.
  
<p align="center">
<img src="https://imgur.com/r78R3KL.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/SVZc9YG.jpg" height="90%", width="90%">
</p>

- Add Querry
  
<p align="center">
<img src="https://imgur.com/l4liKUN.jpg" height="90%", width="90%">
</p>

- Insert querry
  
<p align="center">
<img src="https://imgur.com/boJhF4n.jpg" height="90%", width="90%">
</p>

- Set Visualization Type to be "Map" and save.

<p align="center">
<img src="https://imgur.com/CR4KyDt.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/x5CSZyJ.jpg" height="90%", width="90%">
</p>
<br></br>

## <p align="center"> WORLD MAP OF INCOMING RDP ATTACKS 🔥</p> 

<p align="center">
<img src="https://imgur.com/huEvfWT.jpg" height="90%", width="90%">
</p>

## CONCLUSION
By configuring a detailed logging and monitoring setup using Log Analytics Workspace and Azure Sentinel, valuable insights into global attack patterns were obtained. 
The project highlighted the geographical distribution and intensity of attacks, enhancing my practical skills and emphasizing the importance of proactive cybersecurity measures.




