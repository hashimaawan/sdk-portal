# Load Balancer Service HTTP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIVFRQ

Configuration option for protocols http and https


# Class Name

`LoadBalancerServiceHTTP`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificates` | `List<int>` | Optional | IDs of the Certificates to use for TLS/SSL termination by the Load Balancer; empty for TLS/SSL passthrough or if `protocol` is "http" |
| `CookieLifetime` | `int?` | Optional | Lifetime of the cookie used for sticky sessions |
| `CookieName` | `string` | Optional | Name of the cookie used for sticky sessions |
| `RedirectHttp` | `bool?` | Optional | Redirect HTTP requests to HTTPS. Only available if protocol is "https". Default `false` |
| `StickySessions` | `bool?` | Optional | Use sticky sessions. Only available if protocol is "http" or "https". Default `false` |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

LoadBalancerServiceHTTP loadBalancerServiceHTTP = new LoadBalancerServiceHTTP
{
    Certificates = new List<int>
    {
        897,
    },
    CookieLifetime = 300,
    CookieName = "HCLBSTICKY",
    RedirectHttp = true,
    StickySessions = true,
};
```



