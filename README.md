#  Microsoft-Azure-Network File Shares and Permissions(Video below)
 Microsoft-Azure-ONetwork File Shares and Permissions (Video below)

Create some sample file shares with various permissions

1. Connect/log into DC-1 as your domain admin account (mydomain.com\jane_admin)
    
2. Connect/log into Client-1 as a normal user (mydomain\<someuser>)

3. On DC-1, on the C:\ drive, create 4 folders: “read-access”, “write-access”, “no-access”, “accounting”

4. Set the following permissions (share the folder) for the “Domain Users” group:

5. Folder: “read-access”, Group: “Domain Users”, Permission: “Read”

6. Folder: “write-access”,  Group: “Domain Users”, Permissions: “Read/Write”

7. Folder: “no-access”, Group: “Domain Admins”, “Permissions: “Read/Write”

8. (Skip accounting for now)

Attempt to access file shares as a normal user

9. On Client-1, navigate to the shared folder (start, run, \\dc-1)

10. Try to access the folders you just created. Which folders can you access? Which folders can you create stuff in? Does it make sense?

Create an “ACCOUNTANTS” Security Group, assign permissions, an test access

11. Go back to DC-1, in Active Directory, create a security group called “ACCOUNTANTS”

12. On the “accounting” folder you created earlier, set the following permissions:

13. Folder: “accounting”, Group: “ACCOUNTANTS”, Permissions: “Read/Write”

14. On Client-1, as  <someuser>, try to access the accountants folder. It should fail.

15. Log out of Client-1 as  <someuser>

16. On DC-1, make <someuser> a member of the “ACCOUNTANTS”  Security Group

17. Sign back into Client-1 as <someuser> and try to access the “accounting” share in \\DC-1\ - Does it work now?

