# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerType` | `string` | Required | ID or name of Server type the Server should migrate to |
| `UpgradeDisk` | `bool` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

ServersActionsChangeTypeRequest serversActionsChangeTypeRequest = new ServersActionsChangeTypeRequest
{
    ServerType = "cx11",
    UpgradeDisk = true,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



