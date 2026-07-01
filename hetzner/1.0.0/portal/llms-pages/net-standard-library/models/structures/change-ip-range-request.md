# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`ChangeIpRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Required | The new prefix for the whole Network |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

ChangeIpRangeRequest changeIpRangeRequest = new ChangeIpRangeRequest
{
    IpRange = "10.0.0.0/12",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



