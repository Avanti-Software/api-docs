# Allow Employee Access

You’ll need an Avanti User to access the Avanti API endpoints. This User dictates which employees the API can access. 

We recommend creating a dedicated Avanti User for API authentication. If your integrations need different permissions in Avanti, you can create different users for each integration. 

For example, you should have two users if you’re integrating with both a human resources and time collection service – a user with the necessary HR roles and another with the necessary time collection roles.

You can create a user on the Avanti Desktop Application in Avanti Users. If you’re an API developer, you’ll need to get the Avanti User from the organization’s Avanti Administrator. 

The Avanti User must:
- be Active
- have a Regular or Manager Self Service User Class
- use Avanti Security
- have a User Group with access to the company and the required Pay Groups
- have the role permissions to the required employee positions granted in User Role Assignments

If you need an additional license to create the Avanti User, please contact your Client Success Manager at Success@avanti.ca.

### Create a User in Avanti
Rather than create a new user, we recommend copying an existing user who already has the correct access to Avanti employees. 

**Step 1:** Select a user with the correct employee access, right-click and select **Copy** in Avanti Users.
By default, this can be found in System Administration >> System Access Controls on the Avanti Desktop Application. 

![Copying an Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FCopyingAvantiUsers.png?alt=media&token=5c087096-96c6-4acc-84f4-8c61239f27a3) 

**Step 2:** Right-click and choose **Paste**. 
![Paste an Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FPasteanAvantiUser.png?alt=media&token=5703553b-b55a-431a-8702-4910f1f73086)

**Step 3:** Add the **User ID**. Keep **User Groups** and **Role Assignments** selected in Paste Details, then click **OK**.  

<!-- theme: info -->
>##### Additional Information
>It’s a great idea to name the User ID after your integration, so you can easily remember what this is for in the future. It may take a couple of moments to create the Avanti User. <br>
Please make a note of the User ID; you’ll need to send it to your API developer. 

![Paste details for an Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FPasteDetails.png?alt=media&token=211ca3b2-0719-4cc0-8992-db07785bc82a)

**Step 4:** Select the Avanti User you just created, then click **Modify**. 

![Modify the Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FModifytheAvantiUser.png?alt=media&token=d6c5ac0a-cfea-423a-be67-88cf9fa3607b)

**Step 5:** Set the following for the Avanti User: 
- Select **Active**, if it’s deselected. 
- Select either **Regular** or **Manager Self-Service** for User Class.
- Add a secure **Password** for the Avanti User, then **Confirm Password**. 
- Select **Avanti Security** in User Authenticated By, if it’s not already selected. 
<!-- theme: info -->
>##### Additional Information
>Please make a note of the User Password; you’ll need to send it to your API developer. 

![Avanti User Settings.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FAvantiUserSettings.png?alt=media&token=6e476e2f-969f-4e1a-8796-cf5073968c8a)


**Step 6:** Make a note of the User Groups in the **Selected Column** then select **OK** to save your changes.  

<!-- theme: info -->
>##### Additional Information
>You’ll need this information to allow access to the endpoint.

![Save the Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FSaveAvantiUser.png?alt=media&token=7e7930dd-0df6-4891-95a0-410fffb6ca57)

Nice work! The Avanti User is all set up. The next you'll need to [Allow Access to the Endpoint](/docs/auth-subfunction.md) for more information.  