Azure Entra ID Security Assessment - Phishing Attack Simulation

⚠️ DISCLAIMER: This project is for educational and authorized security testing purposes only. Unauthorized access to computer systems is illegal. Always obtain proper authorization before conducting security assessments.

🎯 Project Overview
A comprehensive security assessment demonstrating advanced phishing techniques to bypass Multi-Factor Authentication (MFA) in Microsoft Entra ID (formerly Azure AD) environments. This project showcases adversary simulation tactics using Evilginx2 for token capture and session hijacking.
Key Achievements

✅ Successfully bypassed MFA using token-based session hijacking
✅ Performed external reconnaissance on Azure AD tenant
✅ Captured user credentials and authentication tokens
✅ Demonstrated real-world attack vectors against cloud identity providers

🏗️ Architecture

Attacker Infrastructure → Evilginx2 Phishing Proxy → Microsoft Entra ID → Target User →  Token Capture & Session Hijacking

🛠️ Tools & Technologies

Microsoft Azure - Cloud infrastructure
Microsoft Entra ID - Identity and access management
PowerShell - Automation and user provisioning
AADInternals - Azure AD reconnaissance
Evilginx2 - Phishing framework with MFA bypass
DigitalOcean - VPS hosting for attack infrastructure
Namecheap - Domain registration

📁 Repository Structure

azure-entra-phishing-simulation/
├── README.md
├── DISCLAIMER.md
├── docs/
│   ├── setup-guide.md
│   ├── attack-flow.md
│   ├── mitigation-strategies.md
│   └── screenshots/
│       ├── evilginx-dashboard.png
│       ├── token-capture.png
│       └── successful-bypass.png
├── scripts/
│   ├── azure-setup/
│   │   ├── Create_Microsoft_Entra_ID_Users.ps1
│   │   └── README.md
│   └── reconnaissance/
│       ├── AADInternals_Commands.ps1
│       ├── users.txt
│       └── README.md
├── evilginx/
│   ├── setup-instructions.md
│   ├── phishlet-config/
│   └── lure-generation.md
├── phishing-templates/
│   ├── email-templates/
│   │   └── password-reset-email.md
│   └── best-practices.md
└── defense/
    ├── detection-rules.md
    ├── prevention-strategies.md
    └── incident-response.md
Cookie-Editor - Session token manipulation

🚀 Quick Start
Prerequisites

Azure subscription with Global Administrator privileges
PowerShell 7+ with Az module
Linux VPS (DigitalOcean recommended)
Registered domain name
Basic understanding of Azure AD and authentication protocols
                
