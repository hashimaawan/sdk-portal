# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server

*This model accepts additional fields of type object.*


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Server from being deleted |
| `Rebuild` | `bool` | Required | If true, prevents the Server from being rebuilt |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Protection20 protection20 = new Protection20
{
    Delete = false,
    Rebuild = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



