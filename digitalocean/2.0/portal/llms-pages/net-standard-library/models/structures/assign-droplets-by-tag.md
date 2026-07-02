# Assign Droplets by Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwRHJvcGxldHMlMjUyMGJ5JTI1MjBUYWc

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`AssignDropletsByTag`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tag` | `string` | Required | The name of a Droplet tag corresponding to Droplets assigned to the load balancer. |
| `Region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. |
| `Algorithm` | [`Algorithm?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/algorithm.md) | Optional | This field has been deprecated. You can no longer specify an algorithm for load balancers.<br><br>**Default**: `Algorithm.round_robin` |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the load balancer was created. |
| `DisableLetsEncryptDnsRecords` | `bool?` | Optional | A boolean value indicating whether to disable automatic DNS record creation for Let's Encrypt certificates that are added to the load balancer.<br><br>**Default**: `false` |
| `EnableBackendKeepalive` | `bool?` | Optional | A boolean value indicating whether HTTP keepalive connections are maintained to target Droplets.<br><br>**Default**: `false` |
| `EnableProxyProtocol` | `bool?` | Optional | A boolean value indicating whether PROXY Protocol is in use.<br><br>**Default**: `false` |
| `Firewall` | [`Firewall1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/firewall-1.md) | Optional | An object specifying allow and deny rules to control traffic to the load balancer. |
| `ForwardingRules` | [`List<ForwardingRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/forwarding-rule.md) | Required | An array of objects specifying the forwarding rules for a load balancer.<br><br>**Constraints**: *Minimum Items*: `1` |
| `HealthCheck` | [`HealthCheck1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/health-check-1.md) | Optional | An object specifying health check settings for the load balancer. |
| `HttpIdleTimeoutSeconds` | `int?` | Optional | An integer value which configures the idle timeout for HTTP requests to the target droplets.<br><br>**Default**: `60`<br><br>**Constraints**: `>= 30`, `<= 600` |
| `Id` | `Guid?` | Optional, Read-only | A unique ID that can be used to identify and reference a load balancer. |
| `Ip` | `string` | Optional, Read-only | An attribute containing the public-facing IP address of the load balancer.<br><br>**Constraints**: *Pattern*: `^$\|^((25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)\.){3}(25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)$` |
| `Name` | `string` | Optional | A human-readable name for a load balancer instance. |
| `ProjectId` | `string` | Optional | The ID of the project that the load balancer is associated with. If no ID is provided at creation, the load balancer associates with the user's default project. If an invalid project ID is provided, the load balancer will not be created. |
| `RedirectHttpToHttps` | `bool?` | Optional | A boolean value indicating whether HTTP requests to the load balancer on port 80 will be redirected to HTTPS on port 443.<br><br>**Default**: `false` |
| `Size` | [`Size2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/size-2.md) | Optional | This field has been replaced by the `size_unit` field for all regions except in AMS2, NYC2, and SFO1. Each available load balancer size now equates to the load balancer having a set number of nodes.<br><br>* `lb-small` = 1 node<br>* `lb-medium` = 3 nodes<br>* `lb-large` = 6 nodes<br><br>You can resize load balancers after creation up to once per hour. You cannot resize a load balancer within the first hour of its creation.<br><br>**Default**: `Size2.lbsmall` |
| `SizeUnit` | `int?` | Optional | How many nodes the load balancer contains. Each additional node increases the load balancer's ability to manage more connections. Load balancers can be scaled up or down, and you can change the number of nodes after creation up to once per hour. This field is currently not available in the AMS2, NYC2, or SFO1 regions. Use the `size` field to scale load balancers that reside in these regions.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `Status` | [`Status12?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-12.md) | Optional, Read-only | A status string indicating the current state of the load balancer. This can be `new`, `active`, or `errored`. |
| `StickySessions` | [`StickySessions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/sticky-sessions.md) | Optional | An object specifying sticky sessions settings for the load balancer. |
| `VpcUuid` | `Guid?` | Optional | A string specifying the UUID of the VPC to which the load balancer is assigned. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

AssignDropletsByTag assignDropletsByTag = new AssignDropletsByTag
{
    Tag = "prod:web",
    Region = Region2.Nyc3,
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
    Algorithm = Algorithm.RoundRobin,
    CreatedAt = DateTime.ParseExact("2017-02-01T22:22:58Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    DisableLetsEncryptDnsRecords = true,
    EnableBackendKeepalive = true,
    EnableProxyProtocol = true,
    HttpIdleTimeoutSeconds = 90,
    Id = new Guid("4de7ac8b-495b-4884-9a69-1050c6793cd6"),
    Ip = "104.131.186.241",
    Name = "example-lb-01",
    ProjectId = "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    RedirectHttpToHttps = true,
    Size = Size2.Lbsmall,
    SizeUnit = 3,
    Status = Status12.New,
    VpcUuid = new Guid("c33931f2-a26a-4e61-b85c-4e95a2ec431b"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



