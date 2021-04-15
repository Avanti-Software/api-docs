# Create Client Credentials
For your API developer to start using Avanti’s API, you’ll need to create the Client Credentials.

<!-- theme: info -->
>Curious about how we authenticate using client credentials? Our API authentication follows the Open ID Connect protocol to authenticate requests using short-lived access tokens.

If you’re an API developer, you’ll need to request some information from your organization’s Avanti Administrator: 
- The Client Credentials
- The Avanti Company Database

## Create the Client Credentials
**Step 1:** Once you've logged into the Avanti Self-Service Portal, manually navigate to the API Settings page:

**https&#58;//myavanti.ca/{Organization ID}-api/admin/apisettings** 

You may notice that there is  **-api** after the Organization ID in the URL. This is the base URL that you will use to make API calls, not the URL to your Avanti Self-Service Portal.

<!-- theme: info -->
>You’ll need to login as a Regular Avanti User with an ADMIN user group.  


**Step 2:** If this is your first time creating an API Client, you’ll need to read and agree to the **Terms and Conditions**.

![Terms and conditions example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fterms-conditions.png?alt=media&token=c558e359-8a26-4b55-b161-f8ce30ee45f2)

**Step 3:** Select **Generate Client**.

![Generate client button example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fgenerate-client-button.png?alt=media&token=bf7bf936-2354-471d-a3b3-ecec2b1f78e8)

**Step 4:** Enter a description in **Client Name**. 

<!-- theme: info -->
>While client names are for display purposes only and can be named anything you want, we recommend a description of the integration. 
For example, if you’re using the integration to add new employees into Avanti, you could call the client **Hire New Employees**. 


**Step 5:** Select **Client Never Expires** to allow this client access indefinitely. If the client should expire, enter the date the client should no longer have access in **Client Expiry Date**. 

<!-- theme: info -->
>Be cautious with clients that don’t expire; you're essentially granting lifetime access to this endpoint to anyone with these credentials. 

Setting a client expiry is especially useful when:
- creating a short-term integration.
- providing the credentials to a third party who only needs access for a limited time.


**Step 6:** Enter the number of minutes before access tokens expire. 

<!-- theme: info -->
>It is best practice to make your access tokens as short-lived as possible. If you’re unsure how long the client credentials need to be active, contact your API developer. 


**Step 7:** Select **Generate** to create the client. 

![Generate client form example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fgenerate-client-form.png?alt=media&token=01e646a3-b454-4443-9190-3caffa051236)

**Step 8:** Copy the Client ID and the Client Secret and store them in a safe place. You’ll need to send these to your API developer. 

![Generated client example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fclients-table.png?alt=media&token=3430bc59-228f-4d18-a077-95d3848bd3dc)


**Step 9:** Select **Exit Configuration**. 


## Identify the Avanti Company Database Name
You’ll need the Company Database name so the integration knows which Avanti company to access. If your integration includes multiple companies, you’ll need to identify every company and provide them to your API Developer. This name is different from the company name you see displayed when you select the company in Avanti.

**Step 1:** Open **Administration Settings** and select **System Info**. 
By default, this can be found in Administration. 

**Step 2:** Copy the **Company Database**. 


## Third-Party API Developers
While anyone at your organization can register to access Avanti’s API Documentation, your third-party API developer will need a special invite to gain access. 

To get access, you’ll need to request access and send your third-party API developer’s email to:
- Your Implementation Specialist, if you haven’t gone live yet. 
- Success@avanti.ca, if you're already using Avanti to process pay.

We’ll send your third-party developer an email to access Avanti’s API Documentation. 

## Provide Information to the API Developer
Wonderful! You’re all done setting up everything in Avanti for the API. Now, all you need to do is pass some information onto your API Developer. Here’s what they’ll need to get started:
- The name of the endpoint. If you’re using a reporter endpoint, they’ll also need the ID of the Report you created in Avanti.
- The Avanti Username and Password. Go to API Allow Employee Access for more information on creating users. 
- The API Client Credentials - the Client ID and the Client Secret. 
- The Avanti Company Database Name.
- Your Avanti Self-Service Portal URL.

Great! You’re all done setting up access to the API and your developer is ready to get started. 