# Access Tokens
If you’re an API developer, you’ll need to request some information from your organization’s Avanti Administrator if you don't already have it: 
- The name of the endpoint.
- The Avanti Username and Password.
- API Client Credentials.
- Avanti company database name.
- Your Avanti Self-Service Portal URL.


## Requesting Access Tokens

An access token must be provided for each authenticated API request. You can request an access token using the [/connect/token](/reference/auth.v1.json/paths/~1connect~1token/post) endpoint. The endpoint requires:
- [Client Credentials](/docs/auth-client-credentials.md)
- [Avanti User Credentials](/docs/auth-users.md)
- A unique Device ID

Device IDs differentiate services running on more than one device. We recommend using a prefix that identifies your service, followed by v4 UUID (universally unique identifier). Device IDs can be up to 128 characters long.

```
Device 1 ID: MyService1-49d62187-582c-4996-b29f-b183d7506aec
Device 2 ID: MyService2-0dfbfc98-c72b-4717-9c4b-ad461a7971e7
```

> **Important:** When requesting an access token the content-type of the request must be **application/x-wwww-form-urlencoded**.

## Using Access Tokens

Access tokens are used as bearer tokens and must be included in the **Authorization** header of every authenticated request made by a client. Access tokens are prefixed with the Bearer keyword.

```
GET /v1/personalinfo
Authorization: Bearer {AccessToken}
```

Failure to include a token or providing an invalid token results in a 401 Unauthorized response from the server.

```
{
    title: "Unauthroized",
    status: 401
}
```
