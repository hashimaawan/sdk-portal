# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AliasIps` | `List<string>` | Required | New alias IPs to set for this Server |
| `Network` | `int` | Required | ID of an existing Network already attached to the Server |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ServersActionsChangeAliasIpsRequest serversActionsChangeAliasIpsRequest = new ServersActionsChangeAliasIpsRequest
{
    AliasIps = new List<string>
    {
        "10.0.1.2",
    },
    Network = 4711,
};
```



