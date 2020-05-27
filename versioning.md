# API Versioning

API versioning allows the Avanti API to update existing endpoints or add new ones while maintaining backwards compatibility. Once a version is finalized, the signatures of all endpoints in that version will not change going forward. Underlying functionality might change between versions but breaking changes will only be introduced if deemed necessary. The endpoint version is specified in the first segment of the endpoint URL.

```
/v{Version Number}/Endpoint
```

As an example to call version 1 of the Personal Information endpoint you would make a call to the following URL.

```
/v1/PersonalInfo
```

In the event that an existing endpoint needs to introduce a breaking change, a new major version of the endpoint will be added. Existing versions of the endpoint will continue to be available.
