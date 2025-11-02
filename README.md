# FUTURE_CS_01
Web Application Security Testing - Altoro Mutual vulnerability assessment. Identified XSS, weak credentials, and information disclosure vulnerabilities.


📋 About the Project
Security testing performed on the Altoro Mutual web application (demo.testfire.net) as part of the Future Interns program. The objective was to identify vulnerabilities following OWASP standards.

🎯 Methodology
🛠️ Tools: Web browser, manual testing, Sucuri SiteCheck

🎯 Target Application: http://demo.testfire.net

🔍 Approach: Manual testing and online scanning

🔧 Scanning Tools Used
🛡️ Sucuri SiteCheck Scanner
🌐 URL: https://sitecheck.sucuri.net/

✅ Result: No malware detected

📊 Status: Site is not blacklisted

⚙️ Technology: Apache-Coyote/1.1

🔓 Vulnerabilities Identified
1. 🚨 Reflected Cross-Site Scripting (XSS)
⚠️ Severity: High
📍 Location: Search field
📝 Description: Malicious script executed in search field

📸 Evidence:
![XSS Popup Executed](xss-popup-executed-successfully.png)

🔧 Reproduction:

bash

1. Access http://demo.testfire.net
2. In Search field, type: <script>alert('XSS')</script>
3. Observe script execution

🔓 Credentials Found:

👤 Username: jsmith

🔒 Password: demo1234

3. 📢 Information Disclosure
🚨 Severity: Critical
📍 Location: Login page source code
📝 Description: Comment in source code reveals internal administration procedure

📸 Evidence:

💻 Code Excerpt:

html
<!-- To get the latest admin login, please contact SiteOps at 415-555-6159 -->

🛡️ Recommendations
🚨 For XSS:
🔒 Implement input sanitization

🛡️ Use Content Security Policy (CSP)

✅ Validate and encode output data

🔑 For Default Credentials:
🗑️ Remove default credentials

💪 Implement strong password policy

🔐 Add multi-factor authentication

📢 For Information Disclosure:
🧹 Remove sensitive comments from source code

🔍 Review all code for exposed information

🚪 Implement proper access controls

📊 OWASP Top 10 Compliance Checklist


OWASP Top 10 2021
🔓 A01: Broken Access Control
🔐 A02: Cryptographic Failures
💉 A03: Injection
👤 A07: Identification & Authentication Failures
⚙️ A05: Security Misconfiguration

📋 Testing Evidence
📸 Additional Screenshots:
🌐 Initial Page: https://screenshots/1-initial-page.png

💉 SQL Injection Test: https://screenshots/2-sql-injection-attempt-failed.png

👤 Sign-in Page: https://screenshots/7-regular-user-signin.png

🚫 Admin Access Error: https://screenshots/9-admin-access-error.png

🔗 Login Page URL: https://screenshots/10-login-page-url.png


🚀 How to Reproduce
📥 Clone this repository

🌐 Access http://demo.testfire.net

📋 Follow steps described in each vulnerability section

📸 Check evidence in screenshots folder

✅ Verify findings using the same methodology
