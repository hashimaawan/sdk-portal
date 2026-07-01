# Firewall 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZpcmV3YWxsNA

*This model accepts additional fields of type object.*


# Class Name

`Firewall4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewall` | `int?` | Optional | ID of the Firewall |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Firewall4 firewall4 = new Firewall4
{
    Firewall = 176,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



