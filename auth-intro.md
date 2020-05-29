# Authentication

Avanti API Authentication follows the [Open ID Connect](https://openid.net/connect) authentication protocol and allows clients to make authenticated requests using short-lived access tokens.

Before you can request an [Access Token](/auth-tokens) and make authenticated requests you will need to:

- Generate [Client Credentials](/auth-client-credentials), a unique Client ID and Client Secret.
- Create the [User Account](/auth-users), a Class A (Administrator) or Class B (Manager) Avanti User with the proper User Group permissions to the Avanti Company. 
- Setup [Subfunction Access](/auth-subfunction) to the API endpoints you want accessible. 
