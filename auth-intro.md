# Authentication

Avanti API Authentication follows the [Open ID Connect](https://openid.net/connect) authentication protocol and allows clients to make authenticated requests using short lived access tokens.

Before you can request an access token and make authenticated requests you will need to:

- Generate a unqiue Client ID and Client Secret.
- Create a Class A (Administrator) or Class B (Manager) Avanti User.
- Give the user Avanti User Group permissions to the Avanti Companies you want to use with the API.
- Setup Subfunction Access to the API endpoints you want made available.
