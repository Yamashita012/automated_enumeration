# Automated Pentesting Script README

## Overview

This Bash script is designed to automate the initial phase of penetration testing, focusing on information gathering and vulnerability assessment. The script performs the following tasks:

1. Conducts an initial Nmap scan on the specified target.
2. Extracts open ports from the Nmap results and saves them to a file.
3. Conducts more detailed Nmap scans on individual ports for service enumeration.
4. Identifies available services and extracts them to a separate file.
5. Utilizes Searchsploit to search for known vulnerabilities related to identified services.
6. Performs directory busting using Gobuster on common web ports (80, 443, 8080).

## Prerequisites

- This script assumes that Nmap, Gobuster, and Searchsploit are installed on the system.

## Usage

1. Make the script executable:

   ```bash
   chmod +x automated_pentest_script.sh
   ```

2. Execute the script with the target domain or IP address:

   ```bash
   ./automated_pentest_script.sh
   ```

## Output

- `nmap-results_2.txt`: Detailed Nmap scan results for individual ports.
- `avail_services.txt`: List of available services on open ports.
- `services.txt`: Extracted services from the Nmap results.
- `searchsploit-results.txt`: Results of Searchsploit for identified services.
- `dir_busting_results.txt`: Gobuster results for directory busting.

## Notes

- The script focuses on common web ports (80, 443, 8080) for Gobuster directory busting.
- Some services may be labeled as "unknown," and Searchsploit won't be applied to them.
- Ensure that the script is run with appropriate permissions and dependencies are installed.

**Disclaimer**: This script is intended for educational and ethical use only. Ensure you have proper authorization before conducting penetration testing on any system. The script author is not responsible for any misuse or damage caused by the script.
