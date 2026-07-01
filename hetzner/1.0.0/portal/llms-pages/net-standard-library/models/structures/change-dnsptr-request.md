# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`ChangeDnsptrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` |
| `Ip` | `string` | Required | IP address for which to set the reverse DNS entry |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

ChangeDnsptrRequest changeDnsptrRequest = new ChangeDnsptrRequest
{
    DnsPtr = "server02.example.com",
    Ip = "1.2.3.4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



