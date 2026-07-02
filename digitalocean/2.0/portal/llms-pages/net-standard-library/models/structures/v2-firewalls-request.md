# V2 Firewalls Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2FirewallsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. |
| `DropletIds` | `List<int>` | Optional | An array containing the IDs of the Droplets assigned to the firewall. |
| `Id` | `string` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. |
| `Name` | `string` | Required | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` |
| `PendingChanges` | [`List<PendingChange>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. |
| `Status` | [`Status9?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". |
| `Tags` | `List<string>` | Optional | - |
| `InboundRules` | [`List<InboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/inbound-rule.md) | Required | - |
| `OutboundRules` | [`List<OutboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/outbound-rule.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2FirewallsRequest v2FirewallsRequest = new V2FirewallsRequest
{
    Name = "firewall",
    InboundRules = new List<InboundRule>
    {
        new InboundRule
        {
            Ports = "8000",
            Protocol = Protocol.Tcp,
            Sources = new Sources
            {
                Addresses = new List<string>
                {
                    "1.2.3.4",
                    "18.0.0.0/8",
                },
                DropletIds = new List<int>
                {
                    8043964,
                },
                KubernetesIds = new List<string>
                {
                    "41b74c5d-9bd0-5555-5555-a57c495b81a3",
                },
                LoadBalancerUids = new List<string>
                {
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                },
                Tags = new List<string>
                {
                    "tags1",
                    "tags2",
                    "tags3",
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    OutboundRules = new List<OutboundRule>
    {
        new OutboundRule
        {
            Ports = "8000",
            Protocol = Protocol.Tcp,
            Destinations = new Destinations
            {
                Addresses = new List<string>
                {
                    "1.2.3.4",
                    "18.0.0.0/8",
                },
                DropletIds = new List<int>
                {
                    8043964,
                },
                KubernetesIds = new List<string>
                {
                    "41b74c5d-9bd0-5555-5555-a57c495b81a3",
                },
                LoadBalancerUids = new List<string>
                {
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                },
                Tags = new List<string>
                {
                    "tags7",
                    "tags8",
                    "tags9",
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    CreatedAt = DateTime.ParseExact("2020-05-23T21:24:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    DropletIds = new List<int>
    {
        8043964,
    },
    Id = "bb4b2611-3d72-467b-8602-280330ecd65c",
    PendingChanges = new List<PendingChange>
    {
        new PendingChange
        {
            DropletId = 8043964,
            Removing = false,
            Status = "waiting",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Status = Status9.Waiting,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



