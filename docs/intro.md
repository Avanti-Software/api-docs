# Introduction to Avanti API

Our API allows Avanti SaaS clients to access and update information in Avanti securely. Use the API to build private services that integrate Avanti with other platforms, create custom reports, display dashboards, and more.

All endpoints in the Avanti API are based on Representational State Transfer (REST) architecture and are accessed via HTTPS. The base URL for all requests is the organization’s Avanti Self-Service Portal address with a **-API** suffix. 

For example, if your Self-Service Portal is https&#58;//myavanti.ca/ABCInc, the base URL for API calls is https&#58;//myavanti.ca/ABCInc-api.

## Leveraging Avanti's API

Creating an integration requires a developer familiar with leveraging API endpoints to build your integration. If you don’t have an API developer on staff, you can involve a third-party developer. 

Regardless of whether you’re using an in-house or third-party developer, the process for integrating using an API is identical. You’ll find everything you need to provide your API Developer developer outlined in the [Getting Started](https://avanti.stoplight.io/docs/avanti-api/ZG9jOjk3NDQ0NDY-getting-started).

Avanti is continuously updating our API! We will add new endpoints to the API as we add new features in the Avanti applications. Visit [Updates](/docs/updates.md) for more information on our new API endpoints and the latest changes.

If none of our existing endpoints meet your needs, you can create endpoints using Avanti’s Reporting tools. The Reporter endpoint can access the contents of any report created in Report Designer. [Custom Endpoints](/docs/custom-endpoints.md) will walk you through setting up the report, and [Reporter](/reference/main.v1.json/paths/~1v1~1Reporter~1%7Bid%7D/get) provides details on the endpoints. 

- Version: 1.0.0
- Terms of Use: https://www.avanti.ca/api-terms-of-use 
- Privacy Policy: https://www.avanti.ca/privacy-policy

We would love to hear any feedback about your experience using the Avanti API. Please email us at [AppFeedback@avanti.ca](mailto:appfeedback@avanti.ca) to help us improve our API. 

## Need Support

Having issues using the Avanti API? Please reach out to [Avanti Support](mailto:support@avanti.ca) if you are a client requiring assistance. Before contacting support, please do your due diligence and review the API documentation in its entirety.
