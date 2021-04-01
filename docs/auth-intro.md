# Authentication and Authorization 

Avanti API Authentication follows the [Open ID Connect](https://openid.net/connect) authentication protocol and allows clients to make authenticated requests using short-lived access tokens.

Before you can request an [Access Token](/docs/auth-tokens.md) and make authenticated requests you will need to:

- Generate unique [Client Credentials](/docs/auth-client-credentials.md), a Client Id and Client Secret.
- Create the [Avanti User](/docs/auth-users.md), a Class A (Administrator) or Class B (Manager) with the required company access and employee permissions. 
- Setup [Subfunction Access](/docs/auth-subfunction.md) to the API endpoints you want accessible. 
