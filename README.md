# Splunk Log Analysis on Kali Linux
Splunk Log Analysis on Kali Linux

## Description
The following will show the steps and screenshots I took to complete the project:

## Languages
- [Python](https://www.python.org/)

## Resources
- [Splunk Documentation](https://docs.splunk.com/)
- [Kali Linux Documentation](https://www.kali.org/docs/)
- [Bureau of Transportation Statistics](https://www.transtats.bts.gov/)

## Utilities Used
- [Virtual Box](https://www.virtualbox.org/)
- [Kali Linux](https://www.kali.org/get-kali/#kali-platforms)
- [Splunk](https://www.splunk.com/)

## Explanation

This project involved setting up Splunk on Kali Linux to analyze logs from the Bureau of Transportation Statistics. 

## Steps

<p align="center">
Open Kali Linux
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Install the free version of Splunk from Splunk's official website 
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Install the .deb package using the following command:
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Start Splunk
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Download Buearu of Transportation Statistics and save at /home/kali/splunk_logs
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Open your web browser and navigate to http://localhost:8000 to access the Splunk web interface
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Log in with the credentials you created during installation.
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Go to Settings > Data Inputs
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Click on Files & Directories 
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Click on New Local File & Directory
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Add the directory where you placed your log files (/home/kali/splunk_logs) and select Next
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Set Source Type (I left default)
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Configure input settings (I left them default) and click Review
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Select Submit
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Verify file input has been created successfully and select Start Searching
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Verify data is showing
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Query 1: Count Unique Carriers (spl query) 
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
Query 2: Filter by Region and Count Events (spl query) 
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>
