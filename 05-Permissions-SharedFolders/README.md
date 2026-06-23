# 05 - Shared Folders & NTFS Permissions

## Goal
Create shared folders with proper NTFS permissions so that only the right users and groups can access them.

## Shares Created
| Folder | Shared Name | Access |
|--------|-------------|--------|
| C:\Shares\IT | IT$ | IT-Team only |
| C:\Shares\HR | HR$ | HR-Team only |
| C:\Shares\Finance | Finance$ | Finance-Team only |

## Steps
1. On the server, create folders under C:\Shares
2. Right click folder → Properties → Sharing → Advanced Sharing
3. Enable sharing and set share permissions
4. Go to Security tab → set NTFS permissions per group
5. Remove "Everyone" from permissions
6. Test access from Windows 11 client with different user accounts
7. Verify users can only access their own department folder

## Verification
- john.smith (IT) can access \\DC01\IT$ but not HR$ or Finance$
- sara.jones (HR) can access \\DC01\HR$ but not IT$ or Finance$

## Screenshots
*(screenshots will be added here)*

## Notes & Issues
*(document any issues you ran into and how you fixed them)*
