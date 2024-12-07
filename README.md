# Log Analysis Script

## Project Overview

This Python-based log analysis script processes and analyzes log files to extract key information, such as:

- **Request counts per IP address**: Identifies the frequency of requests made by each IP address.
- **Most frequently accessed endpoint**: Finds which endpoint is accessed the most from the logs.
- **Suspicious activity detection**: Detects potential brute force login attempts based on failed login attempts.

The results of the analysis are displayed in the terminal and saved into a CSV file for easy reference.

## Core Requirements

### 1. Count Requests per IP Address
- Parse the log file to extract IP addresses.
- Count how many requests each IP address has made.
- Sort and display the results in descending order of request counts.

### 2. Identify Most Frequently Accessed Endpoint
- Extract the endpoints (e.g., URLs or resource paths) from the log file.
- Identify which endpoint was accessed the most.
- Display the endpoint name and its access count.

### 3. Detect Suspicious Activity
- Identify failed login attempts (status code `401` or failure message like "Invalid credentials").
- Flag IP addresses with failed login attempts above a configurable threshold (default: 10 attempts).
- Display the flagged IP addresses and their failed login counts.

### 4. Output Results
- Display the results in a clear, organized format in the terminal.
- Save the results to a CSV file named `log_analysis_results.csv`.

## Project Structure
log_analysis_script/
│

├── sample.log                # Sample log file (input)

├── log_analysis_results.csv  # CSV output file (results)

├── log_analysis.py           # Python script for log analysis

├── README.md                 # This file (documentation)

└── requirements.txt          # Python dependencies (if needed)



## Technologies Used
- Python 3.x
- Regular Expressions (Regex)
- Collections (Counter)
- CSV Module
- Jupyter Notebook (for execution)

# How to Use
### Step 1: Open the Jupyter Notebook
The script is designed to be executed in a Jupyter Notebook environment. Begin by opening Jupyter Notebook on your machine and creating a new notebook or using the existing notebook where you want to run the log analysis script.
### Step 2: Ensure the Log File is Available
Make sure the sample.log file is located at the correct path on your system. If the log file is not in the default location, update the script to point to the correct file path where the sample.log is stored.
### Step 3: Import Required Libraries
Before executing the script, ensure that the necessary Python libraries are available in your environment. The script uses Python's built-in libraries for regular expressions, file handling, and data counting. These libraries are typically included in standard Python distributions, so no additional installation should be required.
### Step 4: Read the Log File
The script contains a function that reads the log file and processes it line by line. This step loads the content of the log file into the script, enabling further analysis of the data.
### Step 5: Count Requests per IP Address
Next, the script processes the log file to count the number of requests made by each unique IP address. The results will be displayed in descending order, showing the IP addresses and the number of requests made from each one.
### Step 6: Identify the Most Frequently Accessed Endpoint
The script also identifies the most frequently accessed endpoint or URL path in the log file. It counts how many times each endpoint has been accessed and displays the endpoint with the highest number of accesses.
### Step 7: Detect Suspicious Activity
The script checks for potential suspicious activity by looking for failed login attempts in the log file. Specifically, it searches for log entries with an HTTP status code of 401, which indicates unauthorized access attempts. IP addresses with a higher number of failed login attempts are flagged as suspicious. By default, the script flags any IP address with more than 10 failed login attempts, but this threshold can be adjusted based on your needs.
### Step 8: Save the Results to a CSV File
Once the analysis is complete, the results are saved to a CSV file. This file includes structured data, such as the number of requests made by each IP address, the most frequently accessed endpoint, and the details of suspicious activity (i.e., IP addresses with excessive failed login attempts). You can specify the file name and location where the CSV file should be saved, making it easy to review or share the analysis.
### Step 9: Check the Output
After running the script, you will see the analysis results printed to the terminal, showing the IP addresses, request counts, most accessed endpoint, and suspicious IP addresses. Additionally, the results will be saved in a CSV file in the directory you specified. You can open this file with any spreadsheet application like Microsoft Excel or Google Sheets for further review.


# THANK YOU
















