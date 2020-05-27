# Client Credentials

When requesting an access token you will need to provide valid Client Credentials (ID and Secret). To generate Client Credentials:

1. Login to your Avanti Self Service Portal with a Class A (Administrator) Avanti User.

2. Once logged-in manually navigate to the API Settings page:

**https://myavanti.ca/{Organization ID}-api/admin/apisettings**

Take note of the **-api** after the Organization ID in the URL. This is the same base URL that you will use when making API calls, not the URL to your Avanti Self Service Portal.

3. Read and agree to the Terms and Conditions if required.

![Terms and conditions example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fterms-conditions.png?alt=media&token=ed1abfd7-e898-4edf-b7a7-14a5f79b22a0)

4. Click the **Genenerate Client** button to create a new client.

![Generate client button example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fgenerate-client-button.png?alt=media&token=bf7bf936-2354-471d-a3b3-ecec2b1f78e8)

5. Enter a name for the client. Client names are for display purposes only. While you can pick any name you want it is recommended you choose one that describes how this client will be using the Avanti API. Example: System X Integration

6. Enter a date for when the client will expire and no longer be valid or check the **Client Never Expires** checkbox. Setting a client expiry is useful when doing short term integration or are providing client credentials to a 3rd party who only need access for a limited time.

7. Enter the number of minutes before access tokens will expire. It is best practices to make your access tokens as short lived as possible.

8. Click the **Generate** button at the bottom of the form to generate the client.

![Generate client form example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fgenerate-client-form.png?alt=media&token=01e646a3-b454-4443-9190-3caffa051236)

7. Copy the Client ID and the Client Secret and store it in a safe place.

![Generated client example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fclients-table.png?alt=media&token=3430bc59-228f-4d18-a077-95d3848bd3dc)

When requesting an access token pass the Client Credentials in the **client_id** and **client_secret** parameters. If valid credentials are not included, the request will fail with a **invalid_client** error.
