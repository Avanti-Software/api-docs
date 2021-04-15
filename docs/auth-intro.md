# Authentication and Authorization 

Avanti API Authentication follows the **Open ID Connect** authentication protocol and allows clients to make authenticated requests using short-lived access tokens. To learn more about this authentication protocol, go to [Open ID Connect](https://openid.net/connect). 

Before you can request an [Access Token](/docs/auth-tokens.md) and make authenticated requests you need:

- Create the [Employee Access](/docs/auth-users.md), a Class A (Administrator) or Class B (Manager) with the required company access and employee permissions. 
- Set the [Endpoint Access](/docs/auth-subfunction.md) to the API endpoints you want accessible. 
- Generate unique [Client Credentials](/docs/auth-client-credentials.md), a Client Id and Client Secret.
