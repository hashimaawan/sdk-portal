# Health Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkhlYWx0aCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`HealthResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Dependencies` | [`List<ServiceDependency>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/service-dependency.md) | Optional | - |
| `Name` | `string` | Required | - |
| `Version` | `string` | Required | The Connect server's version |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;
using System.Collections.Generic;

HealthResponse healthResponse = new HealthResponse
{
    Name = "name4",
    Version = "version0",
    Dependencies = new List<ServiceDependency>
    {
        new ServiceDependency
        {
            Message = "message6",
            Service = "service6",
            Status = "status8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



