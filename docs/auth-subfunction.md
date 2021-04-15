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
>If you haven’t already created an Avanti User for the API integration, go to **API Allow Employee Access** for more information. **Marketing Please add the link.** 

## Grant Access to an Endpoint

To grant access to a specific API endpoint, you’ll first need to identify the endpoint from the Avanti API Documentation. **Liz, find the Link **


![Endpoint.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fget-personalinfo-subfunction-rule.png?alt=media&token=8069dd34-216a-44b4-a377-6f31b80f7710)

Once you’ve identified the endpoint, you’ll be able to grant access. We recommend copying and pasting endpoints from the documentation to avoid mistakes when creating the subfunction access. When copying, be sure to exclude any path parameter; path parameters are anything with **/{  }**.  

For example, entering **api/v1/Dependents** in the subfunction access grants access to both these endpoints, which differ by the path parameter /{empNo}:  
![Both endpoints.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fget-personalinfo-subfunction-rule.png?alt=media&token=8069dd34-216a-44b4-a377-6f31b80f7710)


**Step 1:** Select **Insert** in Subfunction Access Controls.
By default, this can be found in System Administration >> System Access Controls on the Avanti Desktop Application.

**Step 2:** Add **api** in **Function**.

**Step 3:** Add the copied endpoint from the **API Documentation**.

<!-- theme: info -->
>The copied text should start with the version, such as /v1. If it ends in a parameter, such as /{empNo}, ensure it’s **excluded**. 

**Step 4:** Add a **Description** for the endpoint. 

**Step 5:** Set your desired Responsibility to **Insert, Modify (edit), View** and **Delete** using the endpoint. 

- To allow the API to insert, modify, view, and delete, skip to Step 8. 
- To prevent the API from having access, replace the &ast; with a - in the Responsibility. 

For example, I want to use an endpoint to gather dependent information from Avanti. I could have a &ast; for View and a - for Insert, Modify and Delete. This prevents the API from adding, editing, and deleting dependents in Avanti while allowing access to view the dependent information. 
<!-- theme: info -->
>Here’s a quick guide to help align the responsibility needed to the endpoint you’re using. 
>- For a GET endpoint, the API User must have **View** responsibilities.
>- For a DELETE endpoint, the API User must have **Delete** responsibilities.
>- For a POST or PUT endpoint, the API User must have **Modify** and/or **Insert** responsibilities depending on whether you’re updating or creating entries. We recommend granting access to both unless access to one should be restricted.

**Step 6:** Select &ast; in the selected column, then select the Arrow to remove full access. 

**Step 7:** Select one of the User Groups assigned to your API User, then select the Arrow.  

<!-- theme: info -->
>If you haven’t already created an Avanti User for the API integration, go to API Allow Employee Access for more information. **Marketing Please add the link.**

**Step 8:** Select **OK** to save. 

Congratulations! You’re done enabling access to the endpoint. Repeat these steps for every endpoint you’ll use in the integration.

The next step to setup the API is Create the Client Credentials.  **Marketing Please add the link.**

## Grant Access to All Endpoints

To grant access to all endpoints, insert a subfunction access rule in the Avanti Desktop Application. 

<!-- theme: warning -->
>For maximum security, we recommend you do not use this option; it allows the API integration access to all your employees' information. Instead, set up subfunction access for every endpoint you’re using for your integrations.

**Step 1:** Select **Insert** in Subfunction Access Controls.
By default, this can be found in System Administration >> System Access Controls on the Avanti Desktop Application.

**Step 2:** Add **api/&ast; ** in Function.

**Step 3:** Add a **Description** for the endpoint, such as Access to API Endpoints.  

**Step 4:** Set the Responsibility to **Insert, Modify (edit), View** and **Delete** using the endpoint. 

- To allow full access to insert, modify, view, and delete, skip to Step 7. 
- To prevent the API  from having access, replace the &ast; with a - in the Responsibility. For example, I want to use the API to gather information from Avanti. I could have a &ast; for view and - for Insert, Modify and Delete. This prevents the API from adding, editing or deleting information in Avanti while allowing access to gather information. 

<!-- theme: info -->
>Here’s a quick guide to help align the responsibility needed to the endpoint you’re using. 
>- For a GET endpoint, the API User must have **View** responsibilities.
>- For a DELETE endpoint, the API User must have **Delete** responsibilities.
>- For a POST or PUT endpoint, the API User must have **Modify** and/or **Insert** responsibilities depending on whether you’re updating or creating entries. We recommend granting access to both unless access to one should be restricted.

**Step 5:** Select &ast; in the selected column, then select the Arrow to remove full access. 

**Step 6:** Select one of the User Groups assigned to your API User, then select the Arrow.  

<!-- theme: info -->
>If you haven’t already created an Avanti User for the API integration, go to API Allow Employee Access for more information. **Marketing Please add the link.**

**Step 7:** Select **OK** to save. 

Congratulations! You’re all done enabling access to all the endpoints. The next step to setup the API is Create the Client Credentials.  **Marketing Please add the link.**








## Keeping the original 


![Insert subfunction access rule example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fget-personalinfo-subfunction-rule.png?alt=media&token=8069dd34-216a-44b4-a377-6f31b80f7710)


We recommend copying endpoints directly from this documentation to avoid mistakes when creating the subfunction access. Endpoints should include the version and any path parameters. Rule matching is exact, so if two endpoints only differ by path parameters, you will need to create two subfunction access rules.

![Copy endpoint example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fendpoint-url.png?alt=media&token=770ffe38-5826-43dd-a524-fe7c1fe60ad4)

## Grant Access to All Endpoints

To grant access to all endpoints, insert a subfunction access rule in the Avanti Desktop Application. By default, you can find Subfunction Access in the System Administration >> System Access Controls. 

Enter api/* into function, then set the subfunction access security. 

For increased security, we recommend that you do not use this option and set up subfunction access for each endpoint. 

Note: * cannot be used in the method name of any other endpoint.

![Insert catch all subfunction access rule example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fcatch-all-subfunction-rule.png?alt=media&token=4da92d68-757e-4cbb-983a-6ceed28f61df)
