# V2 Load Balancers Forwarding Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMEZvcndhcmRpbmclMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2LoadBalancersForwardingRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ForwardingRules` | [`List<ForwardingRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/forwarding-rule.md) | Required | **Constraints**: *Minimum Items*: `1` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2LoadBalancersForwardingRulesRequest v2LoadBalancersForwardingRulesRequest = new V2LoadBalancersForwardingRulesRequest
{
    ForwardingRules = new List<ForwardingRule>
    {
        new ForwardingRule
        {
            EntryPort = 443,
            EntryProtocol = EntryProtocol.Https,
            TargetPort = 80,
            TargetProtocol = TargetProtocol.Http,
            CertificateId = "892071a0-bb95-49bc-8021-3afd67a210bf",
            TlsPassthrough = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



