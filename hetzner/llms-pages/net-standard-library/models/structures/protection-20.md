# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Server from being deleted |
| `Rebuild` | `bool` | Required | If true, prevents the Server from being rebuilt |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Protection20 protection20 = new Protection20
{
    Delete = false,
    Rebuild = false,
};
```



