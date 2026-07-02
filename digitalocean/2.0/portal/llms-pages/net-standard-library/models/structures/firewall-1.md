# Firewall 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZpcmV3YWxsMQ

An object specifying allow and deny rules to control traffic to the load balancer.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Firewall1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Allow` | `List<string>` | Optional | the rules for allowing traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') |
| `Deny` | `List<string>` | Optional | the rules for denying traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Firewall1 firewall1 = new Firewall1
{
    Allow = new List<string>
    {
        "ip:1.2.3.4",
        "cidr:2.3.0.0/16",
    },
    Deny = new List<string>
    {
        "ip:1.2.3.4",
        "cidr:2.3.0.0/16",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



