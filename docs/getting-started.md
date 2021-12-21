# Getting started

This guide will walk you through the steps to make your first API request. If this is your first time accessing the Avanti API you will first need to create your Access Token in Avanti with appropriate access levels.

## Identify which endpoint you would like to use

Endpoints determine which information in Avanti is accessed. Our endpoints can: 
- Gather information from Avanti for use in another system. 
- Add, update, or remove information from within Avanti. 

You can find all the available endpoints in the Avanti API section. You can work with your API developer to identify the endpoint that works for your integration. 

<!-- theme: info -->

> ##### Additional Information 
If you’re trying to gather employee information from Avanti and can’t find an endpoint for the information, you can create a [Custom Endpoint](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzE-custom-endpoints) using the Reporter Endpoints. All you need to do is create a report in Avanti that collects all the information needed to integrate. 

If you still can’t find the endpoint you’re looking for, please contact your Implementation Specialist or Client Success Manager at success@avanti.ca.

## Grant access to the API in Avanti

#### 1. Allow employee access

The Avanti User directs which information and employees the API can access. This user's permissions determine access to the information and employees. 

Permissions and access work the same as if the user accessed the information within Avanti, using User Group and Role Assignment Permissions. The API User must:
- be an active Regular or Manager User with a secure password. 
- have User Group and Role Assignments to access the desired employees and information from Avanti. 

For all the details to grant access, go to [Employee Access.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzA-employee-accessd) Your API developer needs the Avanti Username and password to create the integration. 

#### 2. Allow endpoint access

Endpoint Access determines what the integration can access. 
To ensure your data’s safety, information for every endpoint is inaccessible until you grant access. You can allow access to each endpoint individually or grant access to all endpoints. We recommend only allowing access to the endpoints you intend to use for security purposes. 

For all the details to grant access, go to [Endpoint Access.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2Njg-endpoint-access) Your API developer needs the API endpoints to create the integration. 

#### 3. Create client credentials and identify the Avanti company database

The API client credentials authorize the use of the API on the Avanti Self-Service Portal. The first time you create your API client credentials, you’ll need to review and accept the Avanti Software API Terms of Use. 

You’ll also need to identify which Avanti Company Database the integration needs to access. If you’re integrating to multiple companies, you’ll need to identify each and provide them to your API developer. This name is different from the company name you see displayed when you select the company in Avanti. 

For all the details to grant access and identifying the Avanti Company Database, go to [Client Credentials.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NjY-client-credentials) Your API developer needs the API Client Credentials and the Avanti Database to create the integration. 

## Provide information to the API developer

You’re all done setting up everything in Avanti for the API. Now, all you need to do is pass some information onto your API developer. Here’s what they’ll need to get started:

- The API Documentation, https://apidocs.avanti.dev/.
- The name of the endpoint.
- The ID of the Report you created in Avanti, if you’re using a report endpoint. 
- The Avanti Username and Password. 
- API Client Credentials. 
- Avanti Company Database name. 
- Your Avanti Self-Service Portal URL. 
Now you're API developer will have everything they need to get started [Creating Access Tokens.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2Njk-access-tokens
)

## Code samples

The following code samples demonstrate a basic API request to retrieve details of an employee by their employee number. Be sure to replace the following variables with your own values when using these samples.

|Variable|Description|
|--|--|
|EMPLOYEE_NUMBER|The unique employee number of the individual|
|COMPANY|The name of your company database|
|TOKEN|Your personal access token granted during authentication|

#### JavaScript

```js
const requestUri = "https://myavanti.ca/COMPANY-api/v1/Employees/Details?empNo=EMPLOYEE_NUMBER";

fetch(requestUri, {
    "method": "GET",
    "headers": {
        "Content-Type": "application/json",
        "Authorization": "Bearer TOKEN"
    }
}).then(response => {
    console.log(response);
}).catch(error => {
    console.error(error);
}
````

#### C#

```csharp
string requestUri = "https://myavanti.ca/COMPANY-api/v1/Employees/Details?empNo=EMPLOYEE_NUMBER";

var client = new HttpClient();
var request = new HttpRequest
{
    Method = HttpMethod.Get,
    RequestUri = new Uri(requestUri),
    Headers =
    {
        { "Authorization", "Bearer TOKEN" },
        { "Content-Type": "application/json" }
    }
};

using (var response = await client.SendAsync(request))
{
    var body = await.Response.Content.ReadAsStringAsync();

    Console.WriteLine(body);
}
```

#### Java

```java
String requestUri = "https://myavanti.ca/COMPANY-api/v1/Employees/Details?empNo=EMPLOYEE_NUMBER";

HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create(requestUri))
    .header("Content-Type", "application/json")
    .header("Authorization", "Bearer TOKEN")
    .method("GET", HttpRequest.BodyPublishers.noBody())
    .build();

HttpResponse<String> response = HttpClient
    .newHttpClient()
    .send(request, HttpResponse.BodyHandlers.ofString());

System.out.println(response.body());

```