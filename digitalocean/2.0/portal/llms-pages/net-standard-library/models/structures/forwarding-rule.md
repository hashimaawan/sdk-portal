# Forwarding Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZvcndhcmRpbmdSdWxl

An object specifying a forwarding rule for a load balancer.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`ForwardingRule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CertificateId` | `string` | Optional | The ID of the TLS certificate used for SSL termination if enabled. |
| `EntryPort` | `int` | Required | An integer representing the port on which the load balancer instance will listen. |
| `EntryProtocol` | [`EntryProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/entry-protocol.md) | Required | The protocol used for traffic to the load balancer. The possible values are: `http`, `https`, `http2`, `http3`, `tcp`, or `udp`. If you set the  `entry_protocol` to `udp`, the `target_protocol` must be set to `udp`.  When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. |
| `TargetPort` | `int` | Required | An integer representing the port on the backend Droplets to which the load balancer will send traffic. |
| `TargetProtocol` | [`TargetProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/target-protocol.md) | Required | The protocol used for traffic from the load balancer to the backend Droplets. The possible values are: `http`, `https`, `http2`, `tcp`, or `udp`. If you set the `target_protocol` to `udp`, the `entry_protocol` must be set to  `udp`. When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. |
| `TlsPassthrough` | `bool?` | Optional | A boolean value indicating whether SSL encrypted traffic will be passed through to the backend Droplets. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

ForwardingRule forwardingRule = new ForwardingRule
{
    EntryPort = 443,
    EntryProtocol = EntryProtocol.Https,
    TargetPort = 80,
    TargetProtocol = TargetProtocol.Http,
    CertificateId = "892071a0-bb95-49bc-8021-3afd67a210bf",
    TlsPassthrough = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



