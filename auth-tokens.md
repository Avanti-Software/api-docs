# Access Tokens

## Requesting Access Tokens

Access tokens are requested using the [/connect/token](/avanti-auth-api/token/access-token) endpoint. The endpoint requires [Client Credentials](/auth/client-credentials), [Avanti User Credentials](/auth/users) and a unqiue Device ID. Device ID's are used to differentiate services that might be running on more than one device. Device ID's can be up to 128 characters long, we recommend you use a prefix that identifies your service followed by v4 UUID (universally unique identifier).

```
Device 1 ID: MyService1-49d62187-582c-4996-b29f-b183d7506aec
Device 2 ID: MyService2-0dfbfc98-c72b-4717-9c4b-ad461a7971e7
```

## Using Access Tokens

Access tokens are used as bearer tokens and are provided in the **Authorization** header of every authenticated request made by a client. Access tokens are prefixed with the Bearer keyword.

```
GET /v1/personalinfo
Authorization: Bearer {AccessToken}
```

Failure to include an token or providing an invalid token will result in a 401 Unauthroized response from the server.

```
{
    title: "Unauthroized",
    status: 401
}
```
