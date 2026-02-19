# M365 Administration Setup Guide

This document explains how I set up the M365 environment for this demo project.

## Prerequisites 
- Microsoft account (free)
- Internet connection

## Step-by-Step Setup

### 1. Get Microsoft 365 Business Standard

1. Visit: https://login.microsoftonline.com
2. Sign up with your personal and billing information (free for the first month)
3. Choose Business standard monthly subscription
4. Save admin credentials securely

**Result:** Tenant with 25 Office 365 E5 licenses

### 3. Create Users

**Via Admin Center:**
- Navigate to Users → Active users
- Click "+ Add a user"
- Fill in user details
- Assign Office 365 E5 license
- Save password

### 4. Configure Exchange Online

**Shared Mailbox:**
1. Teams & groups → Shared mailboxes
2. Add shared mailbox
3. Assign members
   
**Mail Flow Rules:**
1. Exchange Admin Center → Mail flow → Rules
2. Create rules for security (external warnings, attachment blocking)

### 5. Set Up Teams

**Create Team:**
1. Teams Admin Center → Manage teams
2. Add team with members
3. Create channels
   
**Configure Policies:**
1. Messaging policies: Control chat features
2. Meeting policies: Recording, transcription, screen sharing
   
### 6. Create SharePoint Site
1. SharePoint Admin Center → Active sites
2. Create team site
3. Add owners and members
4. Create document libraries as needed

### 7. Enable Security Features

**MFA:**
1. Users → Active users → Multi-factor authentication
2. Enable for all users
**Security Defaults:**
1. Azure Portal → Azure AD → Properties
2. Manage security defaults → Enable
   
**Safe Links:**
1. Microsoft 365 Defender → Policies & rules
2. Threat policies → Safe Links
3. Configure global settings

## Troubleshooting

**Issue:** Can't access admin centers  
**Solution:** Ensure signed in with admin account, clear browser cache

**Issue:** User can't access shared mailbox  
**Solution:** Check permissions, wait 15-30 minutes for propagation

## Time Investment
- Tenant setup: 30 minutes
- PowerShell installation: 45 minutes
- User creation: 30 minutes
- Exchange config: 1.5 hours
- Teams setup: 1 hour
- SharePoint: 45 minutes
- Security: 1 hour
- **Total: ~6 hours**


   
