# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Required | IP range of subnet to delete |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

DeleteSubnetRequest deleteSubnetRequest = new DeleteSubnetRequest
{
    IpRange = "10.0.1.0/24",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



