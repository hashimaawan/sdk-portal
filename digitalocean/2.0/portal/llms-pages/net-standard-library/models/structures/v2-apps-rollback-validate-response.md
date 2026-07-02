# V2 Apps Rollback Validate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSb2xsYmFjayUyNTIwVmFsaWRhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsRollbackValidateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/error.md) | Optional | - |
| `Valid` | `bool?` | Optional | Indicates whether the app can be rolled back to the specified deployment. |
| `Warnings` | [`List<Warning>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/warning.md) | Optional | Contains a list of warnings that may cause the rollback to run under unideal circumstances. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2AppsRollbackValidateResponse v2AppsRollbackValidateResponse = new V2AppsRollbackValidateResponse
{
    Error = new Error
    {
        Code = Code.IncompatiblePhase,
        Components = new List<string>
        {
            "components3",
        },
        Message = "message4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Valid = false,
    Warnings = new List<Warning>
    {
        new Warning
        {
            Code = Code.ExceededRevisionLimit,
            Components = new List<string>
            {
                "components3",
            },
            Message = "message4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Warning
        {
            Code = Code.ExceededRevisionLimit,
            Components = new List<string>
            {
                "components3",
            },
            Message = "message4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



