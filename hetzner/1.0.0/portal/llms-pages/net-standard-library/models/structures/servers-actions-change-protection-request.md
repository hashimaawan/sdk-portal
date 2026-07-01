# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool?` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) |
| `Rebuild` | `bool?` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

ServersActionsChangeProtectionRequest serversActionsChangeProtectionRequest = new ServersActionsChangeProtectionRequest
{
    Delete = true,
    Rebuild = true,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



