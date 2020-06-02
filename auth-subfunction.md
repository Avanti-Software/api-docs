# Subfunction Access

All Avanti API endpoints are secured using Subfunction Access. For an endpoint to be accessible, you must create a subfunction access rule in the Avanti Desktop Application. You may need to coordinate with the Avanti Administrator within your organization to set this up. 

## Subfunction Access Security

The view, insert, modify, and delete responsibilities on the subfunction access define the accessibility to the endpoint’s methods. 
-	To execute a GET, you must have view responsibilities
-	To execute a DELETE, you must have delete responsibilities 
-	To execute a POST or PUT, you must have modify or insert responsibilities depending on whether you are updating or inserting an entry. We recommend granting access to both unless access to one should be restricted.

For access, the Avanti User’s access to the company based on the assigned user groups must match or be higher than the responsibility level on the subfunction access. The responsibility levels range from A to Z, with A being the highest and Z being the lowest. If the responsibility level on the subfunction access is a *, all users will have access. 

The Avanti User must also have user group access to at least one of the Selected User Groups unless the Selected User Group column has a *. If it has a *, all users will have access. 

## Grant Access to an Endpoint
To grant access to a specific API endpoint, insert a subfunction access rule in the Avanti Desktop Application. Enter the full API endpoint with the prefix /api into function, then set the subfunction access security. 

![Insert subfunction access rule example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fget-personalinfo-subfunction-rule.png?alt=media&token=8069dd34-216a-44b4-a377-6f31b80f7710)

We recommend copying endpoints directly from this documentation to avoid mistakes when creating the subfunction access. Endpoints should include the version and any path parameters. Rule matching is exact, so if two endpoints only differ by path parameters, you will need to create two subfunction access rules.

![Copy endpoint example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fendpoint-url.png?alt=media&token=770ffe38-5826-43dd-a524-fe7c1fe60ad4)

## Grant Access to All Endpoints
To grant access to all endpoints, insert a subfunction access rule in the Avanti Desktop Application. Enter api/* into function, then set the subfunction access security. 

For increased security, we recommend that you do not use this option and set up subfunction access for each endpoint. 

Note: * cannot be used in the method name of any other endpoint.

![Insert catch all subfunction access rule example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fcatch-all-subfunction-rule.png?alt=media&token=4da92d68-757e-4cbb-983a-6ceed28f61df)
