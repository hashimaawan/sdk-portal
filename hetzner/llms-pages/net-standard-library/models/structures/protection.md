# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource


# Class Name

`Protection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Resource from being deleted |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Protection protection = new Protection
{
    Delete = false,
};
```



