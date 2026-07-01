# Public Net 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlB1YmxpY05ldDU

Public Network options

*This model accepts additional fields of type object.*


# Class Name

`PublicNet5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EnableIpv4` | `bool?` | Optional | Attach an IPv4 on the public NIC. If false, no IPv4 address will be attached. Defaults to true. |
| `EnableIpv6` | `bool?` | Optional | Attach an IPv6 on the public NIC. If false, no IPv6 address will be attached. Defaults to true. |
| `Ipv4` | `int?` | Optional | ID of the ipv4 Primary IP to use. If omitted and enable_ipv4 is true, a new ipv4 Primary IP will automatically be created. |
| `Ipv6` | `int?` | Optional | ID of the ipv6 Primary IP to use. If omitted and enable_ipv6 is true, a new ipv6 Primary IP will automatically be created. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

PublicNet5 publicNet5 = new PublicNet5
{
    EnableIpv4 = false,
    EnableIpv6 = false,
    Ipv4 = 42,
    Ipv6 = 102,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



