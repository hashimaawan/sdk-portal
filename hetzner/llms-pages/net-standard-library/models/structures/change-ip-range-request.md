# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0


# Class Name

`ChangeIPRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Required | The new prefix for the whole Network |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ChangeIPRangeRequest changeIPRangeRequest = new ChangeIPRangeRequest
{
    IpRange = "10.0.0.0/12",
};
```



