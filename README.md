# Splunk Log Analysis on Kali Linux
Splunk Log Analysis on Kali Linux

## Description
The following will show the steps and screenshots I took to complete the project and the below queries
```python
source="/home/kali/splunk_logs/sample_logs.csv" | stats dc(UNIQUE_CARRIER) AS UniqueCarrierCount
```
```python
source="/home/kali/splunk_logs/sample_logs.csv" REGION="your_region_value" | stats count AS EventCount
```
```python
source="/home/kali/splunk_logs/sample_logs.csv" | timechart span=1h count AS EventCount
```
```python
source="/home/kali/splunk_logs/sample_logs.csv" | stats avg(ARR_DELAY) AS AverageDelay BY UNIQUE_CARRIER
```
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
1. Open Kali Linux
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/af20b2d9-faa5-4bc3-84e6-a3d43969e914" alt="Open Kali Linux">
</p>

<p align="center">
2. Install the free version of Splunk from Splunk's official website 
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/60e8229b-c696-4246-9dad-1e144c609f1b" alt="Install the free version of Splunk from Splunk's official website">
</p>

<p align="center">
3. Install the .deb package using the following command::<br>
</p>

```python
sudo dpkg -i splunk-<version>-<build>.deb
```
<p align="center">
<img src="https://github.com/user-attachments/assets/c7d4210e-251c-41fc-b6cc-29987ca0115a" alt="Install the .deb package using the following command:">
</p>

<p align="center">
4. Start Splunk:<br>
</p>

```python
sudo /opt/splunk/bin/splunk start
```
<p align="center">
<img src="https://github.com/user-attachments/assets/c7d4210e-251c-41fc-b6cc-29987ca0115a" alt="Start Splunk">
</p>

<p align="center">
5. Download Buearu of Transportation Statistics and save at /home/kali/splunk_logs
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/fb553442-68cd-4544-975f-09344448a40a" alt="Download Buearu of Transportation Statistics and save at /home/kali/splunk_logs">
</p>

<p align="center">
6. Open your web browser and navigate to http://localhost:8000 to access the Splunk web interface
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/9febbf4e-d3ef-4d75-a7d5-d66d10fb76f4" alt="Open your web browser and navigate to http://localhost:8000 to access the Splunk web interface">
</p>

<p align="center">
7. Log in with the credentials you created during installation
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/7fa4385d-9212-4a89-bf30-f5d2ffcb31b1" alt="Log in with the credentials you created during installation">
</p>

<p align="center">
8. Go to Settings > Data Inputs
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/9e4220c6-1598-4c83-a175-9a3b2747c1ff" alt="Go to Settings > Data Inputs">
</p>

<p align="center">
9. Click on Files & Directories 
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/ba606126-ecba-49fb-9555-8fdacab87f35" alt="Click on Files & Directories ">
</p>

<p align="center">
10. Click on New Local File & Directory
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/e6ce5f8e-3fb8-4257-81ab-dae457369377" alt="Click on New Local File & Directory">
</p>

<p align="center">
11. Add the directory where you placed your log files (/home/kali/splunk_logs) and select Next
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/460b68c2-5812-4f07-8175-9cb7615de29a" alt="Add the directory where you placed your log files (/home/kali/splunk_logs) and select Next">
</p>

<p align="center">
12. Set Source Type (I left default)
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/2a8162dd-06d8-4bc4-a524-125c2d49fa5c" alt="Set Source Type (I left default)">
</p>

<p align="center">
13. Configure input settings (I left them default) and click Review
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/4fb6a163-3f47-4d87-a87a-1b1f493e5b9c" alt="Configure input settings (I left them default) and click Review">
</p>

<p align="center">
14. Select Submit
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/0853171f-238f-4ac8-bd1a-f73602941165" alt="Select Submit">
</p>

<p align="center">
15. Verify file input has been created successfully and select Start Searching
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/64c5d6ff-2291-4bc1-b037-67ad73173f1a" alt="Verify file input has been created successfully and select Start Searching">
</p>

<p align="center">
16. Verify data is showing
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/814faed1-ee1b-46e9-9dbb-3b3a87560da2" alt="Verify data is showing">
</p>

<p align="center">
17. Query 1: Count Unique Carriers (spl query) 
</p>

```python
source="/home/kali/splunk_logs/sample_logs.csv" | stats dc(UNIQUE_CARRIER) AS UniqueCarrierCount
```
<p align="center">
<img src="https://github.com/user-attachments/assets/238df0a7-6782-47ba-819d-14b82d50566c" alt="Query 1: Count Unique Carriers (spl query) ">
</p>

<p align="center">
18. Query 2: Filter by Region and Count Events (spl query) 
</p>

```python
source="/home/kali/splunk_logs/sample_logs.csv" REGION="your_region_value" | stats count AS EventCount
```
<p align="center">
<img src="https://github.com/user-attachments/assets/a8398850-b601-4337-bb7a-b87295398f16" alt="18. Query 2: Filter by Region and Count Events (spl query) ">
</p>

<p align="center">
18. Query 3: Time-based Analysis
</p>

```python
source="/home/kali/splunk_logs/sample_logs.csv" | timechart span=1h count AS EventCount
```

<p align="center">
18. Average Delay by Carrier
</p>

```python
source="/home/kali/splunk_logs/sample_logs.csv" | stats avg(ARR_DELAY) AS AverageDelay BY UNIQUE_CARRIER
```
