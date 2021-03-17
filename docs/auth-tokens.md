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

### Company

When requesting an access token you need to provide the company you are requesting a token for. This is done using the `company` parameter. This parameter is expecting the company database name, not the company display name.

To find the company database name in ASSP, navigate to the **Admin** page and select the **System Info** tab.

![ASSP Company Database Name Location](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fassp-company-db-location.png?alt=media&token=9530f880-2ba5-462c-b17e-cc441bb6784f)

To find the company database name in Avanti, right click any menu item and select properties or press the keyboard shortcut ctrl+p. This will open the properties window.

![Avanti Database Name Location](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Favanti-company-db-location.png?alt=media&token=fc120776-be97-47ab-a432-ad7d2ac4fac1)

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
