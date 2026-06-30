# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Available` | `List<double>` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `AvailableForMigration` | `List<double>` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `Supported` | `List<double>` | Required | IDs of Server types that are supported in the Datacenter |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
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
};
```



