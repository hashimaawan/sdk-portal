# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ip` | `string` | Optional | - |
| `Network` | `int?` | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

PrivateNet privateNet = new PrivateNet
{
    Ip = "10.0.0.2",
    Network = 4711,
};
```



