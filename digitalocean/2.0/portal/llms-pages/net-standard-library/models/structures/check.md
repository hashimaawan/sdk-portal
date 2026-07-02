# Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNoZWNr

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Check`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `Guid?` | Optional, Read-only | A unique ID that can be used to identify and reference the check. |
| `Enabled` | `bool?` | Optional | A boolean value indicating whether the check is enabled/disabled.<br><br>**Default**: `true` |
| `Name` | `string` | Optional | A human-friendly display name. |
| `Regions` | [`List<Region8>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/region-8.md) | Optional | An array containing the selected regions to perform healthchecks from. |
| `Target` | `string` | Optional | The endpoint to perform healthchecks on. |
| `Type` | [`Type19?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-19.md) | Optional | The type of health check to perform. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Check check = new Check
{
    Id = new Guid("5a4981aa-9653-4bd1-bef5-d6bff52042e4"),
    Enabled = true,
    Name = "Landing page check",
    Regions = new List<Region8>
    {
        Region8.UsEast,
        Region8.EuWest,
    },
    Target = "https://www.landingpage.com",
    Type = Type19.Https,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



