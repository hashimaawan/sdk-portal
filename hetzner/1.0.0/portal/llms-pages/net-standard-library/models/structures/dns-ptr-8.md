# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRuc1B0cjg

*This model accepts additional fields of type object.*


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `Ip` | `string` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

DnsPtr8 dnsPtr8 = new DnsPtr8
{
    DnsPtr = "server.example.com",
    Ip = "2001:db8::1",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



