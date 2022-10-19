



# O365
  
Connect to Outlook using O365.  

## How to install this module
  
__Download__ and __install__ the content in 'modules' folder in Rocketbot path.

## How to use this module

Before using this module, you need to register your app in the Azure App Registrations portal.

1. Sign in to the Azure portal (Applications Registration: https://portal.azure.com/#view/Microsoft_AAD_RegisteredApps/ApplicationsListBlade ).
2. Select "New record".
3. Under “Compatible account types” supported choose:
    a. "Accounts in any organizational directory (any Azure AD directory: multi-tenant) and personal Microsoft accounts (such as Skype or Xbox)" for this case use Tenant ID = common
    b. "Only accounts from this organizational directory (only this account: single tenant) for this case use application-specific Tenant ID.
4. Set the redirect uri (Web) as: https://login.microsoftonline.com/common/oauth2/nativeclient and click "Register".
5. Copy the application (client) ID. You will need this value.
6. Under "Certificates and secrets", generate a new client secret. Set the expiration (preferably 24 months). Copy the VALUE of the created client secret (NOT the Secret ID). It will hide after a few minutes.
7. Under "API permissions", click "Add a permission", select "Microsoft Graph", then "Delegated permissions", find and select "Mail.ReadWrite" and "User.Read", and finally " Add permissions".
8. In the Rocketbot console a url will be generated (Example: https://login.microsoftonline.com/common/oauth2/v2.0/authorize?response_type=code&client_id=82f8efcd-6a0d-4532-a62e-3e2aecb4d19f&redirect_uri=https%3A%2F%2Flogin.microsoftonline.com%2Fcommon%2Foauth2%2Fnativeclient&scope=Mail.ReadWrite+User.Read.All&state=3LvNFBfX0qej9Q0rsixmSWjCGJyi0M&access_type=offline ), copy and paste it into your browser.
9. Accept the permissions granting and it will return a screen without content. Copy the URL (Example: https://login.microsoftonline.com/common/oauth2/nativeclient?code=M.R3_SN1.5dcda10b-6567-ce05-3a5b-f67145c62684&state=3LvNFBfX0qej9Q0rsixmSWjCGJyi0M) and paste it into Rocketbot console below "Paste the authenticated url here:".
10. Press "enter" and if the operation was successful you will see in the console: "Authentication Flow Completed. Oauth Access Token Stored. You can now use the API." and a file will have been created with your credentials, in the root folder of Rocketbot, called o365_token.txt or o365_token_{session}.txt.


## Overview


1. Connect to O365  
Connect to O365 application instance

2. List all emails  
List all email, you can specify a filter

3. List unread emails  
List unread emails

4. Read email for ID  
Read email for ID

5. Send Email  
Send email

6. Reply Email  
Reply an email

7. Forward Email  
Forward an email

8. Download attachments  
Download attached files

9. Mark as unread  
Mark an email as unread

10. Email folders list  
List of email folders

11. Move email  
Move an email from one folder to another

12. Create folder  
Creates a new folder in the email

13. Get groups  
Get list of Groups

14. Get group  
Get Group by ID

15. Get site  
Get site of the Group

16. Get site lists  
Get lists of the Site

17. Create List  
Create a new list

18. Get list Items  
Get the items of a list

19. Get Item  
Get an item from a list

20. Create Item  
Create an item in a list

21. Delete Item  
Delete an item from a list

22. Update Item  
Update an item data  




----
### OS

- windows
- mac
- linux
- docker

### Dependencies
- [**bs4**](https://pypi.org/project/bs4/)
### License
  
![MIT](https://camo.githubusercontent.com/107590fac8cbd65071396bb4d04040f76cde5bde/687474703a2f2f696d672e736869656c64732e696f2f3a6c6963656e73652d6d69742d626c75652e7376673f7374796c653d666c61742d737175617265)  
[MIT](http://opensource.org/licenses/mit-license.ph)