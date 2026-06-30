# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg


# Class Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool?` | Optional | If true, prevents the Primary IP from being deleted |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ChangeProtectionRequest2 changeProtectionRequest2 = new ChangeProtectionRequest2
{
    Delete = true,
};
```



