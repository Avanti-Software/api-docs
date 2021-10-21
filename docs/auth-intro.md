# Authentication and Authorization 

Avanti API Authentication follows the **Open ID Connect** authentication protocol and allows clients to make authenticated requests using short-lived access tokens. To learn more about this authentication protocol, go to [Open ID Connect.](https://openid.net/connect)

Before an API Developer can request an [Access Token](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2Njk-access-tokens
) and make authenticated requests, they'll need:

- Create the [Employee Access](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzA-employee-access), a Regular or Manager User with the required company access and employee permissions.
- Set the [Endpoint Access](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2Njg-endpoint-access) to the API endpoints you want accessible. 
- Generate unique [Client Credentials,](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NjY-client-credentials) a Client Id, Client Secret and the Avanti Company Database Name. 
