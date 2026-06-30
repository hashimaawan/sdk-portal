# Change Protection Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0MQ


# Class Name

`ChangeProtectionRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool?` | Optional | If true, prevents the Network from being deleted |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ChangeProtectionRequest1 changeProtectionRequest1 = new ChangeProtectionRequest1
{
    Delete = true,
};
```



