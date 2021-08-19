# Create and Manage Azure AD Users in the Portal

## 1. Create Azure AD User Accounts

1. In the Azure portal, click the hamburger icon at the top-left of the screen to open the menu.

2. From the menu, select Azure Active Directory.

3. From the menu on the left, select Users.

4. From the menu at the top, click New user.

5. In the User name field, enter a username for the first new user account. Leave the domain name as is.

6. In the Name field, enter a first name and last name for the first new user account.

7. Scroll down and view some of the other options you can select for a new user account. For the purposes of this hands-on lab, you do not need to configure any other options for the new user account.

>Note: Attempting to assign a role to your user may break your hands-on lab.

8. Click Create.

9. Repeat steps 4 through 8 to create your second new user account.

10. Verify that both user accounts you just created now appear in the list of All users in your Azure Active Directory service.

## 2. Modify an Azure AD User Account

1. From the All users view, select one of the users you just created to open their profile.

2. View some of the options and settings that you can modify for a user account using the menu at the left.

3. If necessary, select Profile in the menu to return to the user's profile.

4. From the menu at the top, click Edit.

5. Modify some of the settings for the user, such as entering their First name and Last name or updating the information under Job info.

6. Click Save.

7. Click View to toggle back to the Profile view.

8. From the menu at the top, click Reset password.

9. In the Reset password pane that displays on the right, click the Reset password button.

>Note: This generates a temporary password that must be changed on the next sign in. You would need to take note of the temporary password that is displayed and provide it to the user.

## 3. Revoke Access to an Azure AD User Account

1. From the menu at the top, click Edit.

2. Scroll down to the Settings section and, for the Block sign in option, click Yes.

3. Click Save.

4. Click View to toggle back to the Profile view.

5. From the menu at the top, click Revoke sessions.

6. View the information that displays in the notification, and click Yes.

## 4. Delete an Azure AD User Account

1. From the menu at the top, click Delete.

2. View the information that displays in the notification, and click Yes.

3. From the menu at the top, click Refresh and verify that the user account has been removed from the accounts in the All users list.

4. From the menu on the left, select Deleted users. The user account you just deleted should appear in the list of deleted accounts.

5. Select the check box for the user account and note that you could choose the Restore user or Delete permanently options from the top menu if you needed to take further action on the account.