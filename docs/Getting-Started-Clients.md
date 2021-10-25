# Getting Started on the API

Before your API developer can get started leveraging Avanti’s API, there are a couple of steps you’ll need to complete. Regardless of whether an API developer you have on staff or a third-party is creating the integration, this setup is the same.  
- Decide which Avanti Endpoint would work for your integration. 
- Grant access in Avanti for API. 
- Provide your API developer or the API third-party with the credentials they need. 
- Your API/third-party developer creates the integration leveraging Avanti’s endpoints. 


## Find the Avanti Endpoint
Endpoints determine which information in Avanti is accessed. Our endpoints can: 
- Gather information from Avanti for use in another system. 
- Add, update, or remove information from within Avanti. 

You can find all the available endpoints in the Avanti API section. You can work with your API developer to identify the endpoint that works for your integration. 

<!-- theme: info -->

> ##### Additional Information 
If you’re trying to gather employee information from Avanti and can’t find an endpoint for the information, you can create a [Custom Endpoint](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzE-custom-endpoints) using the Reporter Endpoints. <br>The Reporter endpoint gathers information contained in a Report Designer report. All you need to do is create a report in Avanti that collects all the information needed to integrate. 

If you still can’t find the endpoint you’re looking for, please contact your Implementation Specialist or Client Success Manager, success@avanti.ca; they can help guide you through any questions. 

## Grant Access to the API in Avanti
There’s several things you’ll need to set up in Avanti to ensure only the people you want can access your data. 

**1. Allow Employee Access** <Br>
The Avanti User dictates the information and employees the API can access. This user's permissions determine access to the information and employees. 

Permissions and access work the same as if the user accessed the information within Avanti, using User Group and Role Assignment Permissions. The API User must:
- be an active Regular or Manager User with a secure password. 
- have User Group and Role Assignments to access the desired employees and information from Avanti. 

For all the details to grant access, go to [Employee Access.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzA-employee-accessd) Your API developer needs the Avanti Username and password to create the integration. 

**2. Allow Endpoint Access** <Br>
Endpoint Access determines what the integration can access. 
To ensure your data’s safety, information for every endpoint is inaccessible until you grant access. You can allow access to each endpoint individually or grant access to all endpoints. We recommend only allowing access to the endpoints you intend to use for security purposes. 

For all the details to grant access, go to [Endpoint Access.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2Njg-endpoint-access) Your API developer needs the API endpoints to create the integration. 

**3. Create Client Credentials and Identify the Avanti Company Database** <Br>
The API client credentials authorize the use of the API on the Avanti Self-Service Portal. The first time you create your API client credentials, you’ll need to review and accept the Avanti Software API Terms of Use. 

You’ll also need to identify which Avanti Company Database the integration needs to access. If you’re integrating to multiple companies, you’ll need to identify each and provide them to your API developer. This name is different from the company name you see displayed when you select the company in Avanti. 

For all the details to grant access and identifying the Avanti Company Database, go to [Client Credentials.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NjY-client-credentials) Your API developer needs the API Client Credentials and the Avanti Database to create the integration. 

## Provide Information to the API Developer
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