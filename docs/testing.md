# Testing Avanti APIs

You can try out our API without leaving the documentation. Each API endpoint has a **Send a Test Request** section that you can use to send requests. This process is streamlined so you can familiarize yourself with the API quickly. 

## Request an Access Token

Before you can make a request to the Avanti API, you will need to make a Post Request for an access token. You can do this in the [Access Tokens](/reference/auth.v1.json/paths/~1connect~1token/post) section of the Tokens in Authentication API. Access tokens are required to make authenticated requests against the Avanti API. 

To create an Access Token, select Send in **Send a Test Request** at the bottom of the Access Token screen. The client credentials and a test user are pre-populated for your convenience. 

![Send a test request widget to get an access token.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fsend-token-request.png?alt=media&token=f6826e16-449e-4867-aa2f-b5253436623c)

If the request is successful, the response will contain an access token. Please copy the access token so you can paste it into a request.

![Copy access token from response.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fsend-token-response.png?alt=media&token=6ddc117e-0e2e-4441-8405-ddc4102a24d7)

## Making a Request

Once you have an access token, you are ready to start making requests. Go to **Send a Test Request** at the bottom of any Avanti API endpoint and paste the token into the **bearer_token** field in the **\$\$.env** section of the **Settings** tab.

![Paste the access token to the bearer_token field.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fsend-request-with-token.png?alt=media&token=7099627e-2a1e-4101-aad7-435aac6c818a)

This token is saved as a **bearer_token** environment variable will apply to all your requests going forward, so you should only need to set it on the initial request. You can verify this by viewing the **Authorization** header on the **Headers** tab.

![bearer_token variable is applied to authorization header.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fauthorization-header.png?alt=media&token=88caf679-5d3a-42b7-b00e-6481347e8e1e)

Access tokens to **Send a Test Request** are valid for two hours. Once it expires, request a new token. See the [Authentication](/docs/auth-getting-started.md) section for more details on how authentication works in the Avanti API.
