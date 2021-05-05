# Create Client Credentials
For your API developer to start using Avanti’s API, you’ll need to create the Client Credentials.

<!-- theme: info -->
>Curious about how we authenticate using client credentials? Our API authentication follows the [Open ID Connect](https://openid.net/connect/) Protocol to authenticate requests using short-lived access tokens.

## Create the Client Credentials
Avanti 10 must be applied before you can create Client Credentials. 

**Step 1:** Select **System Configuration** in the New Avanti Experience on ASSP. 

<!-- theme: info -->
>You’ll need to login as a Regular Avanti User with an ADMIN user group.  

![System Configuration.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FSystemConfiguration.png?alt=media&token=6b3b4530-18f6-4608-8ca1-1722cf0403d3)

**Step 2:** In System, select **API Settings**.

![API Settings.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FAPISettings.png?alt=media&token=b2192e1b-41eb-4b8c-8b2d-fcb6529c5eeb)

**Step 3:** If this is your first time creating an API Client, you’ll need to read and agree to the [Terms and Conditions.](https://www.avanti.ca/api-terms-of-use)

![Terms and conditions example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fterms-conditions.png?alt=media&token=c558e359-8a26-4b55-b161-f8ce30ee45f2)

**Step 4:** Select **Generate Client**.

![Generate client button example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FGenerateClients.png?alt=media&token=883ae45b-b7a4-4047-ac22-519b61f6d642)

**Step 5:** Enter a description in **Client Name**. 

<!-- theme: info -->
>While client names are for display purposes only and can be named anything you want, we recommend a description of the integration. 
For example, if you’re using the integration to add new employees into Avanti, you could call the client **Hire New Employees**. 

![ClientName.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FClientName.png?alt=media&token=ee4a7b33-3c76-4e64-bdd4-43d53c7318df)

**Step 6:** Select **Client Never Expires** to allow this client access indefinitely. If the client should expire, enter the date the client should no longer have access in **Client Expiry Date**. 

<!-- theme: info -->
>Be cautious with clients that don’t expire; you're essentially granting lifetime access to this endpoint to anyone with these credentials. 

Setting a client expiry is especially useful when:
- creating a short-term integration.
- providing the credentials to a third party who only needs access for a limited time.

![Client Expiry.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FClientExpiry.png?alt=media&token=776808de-8fb0-42fc-b14a-046bc8fac5a6)

**Step 7:** Enter the number of minutes before access tokens expire. 

<!-- theme: info -->
>It is best practice to make your access tokens as short-lived as possible. If you’re unsure how long the client credentials need to be active, contact your API developer. 

![Access Token Lifetime.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FAccessTokenLifetime.png?alt=media&token=d2361089-4943-43e5-b20b-15fc8523b8a4)

**Step 8:** Select **Generate** to create the client. 

![Generate the Client.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FGenerateTheClient.png?alt=media&token=a66b34b4-027b-405e-862a-58c418f346eb)

**Step 9:** Copy the Client ID and the Client Secret and store them in a safe place. You’ll need to send these to your API developer. 

![Copy the Client ID and Secret.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FCopyClient.png?alt=media&token=c3a54a89-4547-4c2a-8067-aa12290d8643)


**Step 10:** Select **Exit Configuration**. 

![Exit Configuration.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FExitConfig.png?alt=media&token=5073d9c3-e4bc-4e76-858f-a1cf63329d6f)


## Identify the Avanti Company Database Name
You’ll need the Company Database name so the integration knows which Avanti company to access. If your integration includes multiple companies, you’ll need to identify every company and provide them to your API Developer. This name is different from the company name you see displayed when you select the company in Avanti.

**Step 1:** Copy the **Company Database** on the System Info Tab in Administration Settings. You'll need to send this to your API Developer.
By default, this can be found in Administration on the Avanti Self-Service Portal. 

![ASSP Company Database Name Location](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2FClient%20Credentials%2FCompanyDatabaseName.png?alt=media&token=ac4ffec3-14db-4da7-921d-834eb5fe7e75)

## Provide Information to the API Developer
Wonderful! You’re all done setting up everything in Avanti for the API. Now, all you need to do is pass some information onto your API Developer. Here’s what they’ll need to get started:
- The URL for the API documentation https://apidocs.avanti.dev/. 
- The name of the endpoint. If you’re using a reporter endpoint, they’ll also need the ID of the Report you created in [Custom Endpoints.](/docs/custom-endpoints.md)
- The Avanti Username and Password created in [Employee Access](/docs/auth-users.md). 
- The API Client Credentials - the Client ID and the Client Secret. 
- The Avanti Company Database Name.
- Your Avanti Self-Service Portal URL.

Great! You’re all done setting up access to the API and your developer is ready to get started. 