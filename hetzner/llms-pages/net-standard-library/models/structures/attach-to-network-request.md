# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q


# Class Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AliasIps` | `List<string>` | Optional | Additional IPs to be assigned to this Server |
| `Ip` | `string` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address |
| `Network` | `int` | Required | ID of an existing network to attach the Server to |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

AttachToNetworkRequest attachToNetworkRequest = new AttachToNetworkRequest
{
    Network = 4711,
    AliasIps = new List<string>
    {
        "10.0.1.2",
    },
    Ip = "10.0.1.1",
};
```



