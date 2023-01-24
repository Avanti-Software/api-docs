# Allow Endpoint Access

The API cannot access any of your Avanti information until you allow it. There’s two ways to grant access to an endpoint:
1. Grant access to a specific endpoint. 
2. Grant access to all endpoints. 

We recommend setting up access for each endpoint separately to ensure maximum security. 

If you’re an API developer, you’ll need to coordinate with the organization’s Avanti Administrator for access. 

## API Endpoint Access Overview
Before creating subfunction access controls, you’ll need to know a little more about how to grant access. The view, insert, modify, and delete responsibilities on the subfunction access define the accessibility to the endpoint’s methods.
- For a GET endpoint, the API User must have view responsibilities.
- For a DELETE endpoint, the API User must have delete responsibilities.
- For a POST or PUT endpoint, the API User must have modify or insert responsibilities depending on whether it’s updating or creating entries. We recommend granting access to both unless access to one should be restricted.

The Avanti User has access based on the assigned User Groups. Their user group must match or be higher than the responsibility level on the subfunction access. The responsibility levels range from A to Z, with A being the highest and Z being the lowest. If the responsibility level on the subfunction access is a , all users have access.

The Avanti User must also have user group access to at least one of the Selected User Groups unless the Selected User Group column has an &ast;. If it has a &ast;, all users have access.

<!-- theme: info -->
>If you haven’t already created an Avanti User for the API integration, go to [API Allow Employee Access](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzA-employee-access) for more information. 

## Grant Access to an Endpoint

To grant access to a specific API endpoint, you’ll first need to identify the endpoint from the Avanti API section of the [API Documentation.](https://avanti.stoplight.io/) 

![Endpoint.](../assets/images/Endpoint.png)

Once you’ve identified the endpoint, you’ll be able to grant access. We recommend copying and pasting endpoints from the documentation to avoid mistakes when creating the subfunction access. When copying, be sure to exclude any path parameter; path parameters are anything with **/{  }**.  

For example, entering **api/v1/Dependents** in the subfunction access grants access to both these endpoints, which only differ by the path parameter /{empNo}:  

![Both endpoints.](../assets/images/EndpointsDependants.png)

**Step 1:** Select **Insert** in Subfunction Access Controls.
By default, this can be found in System Administration >> System Access Controls on the Avanti Desktop Application.

![Insert for endpoint access. ](../assets/images/EndpointAccessInsert.png)

**Step 2:** Add **api** in **Function**, then add the endpoint copied from the **API Documentation**.

<!-- theme: info -->
>The copied text should start with the version, such as /v1. If it ends in a parameter, such as /{empNo}, ensure it’s **excluded**. 

![Insert for endpoint access. ](../assets/images/EndpointAccessFunction.png)

**Step 3:** Add a **Description** for the endpoint. 

![Add Description for endpoint access. ](../assets/images/EndpointAccessDescription.png)

**Step 4:** Set your desired Responsibility to **Insert, Modify (edit), View** and **Delete** using the endpoint. 

- To allow the API to insert, modify, view, and delete, skip to Step 6. 
- To prevent the API from having access, replace the &ast; with a - in the Responsibility. 

For example, I want to use an endpoint to gather dependent information from Avanti. I could have a &ast; for View and a - for Insert, Modify and Delete. This prevents the API from adding, editing, and deleting dependents in Avanti while allowing access to view the dependent information. 
<!-- theme: info -->
>Here’s a quick guide to help align the responsibility needed to the endpoint you’re using. 
>- For a GET endpoint, the API User must have **View** responsibilities.
>- For a DELETE endpoint, the API User must have **Delete** responsibilities.
>- For a POST or PUT endpoint, the API User must have **Modify** and/or **Insert** responsibilities depending on whether you’re updating or creating entries. We recommend granting access to both unless access to one should be restricted.

![Adjust Responsibility for endpoint access. ](../assets/images/EndpointAccessResponsibility.png)

**Step 5:** Select &ast; in the selected column, then select the Arrow to remove full access.

![Remove User Group for endpoint access. ](../assets/images/EndpointAccessRemoveWildcard.png)

**Step 6:** Select one of the User Groups assigned to your API User, then select the Arrow. Click **OK** to save. 

<!-- theme: info -->
>If you haven’t already created an Avanti User for the API integration, go to [API Allow Employee Access](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzA-employee-access) for more information. 

![Save endpoint access. ](../assets/images/EndpointAccessOk.png)

Congratulations! You’re done enabling access to the endpoint. Repeat these steps for every endpoint you’ll use in the integration.

<!-- theme: info -->
>If you're adjusthing access and already have Client Credentials, all you'll need to do is [Reload Settings](https://avanti.stoplight.io/docs/avanti-api/45925478e011d-create-client-credentials#reload-web-settings) for your changes to take effect.  

The next step to setup the API is [Create the Client Credentials.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NjY-client-credentials) 

## Grant Access to All Endpoints

To grant access to all endpoints, insert a subfunction access rule in the Avanti Desktop Application. 

<!-- theme: warning -->
>For maximum security, we recommend you do not use this option; it allows the API integration access to all your employees' information. Instead, set up subfunction access for every endpoint you’re using for your integrations.

**Step 1:** Select **Insert** in Subfunction Access Controls, then add api/* in Function. 
By default, this can be found in System Administration >> System Access Controls on the Avanti Desktop Application.

![Insert for full access. ](../assets/images/FullAccessFunction.png)

**Step 2:** Add a **Description** for the endpoint, such as Access to API Endpoints.  

![Add Description for full access. ](../assets/images/FullAccessDescription.png)

**Step 3:** Set the Responsibility to **Insert, Modify (edit), View** and **Delete** using the endpoint. 

- To allow full access to insert, modify, view, and delete, select **OK** and you're done granting access.  
- To prevent the API  from having access, replace the &ast; with a - in the Responsibility. For example, I want to use the API to gather information from Avanti. I could have a &ast; for view and - for Insert, Modify and Delete. This prevents the API from adding, editing or deleting information in Avanti while allowing access to gather information. 

<!-- theme: info -->
>Here’s a quick guide to help align the responsibility needed to the endpoint you’re using. 
>- For a GET endpoint, the API User must have **View** responsibilities.
>- For a DELETE endpoint, the API User must have **Delete** responsibilities.
>- For a POST or PUT endpoint, the API User must have **Modify** and/or **Insert** responsibilities depending on whether you’re updating or creating entries. We recommend granting access to both unless access to one should be restricted.

![Adjust Responsibility for full access. ](../assets/images/FullAccessResponsibility.png)

**Step 4:** Select &ast; in the selected column, then select the Arrow to remove full access. 

![Remove User Group for full access. ](../assets/images/FullAccessRemoveWildcard.png)

**Step 5:** Select one of the User Groups assigned to your API User, then select the Arrow and click **OK.**

<!-- theme: info -->
>If you haven’t already created an Avanti User for the API integration, go to [API Allow Employee Access](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NzA-employee-access) for more information. 

![Save endpoint full access. ](../assets/images/FullAccessOk.png)

<!-- theme: info -->
>If you're adjusthing access and already have Client Credentials, all you'll need to do is [Reload Settings](https://avanti.stoplight.io/docs/avanti-api/45925478e011d-create-client-credentials#reload-web-settings) for your changes to take effect.  

Congratulations! You’re all done enabling access to all the endpoints. The next step to setup the API is [Create the Client Credentials.](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjgxNDM2NjY-client-credentials) 

