# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AliasIps` | `List<string>` | Required | New alias IPs to set for this Server |
| `Network` | `int` | Required | ID of an existing Network already attached to the Server |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

ServersActionsChangeAliasIpsRequest serversActionsChangeAliasIpsRequest = new ServersActionsChangeAliasIpsRequest
{
    AliasIps = new List<string>
    {
        "10.0.1.2",
    },
    Network = 4711,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



