# Complete Setup Guide

## Prerequisites Checklist
- [ ] Azure subscription (free trial works)
- [ ] Domain name registered
- [ ] Linux VPS (2GB RAM minimum)
- [ ] PowerShell 7+
- [ ] Basic networking knowledge

## Step-by-Step Instructions

### Environment Setup

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




