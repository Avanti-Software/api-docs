# Access Tokens

## Requesting Access Tokens

An access token must be provided for each authenticated API request. You can request an access token using the [/connect/token](/avanti-auth-api/token/access-token) endpoint. The endpoint requires:
- [Client Credentials](/auth/client-credentials)
- [Avanti User Credentials](/auth/users)
- A unique Device ID

Device IDs differentiate services running on more than one device. We recommend using a prefix that identifies your service, followed by v4 UUID (universally unique identifier). Device IDs can be up to 128 characters long.

```
Device 1 ID: MyService1-49d62187-582c-4996-b29f-b183d7506aec
Device 2 ID: MyService2-0dfbfc98-c72b-4717-9c4b-ad461a7971e7
```

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
