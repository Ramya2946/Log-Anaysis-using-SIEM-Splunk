### Ramya Ajay
### CB.EN.P2CYS22004
### 1. Understand the architecture of Splunk and the installation process. Setup collector and forwarder,then ensure the logs are accumulated in Splunk. Familiarize yourself with the dashboard fields.

Splunk Architecture

- **Data collection**: Splunk can collect data from a variety of sources such as servers, network devices, applications, sensors, and more. It uses agents and connectors to collect data and send it to the Splunk server.
- **Data indexing**: The collected data is indexed and stored in Splunk's proprietary format, which is optimized for searching and querying. The indexing process involves breaking the data into events, extracting fields from the events, and creating an index for each field.
- **Search and analysis**: Splunk provides a powerful search and analysis engine that allows users to query the indexed data using a search language called SPL (Splunk Processing Language). Users can create ad-hoc searches or save them as dashboards and alerts for later use.
- **Visualization**: Splunk provides a range of visualization options such as charts, graphs, and tables to help users understand and analyze their data. Users can customize the visualization options to suit their needs.
- **Deployment options**: Splunk can be deployed on-premises, in the cloud, or as a hybrid deployment. Splunk Enterprise can be deployed as a single instance or as a distributed environment with multiple indexers, search heads, and forwarders.

#### Installing Splunk Forwarder in Kali
![Screenshot (503)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/bab84507-df07-4ae6-86cb-3a39d428262c)
![Screenshot (504)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/5381175f-c518-4bfa-8188-5cc425875bd9)

#### Splunk Forwarding Configuration
![Screenshot (495)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/3a8092de-8188-4ca2-85c6-fa0fe1e1be18)

- Configure the splunk forwarder with the splunk enterprise and send logs.
![VirtualBox_kali_14_05_2023_13_40_29](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/23a55f3e-3ba4-4862-86ec-0e020b2b159b)
![VirtualBox_kali_15_05_2023_13_26_27](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/324569a3-119c-486a-9cf5-185fd235e951)
![Screenshot (505)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/cc874f9c-2127-4bc9-aa41-cf42557c467e)

### 2. Run Splunk >> Forwarder can be in the same system or another system (user’s convenience) >>Make sure the logs are indexing in the Splunk enterprise.
### • Run any network and port scanning commands from the host to the target machine. Run at least 5 to 8 commands. (If required, any tools can also be used).
### • Use the search section in Splunk to analyze the firewall logs to find the log of the above process and the exact IP from where the scan was performed. HINT: Use the “stats” command.
### • Analyze the log file and create an alert for any further similar activities.
- Now we perform a nmap-scan and save it as a log file ,then send the nmap logs
![VirtualBox_kali_14_05_2023_14_00_21](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/65b20e1f-55c1-4cd9-9bf4-f4f1a67cbc56)

- Use command 'scan' in splunk to find the logs
![Screenshot (498)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/a1ac2e7a-d460-4ac1-8d9a-70ebfd8dc00c)


### 3. Run Splunk >> Forwarder can be in the same system or another system(user’s convenience) >>Make sure the logs are indexing in the Splunk enterprise.
### • Perform any communication using unencrypted traffic.
### • Use the Splunk search section to check the firewall logs to analyzewhich application usesunencrypted data.
### • Analyze the log file and create an alert for any further similar activities.
- Visit a http site
![VirtualBox_kali_15_05_2023_12_44_20](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/90997837-b368-435c-a8f8-1bd85b522771)

- Now we add the location of the default logs of kali i.e /var/log into splunk
![VirtualBox_kali_14_05_2023_14_05_59](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/ffb8c931-802a-4799-9e07-06a4a427b35a)

- The result in splunk
![Screenshot (499)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/b342a083-8690-4d38-a059-1ae794998eae)
![Screenshot (500)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/0bb8652f-81d4-440d-9fcc-ceb63bdc2b53)


### 4. Run Splunk >> Forwarder can be in the same system or another system (user’s convenience) >>Make sure the logs are indexing in the Splunk enterprise. Download malware from this site https://dasmalwerk.eu/ . CAUTION: THEY ARE REAL MALWARE. USE IN AN ISOLATED ENVIRONMENT. >> Run the malware in your target system.
### • After running your malware file, either it is stopped by your antivirus or not using the search section, find the antivirus log for the past 1 hour.
### • Run different malware files again in the same target system and use the search section  to find the time range between the previous and current malware file execution. HINT: Use the “stats” command.
### • Then save that search as an alert to show a notification when the same type happens again.

### 5. Run Splunk >> Forwarder can be in the same system or another system (user’s convenience)  >>Make sure the logs are indexing in the Splunk enterprise.
### • Logout of the target system and perform multiple failed attempts. Then use the search section to filter out the failed attempt logs. Hint: Use the “stats” command.
### • Analyze the log file and create an alert for any further similar activities.

- Perform multiple login failed attempts.
![VirtualBox_kali_15_05_2023_12_48_12](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/05ed58de-acde-4687-9cfa-72be49bf2e80)

- Go to Splunk Enterprise and enter the host name

![Screenshot (501)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/d60403e4-cbb6-4e17-8ebe-2ea2b3ea3051)

- The result in splunk Enterprise
 
![Screenshot (502)](https://github.com/Ramya2946/Log-Anaysis-using-SIEM-Splunk/assets/123251017/d09266b6-4f47-4150-aeca-e7b2fe2a1d61)








