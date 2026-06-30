# Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0


# Class Name

`ChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool?` | Optional | If true, prevents the Floating IP from being deleted |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ChangeProtectionRequest changeProtectionRequest = new ChangeProtectionRequest
{
    Delete = true,
};
```



