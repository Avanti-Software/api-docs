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

**Step 1:** Open **Avanti Users** in the Avanti Desktop Application.
By default, this can be found in System Administration >> System Access Controls. 

**Step 2:** Select a user with the correct employee access, right-click and select **Copy**.
![Copying an Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FCopying%20an%20Avanti%20User.png?alt=media&token=29b5fa25-6456-4511-bd43-b984213a8640) 

**Step 3:** Right-click and choose **Paste**. 
![Paste an Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FPaste%20an%20Avanti%20User.png?alt=media&token=0cdb853b-3abc-426a-8766-ce5dc1752003)

**Step 4:** Add the **User ID**. Keep **User Groups** and **Role Assignments** selected in Paste Details, then click **OK**.  

<!-- theme: info -->
>##### Additional Information
>It’s a great idea to name the User ID after your integration, so you can easily remember what this is for in the future. It may take a couple of moments to create the Avanti User. <br>
Please make a note of the User ID; you’ll need to send it to your API developer. 

![Paste details for an Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FPasteDetails.png?alt=media&token=211ca3b2-0719-4cc0-8992-db07785bc82a)

**Step 5:** Select the Avanti User you just created, then click **Modify**. 

![Modify the Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FModifytheAvantiUser.png?alt=media&token=129921ca-517a-4a91-8a8e-662e142c3cf9)

**Step 6:** Set the following for the Avanti User: 
- Select **Active**, if it’s deselected. 
- Select either **Regular** or **Manager Self-Service** for User Class.
- Add a secure **Password** for the Avanti User, then **Confirm Password**. 
- Select **Avanti Security** in User Authenticated By, if it’s not already selected. 
<!-- theme: info -->
>##### Additional Information
>Please make a note of the User Password; you’ll need to send it to your API developer. 

![Avanti User Settings.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FAvantiUserSettings.png?alt=media&token=a8460bb2-3450-4688-a564-4ff49b6f0840)


**Step 7:** Make a note of the User Groups in the **Selected Column** then select **OK** to save your changes.  

<!-- theme: info -->
>##### Additional Information
>You’ll need this information to allow access to the endpoint.

![Save the Avanti User.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FCreating%20Users%2FSaveAvantiUser.png?alt=media&token=81a67d1e-3fb2-47e9-bc9e-b3da1044fe95)

Nice work! The Avanti User is all set up. The next step is Allow Access to the Endpoint. 
**Marketing, please add the link.**