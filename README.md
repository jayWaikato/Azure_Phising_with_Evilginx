# Azure Entra ID Security Assessment - Phishing Attack Simulation

> **⚠️ DISCLAIMER**: This project is for educational and authorized security testing purposes only. Unauthorized access to computer systems is illegal. Always obtain proper authorization before conducting security assessments.

## 🎯 Project Overview

A comprehensive security assessment demonstrating advanced phishing techniques to bypass Multi-Factor Authentication (MFA) in Microsoft Entra ID (formerly Azure AD) environments. This project showcases adversary simulation tactics using Evilginx2 for token capture and session hijacking.

### Key Achievements
- ✅ Successfully bypassed MFA using token-based session hijacking
- ✅ Performed external reconnaissance on Azure AD tenant
- ✅ Captured user credentials and authentication tokens
- ✅ Demonstrated real-world attack vectors against cloud identity providers

## 🏗️ Architecture

```
Attacker Infrastructure → Evilginx2 Phishing Proxy → Microsoft Entra ID → Target User
                          ↓
                    Token Capture & Session Hijacking
```

## 🛠️ Tools & Technologies

- **Microsoft Azure** - Cloud infrastructure
- **Microsoft Entra ID** - Identity and access management
- **PowerShell** - Automation and user provisioning
- **AADInternals** - Azure AD reconnaissance
- **Evilginx2** - Phishing framework with MFA bypass
- **DigitalOcean** - VPS hosting for attack infrastructure
- **Namecheap** - Domain registration
- **Cookie-Editor** - Session token manipulation

## 📁 Repository Structure

```
azure-entra-phishing-simulation/
├── README.md
├── DISCLAIMER.md
├── docs/
│   ├── setup-guide.md
│   ├── attack-flow.md
│   └── screenshots/
│       ├── evilginx-dashboard.png
│       ├── token-capture.png
│       └── successful-bypass.png
├── PS_Scripts/
│   ├── azure-setup/
│   │   ├── Create_Microsoft_Entra_ID_Users.ps1
│   └── reconnaissance/
│       ├── AADInternals_Commands.ps1

```

## 🚀 Quick Start

### Prerequisites
- Azure subscription with Global Administrator privileges
- PowerShell 7+ with Az module
- Linux VPS (DigitalOcean recommended)
- Registered domain name
- Basic understanding of Azure AD and authentication protocols


## 🔍 Reconnaissance Techniques

- **Tenant ID Discovery**: Identify target organization's Azure AD tenant
- **Domain Enumeration**: Map all domains associated with tenant
- **User Enumeration**: Validate email addresses without authentication
- **Authentication Method Discovery**: Determine if federated or managed

## 🎣 Phishing Methodology

1. **Adversary-in-the-Middle (AitM)**: Evilginx2 proxies authentication requests
2. **Token Capture**: Intercepts OAuth tokens and session cookies
3. **Real-time Proxying**: Maintains legitimate connection to Microsoft
4. **MFA Bypass**: Tokens contain MFA validation, bypassing additional checks


## 📸 Screenshots

| Evilginx Dashboard | Token Capture | Successful Bypass |
|-------------------|---------------|-------------------|
| ![Dashboard](docs/screenshots/evilginx-dashboard.png) | ![Tokens](docs/screenshots/token-capture.png) | ![Access](docs/screenshots/successful-bypass.png) |

## 📚 Learning Resources

- [Microsoft Entra ID Documentation](https://learn.microsoft.com/en-us/entra/identity/)
- [AADInternals GitHub](https://github.com/Gerenios/AADInternals)
- [Evilginx2 Documentation](https://github.com/kgretzky/evilginx2)
- [MITRE ATT&CK: Phishing](https://attack.mitre.org/techniques/T1566/)
- [OAuth 2.0 Security Best Practices](https://oauth.net/2/security-best-practices/)

## ⚖️ Legal & Ethical Considerations

- ✅ Obtain written authorization before testing
- ✅ Define scope and boundaries clearly
- ✅ Protect captured data and delete after assessment
- ✅ Provide detailed remediation guidance
- ✅ Follow responsible disclosure practices

**This project is intended for authorized security professionals conducting legitimate penetration tests.**

## 🤝 Contributing

Contributions are welcome! Please read the contributing guidelines before submitting pull requests.

## 🙏 Acknowledgments

- Microsoft Security Response Center
- Kuba Gretzky (Evilginx2 creator)
- Dr. Nestori Syynimaa (AADInternals creator)
- The cybersecurity community

---

**⚠️ Remember**: With great power comes great responsibility. Use these techniques only for authorized security assessments to improve organizational security posture.
