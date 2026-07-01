# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`CreatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `int?` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. |
| `AssigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` |
| `AutoDelete` | `bool?` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. |
| `Datacenter` | `string` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | - |
| `Type` | [`Type51`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-51.md) | Required | Primary IP type |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

CreatePrimaryIpRequest createPrimaryIpRequest = new CreatePrimaryIpRequest
{
    AssigneeType = "server",
    Name = "my-ip",
    Type = Type51.Ipv4,
    AssigneeId = 17,
    AutoDelete = false,
    Datacenter = "fsn1-dc8",
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



