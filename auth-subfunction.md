# Subfunction Access

All Avanti API endpoints are secured using Avanti’s Subfunction Access. For an endpoint to be accessible, a subfunction access rule must be defined.

When defining a subfunction rule, the full API endpoint is the function name prefixed by **/api**. The subfunction’s view, insert, modify and delete responsibilities define the accessibility to the endpoint's methods. To execute a GET you must have view responsibilities, to execute a DELETE you must have delete responsibilities and to execute a POST or PUT you must have modify and or insert responsibilities.

![Insert subfunction access rule example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fget-personalinfo-subfunction-rule.png?alt=media&token=8069dd34-216a-44b4-a377-6f31b80f7710)

We recommend that you copy endpoints directly from the [Avanti API Reference](/avanti-api) to avoid mistakes when creating your subfunction rules. Endpoints should include the version and any path parameters. Rule matching is exact so if two endpoints only differ by path parameters a rule will be needed for each.

![Copy endpoint example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fendpoint-url.png?alt=media&token=770ffe38-5826-43dd-a524-fe7c1fe60ad4)

To give full access to all endpoints you can create a API wildcard rule using the function name **api/\***. This rule is specific and a \* cannot be used as wildcard in the method name for other endpoints.

![Insert catch all subfunction access rule example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Fcatch-all-subfunction-rule.png?alt=media&token=4da92d68-757e-4cbb-983a-6ceed28f61df)
