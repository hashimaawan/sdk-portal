# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle

*This model accepts additional fields of type object.*


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Available` | `List<double>` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `AvailableForMigration` | `List<double>` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `Supported` | `List<double>` | Required | IDs of Server types that are supported in the Datacenter |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

ServerTypes serverTypes = new ServerTypes
{
    Available = new List<double>
    {
        1,
        2,
        3,
    },
    AvailableForMigration = new List<double>
    {
        1,
        2,
        3,
    },
    Supported = new List<double>
    {
        1,
        2,
        3,
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



