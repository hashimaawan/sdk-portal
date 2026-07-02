# Geographical Information about an App Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdlb2dyYXBoaWNhbCUyNTIwaW5mb3JtYXRpb24lMjUyMGFib3V0JTI1MjBhbiUyNTIwYXBwJTI1MjBvcmlnaW4

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`GeographicalInformationAboutAnAppOrigin`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Continent` | `string` | Optional, Read-only | - |
| `DataCenters` | `List<string>` | Optional, Read-only | - |
| `Default` | `bool?` | Optional, Read-only | Whether or not the region is presented as the default. |
| `Disabled` | `bool?` | Optional, Read-only | - |
| `Flag` | `string` | Optional, Read-only | - |
| `Label` | `string` | Optional, Read-only | - |
| `Reason` | `string` | Optional, Read-only | - |
| `Slug` | `string` | Optional, Read-only | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

GeographicalInformationAboutAnAppOrigin geographicalInformationAboutAnAppOrigin = new GeographicalInformationAboutAnAppOrigin
{
    Continent = "europe",
    DataCenters = new List<string>
    {
        "ams",
    },
    MDefault = true,
    Disabled = true,
    Flag = "ams",
    Label = "ams",
    Reason = "to crowded",
    Slug = "basic",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



