# API Versioning

API versioning allows the Avanti API to update existing endpoints and add new ones while maintaining backwards compatibility. Once a version is finalized, there will be no further changes to the signatures of the endpoints. Underlying functionality might change between versions but breaking changes will only be introduced if deemed necessary. 

The endpoint version is specified in the first segment of the endpoint URL.

```
/v{Version Number}/Endpoint
```

For example, the following will call version 1 of the Personal Information endpoint.

```
/v1/PersonalInfo
```

In the event that a breaking change needs to be introdueced to an existing endpoint, a new version of the endpoint will be added. Existing versions of the endpoint will continue to be available.

