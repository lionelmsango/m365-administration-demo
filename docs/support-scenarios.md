# Common M365 Support Scenarios

Real-world admin tasks with step-by-step solutions.

---

## Scenario 1: User Forgot Password

**Problem:** User cannot sign in, forgot password

**Solution:**
1. Microsoft 365 Admin Center → Users → Active users
2. Find user, click name
3. Click "Reset password" (key icon)
4. Choose: Auto-generate password OR Let me create password
5. ✓ Require password change at next sign-in
6. Click "Reset password"
7. Send new password to user securely (don't email it!)
   
**Time:** 2 minutes

## Scenario 2: User Needs Access to Shared Mailbox

**Problem:** User cannot see shared mailbox in Outlook

**Solution:**
1. Teams & groups → Shared mailboxes
2. Click on the shared mailbox (e.g., "IT Support")
3. Click "Edit" next to Members
4. Click "+ Add members"
5. Search for user, select, click "Add"
6. Click "Save"
   
**Wait:** 15-30 minutes for changes to propagate

**User action:** - Outlook desktop: Restart Outlook, mailbox appears in left pane
Outlook web: Refresh browser, mailbox appears

**Time:** 5 minutes + wait time

---

## Scenario 3: User Can't Join Teams Meeting

**Problem:** External guest can't join Teams meeting

**Solution:**
1. Teams Admin Center → Meetings → Meeting settings
2. Check "Anonymous users can join a meeting": Should be ON
3. If off, turn it ON and click "Save"
   
**For organizer:**
1. Check meeting invite has correct join link
2. Verify meeting hasn't expired
3. Try generating new meeting link
   
**For guest:**
1. Use "Join on the web instead" option
2. Don't need Teams account for web join
3. Enter name and join
4. 
**Time:** 5-10 minutes

---

## Scenario 4: Can't Upload File to SharePoint

**Problem:** User gets error when uploading file to SharePoint

**Common causes:**
1. File name has invalid characters (< > : " / \ | ? *)
2. File path too long (>400 characters)
3. File size too large (>100GB for OneDrive, 250GB for SharePoint)
4. User doesn't have permission
   
**Solution:**

**Check permissions:**
1. SharePoint site → Settings (gear icon) → Site permissions
2. Verify user is in Members or Owners group
**Fix file name:**
1. Rename file to remove special characters
2. Keep name under 128 characters
   
**Fix path:**
1. Move to folder closer to root
2. Shorten folder names
   
**Time:** 5-10 minutes

---

## Scenario 5: License Assignment Error

**Problem:** Cannot assign license to user - "No licenses available"

**Solution:**
1. Billing → Licenses
2. Check available licenses
3. If none available:- Remove license from inactive user- OR purchase more licenses
   
**Reassign from inactive user:**
1. Users → Active users
2. Find inactive user
3. Click user → Licenses and apps
4. Uncheck license → Save
5. Assign to new user
   
**Time:** 5 minutes-

## Scenario 6: Shared Mailbox Sending Failed

**Problem:** User can't send email from shared mailbox

**Solution:**

**Check permissions:**
1. Shared mailboxes → Click mailbox
2. User needs both:- Full Access (to see mailbox)- Send As (to send emails)
   
**Add Send As:**
1. Click "Edit" next to Email forwarding
2. NO - that's wrong spot
3. Use Exchange Admin Center:
   - Recipients → Mailboxes
   - Click shared mailbox
   - Delegation tab
   - Add user to "Send As"

**Time:** 10 minutes

---

## Scenario 7: Too Many Emails in Mailbox

**Problem:** User mailbox is full (quota reached)

**Solution:**

**Quick fix:**
1. User should delete large emails
2. Empty Deleted Items folder
3. Archive old emails to PST (not recommended long-term)
   
**Admin fix - Increase quota:**
1. Exchange Admin Center → Recipients → Mailboxes
2. Click user mailbox
3. Edit mailbox quota
4. Increase "Issue warning at" and "Prohibit send at"
   
**Better solution:**
1. Enable Online Archive
2. Set up retention policy
3. Educate user on email management
   
**Time:** 15 minutes

---

## Scenario 8: External Sharing Not Working

**Problem:** User can't share OneDrive file with external person

**Solution:**
1. SharePoint Admin Center → Policies → Sharing
2. Check SharePoint sharing level: "Anyone" or "New and existing guests"
3. Check OneDrive sharing level: Same as SharePoint or more restrictive
   
**If set to "Only people in organization":**
1. Change to "New and existing guests"
2. Click "Save"
3. Wait 15 minutes for propagation

**Security note:**
- "Anyone" = no sign-in required (use carefully)
- "New and existing guests" = requires Microsoft account
  
**Time:** 10 minutes

---

## Quick Reference - Where to Find Things
| Task | Admin Center |
|------|--------------|
| Create user | Microsoft 365 → Users → Active users |
| Reset password | Microsoft 365 → Users → Active users |
| Assign license | Microsoft 365 → Users → Active users |
| Shared mailbox | Microsoft 365 → Teams & groups → Shared mailboxes |
| Mail flow rules | Exchange → Mail flow → Rules |
| Create team | Teams → Manage teams |
| Teams policies | Teams → Messaging/Meeting policies |
| SharePoint site | SharePoint → Active sites |
| MFA settings | Users → Active users → MFA |
| Security Score | Microsoft 365 Defender → Secure Score |
