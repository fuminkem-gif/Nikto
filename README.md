# 🔍 Vulnerability Scanning with Nikto

## 📌 Objective

The objective of this lab is to perform web server vulnerability scanning using Nikto, identify potential misconfigurations and vulnerabilities, and analyze the results in a controlled cybersecurity lab environment.

## 🛠 Tools Used

. Kali Linux

. Nikto Web Vulnerability Scanner

. Nano text editor

. Firefox Web Browser

## 🌐 Lab Environment

. Target IPs hosted within a private lab network

. Web services running on selected hosts

## 🧪 Step-by-Step Procedure

1️⃣ Create a Target IP List

. Create a file and add the IP addresses to be scanned:

nano ip_list.txt

. Add the following IP addresses inside the file:

10.6.6.14
10.6.6.1
10.6.6.13
10.6.6.23
172.17.0.2

. Save and exit (CTRL + X, then Y, then ENTER).

2️⃣ Run Nikto Scan on Multiple Targets

Scan all IP addresses listed in the file:

nikto -h ip_list.txt

3️⃣ Run a Specific Scan and Generate an HTML Report

Perform a focused scan and save the results as an HTML file:

nikto -h 172.17.0.2 -o scan_results.html

4️⃣ Locate and Open the Scan Results

A. Locate the output file:

locate scan_results.html

B. Open the report in a browser:

Open Firefox and load the HTML report.

📸 Screenshot example: Nikto HTML report displayed in browser.

## 🔍 Key Findings and Observations

. Outdated server software detected

. Insecure or missing HTTP security headers

. Default/accessible files and directories

. References to known vulnerabilities (CVEs)

. Indicators of weak server hardening

## 📊 Conclusion

Nikto proved effective in detecting multiple web server weaknesses that could be exploited by attackers.
Regular vulnerability scanning is essential for maintaining secure web services and ensuring proactive defense.
