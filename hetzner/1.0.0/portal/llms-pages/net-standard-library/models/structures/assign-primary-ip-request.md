# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`AssignPrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `int` | Required | ID of a resource of type `assignee_type` |
| `AssigneeType` | `string` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `"server"` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

AssignPrimaryIpRequest assignPrimaryIpRequest = new AssignPrimaryIpRequest
{
    AssigneeId = 4711,
    AssigneeType = "server",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



