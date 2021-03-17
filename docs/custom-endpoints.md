# Custom Endpoints

If none of our standard endpoints provide the required data, you can build custom endpoints using Avanti's reporting tools. Report Designer provides access to most employee-centric information and is available via the [Reporter](/avanti-api/reporter/get-report-data) endpoint.

To get started, open Report Definitions in the Avanti Desktop Application and select Insert to create a new report. Give the report a name (also known as the Report ID) and title. Now add the information you want in your endpoint as columns in the report.

![New report example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Freport-new.png?alt=media&token=c602140a-4c88-4f99-b907-82542122f0d0)

In the example above, we created a new report called **MyEndpoint** and added some employment data sources such as pay group, position, hire date and termination date. 

Next, select **Web Enabled** on the **System Access** tab. Restrict access to Print so only the API user can access the report. 

![Web enable report example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Freport-web-enabled.png?alt=media&token=6332b17e-9ba4-4cb6-97e3-accf026d79b6)

![User group permissions example.](https://firebasestorage.googleapis.com/v0/b/avanti-hcm.appspot.com/o/api-docs%2Freport-print-permissions.png?alt=media&token=222cfc40-bf4b-4bc2-b40c-1ef2ad100e94)

Once you finish creating your report and select OK to save the changes, you can start making requests to the [Reporter](/avanti-api/reporter/get-report-data) endpoint. 

When making a request, you will need to provide the Report ID to your custom report. Property names are generated based on column headers and are converted to valid camel-cased property names. For example, a column header **Employee No** would become **employeeNo**. Columns that do not have any data will exclude the property.

Based on the example above, the endpoint will return data like this:

```
GET /v1/Reporter/MyEndpoint

[
    {
        "employeeNo": "000000011",
        "payGroup": "001",
        "position": "3000",
        "active": "Y",
        "initialHireDate": "1992-03-06T00:00:00"
    },
    {
        "employeeNo": "000000012",
        "payGroup": "001",
        "position": "9001",
        "active": "Y",
        "initialHireDate": "1990-02-28T00:00:00",
        "terminationDate": "2019-08-01T00:00:00"
    },
    {
        "employeeNo": "000000013",
        "payGroup": "001",
        "position": "9001",
        "active": "Y",
        "initialHireDate": "2000-01-01T00:00:00"
    },
		...
]
```

A bad request error will occur if the request is for:
- an invalid Report ID
- a valid Report ID that the API User does not have access to print based on **Access Controls**.

```
{
    "title": "One or more validation errors occurred.",
    "status": 400,
    "errors": {
        "": [
            "Valid Report ID is required."
        ]
    }
}
```
