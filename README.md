# Log-Analytics-Workspace

# What is LAW?
- It is a central solution for all of your logs
- Companies will have machines that log everything
- Admins can use LAW to store the log data and admins can perform Kusto Query Language to perform queries on the data.

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/174463356-e8c7e88c-1225-4ab7-b7d0-7de9cc5c25be.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>


# Resources do not need to be in the same region as LAW. Note* data transfers not in the same region will be charged



# LAW - Connecting the Virtual Machines
- Virtual Machines > Select the VMs > Connect 
- An agent will be installed and it will send data to the LAW.
- On-Prem VM can also be sent to a LAW

# How to connect on-prem machines to LAW
- Download the Windows Agent on the LAW
- Right click on RDP file > edit >  Local Resources > More > Check Local Disk > Copy the agent onto the VM 
- Set up the monitoring agent < Connect the Agent to Azure Log Analytics > Enter the Workspace ID and Primary Key form the LAW
- The agent will be installed and the VM will be connected to the LAW.

# Log Analytics Queries
- KQL stands for Kusto Query Language
- KQL is the language that the Log Analytics Workspace understands
- System event logs are stored in the Event table

# Use Case: Connect two VM's and make 5 queries through the LAW


# LAW - How to send custom logs to LAW
- Access.log file wil tell admins information about all of the IP addresses/clients that are accessing the homepage of NGINX servers that installed on the LinuxVM
- Says admins want to stream this information to the LAW
- Copy the access.log onto your directory and go to LAW
- Custom Logs> Add custom log> select the access.log file from your local machine
- Add the collection path which is the path of where the access.log file is stored
- Ensure that the virtual machine is connected to the log analytics workspace (LAW) - It will install a LAW agent onto the vm.
- After connecting, ensure you still access the homepage so the log can record the data.

# LAW - Use Azure Resource Templates (ARM) to connect a VM to an LAW (169)
- 

# LAW - Alerts
- Alerts can be created based on the data collected on the log analytics workspace.
