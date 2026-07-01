# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRuc1B0cg

*This model accepts additional fields of type object.*


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `Ip` | `string` | Required | Single IPv4 or IPv6 address |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

DnsPtr dnsPtr = new DnsPtr
{
    DnsPtrProp = "server.example.com",
    Ip = "2001:db8::1",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



