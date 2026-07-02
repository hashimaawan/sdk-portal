# V2 Databases Maintenance Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME1haW50ZW5hbmNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DatabasesMaintenanceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Day` | `string` | Required | The day of the week on which to apply maintenance updates. |
| `Description` | `List<string>` | Optional, Read-only | A list of strings, each containing information about a pending maintenance update. |
| `Hour` | `string` | Required | The hour in UTC at which maintenance updates will be applied in 24 hour format. |
| `Pending` | `bool?` | Optional, Read-only | A boolean value indicating whether any maintenance is scheduled to be performed in the next window. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2DatabasesMaintenanceRequest v2DatabasesMaintenanceRequest = new V2DatabasesMaintenanceRequest
{
    Day = "tuesday",
    Hour = "14:00",
    Description = new List<string>
    {
        "Update TimescaleDB to version 1.2.1",
        "Upgrade to PostgreSQL 11.2 and 10.7 bugfix releases",
    },
    Pending = true,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



