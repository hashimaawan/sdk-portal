# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlVzZWRCeQ


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of resource referenced |
| `Type` | `string` | Required | Type of resource referenced |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

UsedBy usedBy = new UsedBy
{
    Id = 4711,
    Type = "load_balancer",
};
```



