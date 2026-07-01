# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0

*This model accepts additional fields of type object.*


# Class Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AliasIps` | `List<string>` | Optional | - |
| `Ip` | `string` | Optional | - |
| `MacAddress` | `string` | Optional | - |
| `Network` | `int?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

PrivateNet4 privateNet4 = new PrivateNet4
{
    AliasIps = new List<string>
    {
        "alias_ips0",
        "alias_ips9",
    },
    Ip = "10.0.0.2",
    MacAddress = "86:00:ff:2a:7d:e1",
    Network = 4711,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



