
![InspectJS ](./InspectJS.jpeg)

# 🔍 inspectJS

**Advanced JavaScript File Discovery and Analysis Tool**

![Python](https://img.shields.io/badge/Python-3.6+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Windows%20%7C%20macOS-lightgrey.svg)

`inspectJS` is a powerful security tool designed to automatically discover and analyze JavaScript files in web applications. It scans for sensitive information, API endpoints, and potential security vulnerabilities exposed in client-side JavaScript code.

## ✨ Features

- **🔍 Automated JS Discovery** - Automatically finds JavaScript files from websites
- **🔐 Sensitive Data Detection** - Identifies API keys, tokens, passwords, and secrets
- **🌐 Endpoint Analysis** - Discovers API endpoints and HTTP requests
- **🎯 Critical Risk Assessment** - Color-coded risk evaluation (HIGH/MEDIUM/LOW)
- **⚡ Multi-threaded Scanning** - Fast parallel analysis of multiple files
- **📊 Comprehensive Reporting** - Detailed reports with source file attribution
- **🔒 SSL Support** - Configurable SSL verification for testing environments

## 🚀 Installation

### Prerequisites
- Python 3.6 or higher
- pip package manager

### Quick Install
```bash
# Clone the repository
git clone https://github.com/mitsec/inspectjs.git
cd inspectjs

# Install dependencies
pip install -r requirements.txt

# Run the tool
python inspectjs.py -u https://example.com


📖 Usage

python inspectjs.py -u https://target-website.com

Advanced Options

# Save results to file
python inspectjs.py -u https://target.com -o report.txt

# Use multiple threads for faster scanning
python inspectjs.py -u https://target.com -t 10

# Enable SSL verification
python inspectjs.py -u https://target.com --verify-ssl

# Set discovery depth
python inspectjs.py -u https://target.com -d 2

Command Line Arguments



Argument	Description	Default
-u, --url	Target website URL (required)	-
-o, --output	Save results to file	-
-t, --threads	Number of concurrent threads	5
-d, --depth	Discovery depth level	1
--verify-ssl	Enable SSL certificate verification	False

🎯 What It Detects
🔴 Critical Secrets
API Keys - Various API key patterns and secrets

JWT Tokens - JSON Web Tokens in code

Passwords - Hardcoded passwords and credentials

AWS Keys - AWS access and secret keys

Database URLs - Connection strings for databases

🌐 API & Endpoints
REST API Endpoints - /api/, /v1/, /graphql etc.

HTTP Requests - Fetch, Axios, XHR, jQuery calls

Authentication Endpoints - Login, register, auth routes

Admin Interfaces - Admin panels and management endpoints

📧 Other Information
Email Addresses - Found in JavaScript code

IP Addresses - Hardcoded IP addresses

Custom Endpoints - Application-specific API routes

📊 Sample Output


inspectJS powered by mitsec
    (x.com/ynsmroztas)

[*] Target Site: https://example.com
[*] Threads: 5
[*] SSL Verification: Disabled

──────────────────────────────────────────────────
[*] Discovering JS files...
[+] 8 JS files discovered
[*] Analyzing JS files...
[>] Downloading: https://example.com/app.js
[+] Analyzing: https://example.com/app.js (15,230 chars)

══════════════════════════════════════════════════
                  COMPREHENSIVE ANALYSIS REPORT
══════════════════════════════════════════════════
🔗 Target Site: https://example.com
📅 Scan Date: 2024-01-15 14:30:22
📁 Discovered JS Files: 8
──────────────────────────────────────────────────

🔴 CRITICAL API_KEYS FOUND (3):
   1. api_key_123456789
      📎 Source: https://example.com/app.js
      📝 Context: ...const API_KEY = "api_key_123456789";...

🚨 CRITICAL ENDPOINT REQUESTS (2):
   1. POST /api/v1/login
      📎 Source: https://example.com/app.js
      🔍 Type: login
      📋 Query Parameters: username, password

══════════════════════════════════════════════════
                    SCAN SUMMARY
══════════════════════════════════════════════════
   📁 Discovered JS Files: 8
   🔴 Critical Secrets: 3
   🌐 HTTP Requests: 5
   🚨 Critical Endpoints: 2
   📊 Total Findings: 15
   ⚡ SECURITY RISK: HIGH
══════════════════════════════════════════════════
🛡️ Use Cases


Security Audits
Penetration Testing - Identify exposed secrets in client-side code

Bug Bounty Hunting - Find sensitive information disclosure

Security Assessments - Evaluate web application security posture

Development
Code Review - Automatically detect hardcoded secrets

CI/CD Integration - Scan during development pipelines

Compliance Checks - Ensure no sensitive data in frontend code

⚠️ Legal & Ethical Use
Important: This tool is designed for:

Security research and education

Authorized penetration testing

Bug bounty programs with permission

Security assessments of your own applications

Never use this tool against websites without explicit permission. Unauthorized testing may violate laws and terms of service.

👨‍💻 Author
mitsec

Twitter: @ynsmroztas

GitHub: github.com/ynsmroztas

