# Create Client Credentials
For your API developer to start using Avanti’s API, you’ll need to create the Client Credentials.

<!-- theme: info -->
>Curious about how we authenticate using client credentials? Our API authentication follows the [Open ID Connect](https://openid.net/connect/) Protocol to authenticate requests using short-lived access tokens.

## Create the Client Credentials

**Step 1:** Select **System Configuration** in the New Avanti Experience on ASSP. 

<!-- theme: info -->
>You’ll need to login as a Regular Avanti User with an ADMIN user group.  

![System Configuration.](../assets/images/SyConfiguration.png)

**Step 2:** In System, select **API Settings**.

![API Settings.](../assets/images/APISettings.png)


**Step 3:** Select **Generate Client**.

![Generate client button example.](../assets/images/GenerateClients.png)

**Step 4:** Enter a description in **Client Name**. 

<!-- theme: info -->
>While client names are for display purposes only and can be named anything you want, we recommend a description of the integration. 
For example, if you’re using the integration to add new employees into Avanti, you could call the client **Hire New Employees**. 

![ClientName.](../assets/images/ClientName.png)

**Step 5:** Select **Client Never Expires** to allow this client access indefinitely. If the client should expire, enter the date the client should no longer have access in **Client Expiry Date**. 

<!-- theme: info -->
>Be cautious with clients that don’t expire; you're essentially granting lifetime access to this endpoint to anyone with these credentials. 

Setting a client expiry is especially useful when:
- creating a short-term integration.
- providing the credentials to a third party who only needs access for a limited time.

![Client Expiry.](../assets/images/ClientExpiry.png)

**Step 6:** Enter the number of minutes before access tokens expire. 

<!-- theme: info -->
>It is best practice to make your access tokens as short-lived as possible. If you’re unsure how long the client credentials need to be active, contact your API developer. 

![Access Token Lifetime.](../assets/images/AccessTokenLifetime.png)

**Step 7:** Select **Generate** to create the client. 

![Generate the Client.](../assets/images/GenerateTheClient.png)

**Step 8:** Copy the Client ID and the Client Secret and store them in a safe place. You’ll need to send these to your API developer. 

![Copy the Client ID and Secret.](../assets/images/CopyClient.png)

**Step 9:** Select **Exit Configuration**. 

![Exit Configuration.](../assets/images/ExitConfig.png)

## Reload Web Settings

**Step 1:** Open **Administration Settings** in the New Avanti Experience on ASSP and select **Reload Settings**. <br>
By default, this can be found in Administration on the Avanti Self-Service Portal. 


![Admin Settings.](../assets/images/ReloadSettings.png)


## Identify the Avanti Company Database Name
You’ll need the company database name so the integration knows which Avanti company to access. If your integration includes multiple companies, you’ll need to identify each company and provide them to your API Developer. This name differs from the company name you see when selecting the company in Avanti.

>If you’ve [already moved to the latest ASSP](https://help.avanti.ca/support/solutions/articles/36000498186-faq#FAQ-Q:HowdoIknowifmycompanyalreadyhasthelatestASSP?), you won’t see Reload Settings; your changes will take effect within 5 minutes.

**Step 1:** Open **Companies** in the Avanti Desktop. By default, this can be found in System Administration >> System Access Controls. 

![Companies in Avanti Desktop](../assets/images/CompanyInDesktop.png)

**Step 2:** Right-click on a Company, select **Export to Excel** or **Export to OneDrive**, and save the file. From there, you can copy the names from the **CompanyName** column.

![Company Database Name](../assets/images/CompanyName-ExportExcel.png)


## Provide Information to the API Developer
Wonderful! You’re all done setting up everything in Avanti for the API. Now, all you need to do is pass some information onto your API Developer. Here’s what they’ll need to get started:
- The URL for the API documentation https://apidocs.avanti.dev/. 
- The name of the endpoint. If you’re using a reporter endpoint, they’ll also need the ID of the Report you created in [Custom Endpoints.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzE-custom-endpoints)
- The Avanti Username and Password created in [Employee Access](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzA-employee-access). 
- The API Client Credentials - the Client ID and the Client Secret. 
- The Avanti Company Database Name.
- Your Avanti Self-Service Portal URL.

Great! You’re all done setting up access to the API and your developer is ready to get started. 