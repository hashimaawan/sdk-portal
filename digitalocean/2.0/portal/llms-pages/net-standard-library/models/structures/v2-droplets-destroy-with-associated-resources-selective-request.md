# V2 Droplets Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing information about a resource to be scheduled for deletion.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIps` | `List<string>` | Optional | An array of unique identifiers for the floating IPs to be scheduled for deletion. |
| `ReservedIps` | `List<string>` | Optional | An array of unique identifiers for the reserved IPs to be scheduled for deletion. |
| `Snapshots` | `List<string>` | Optional | An array of unique identifiers for the snapshots to be scheduled for deletion. |
| `VolumeSnapshots` | `List<string>` | Optional | An array of unique identifiers for the volume snapshots to be scheduled for deletion. |
| `Volumes` | `List<string>` | Optional | An array of unique identifiers for the volumes to be scheduled for deletion. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2DropletsDestroyWithAssociatedResourcesSelectiveRequest v2DropletsDestroyWithAssociatedResourcesSelectiveRequest = new V2DropletsDestroyWithAssociatedResourcesSelectiveRequest
{
    FloatingIps = new List<string>
    {
        "6186916",
    },
    ReservedIps = new List<string>
    {
        "6186916",
    },
    Snapshots = new List<string>
    {
        "61486916",
    },
    VolumeSnapshots = new List<string>
    {
        "edb0478d-7436-11ea-86e6-0a58ac144b91",
    },
    Volumes = new List<string>
    {
        "ba49449a-7435-11ea-b89e-0a58ac14480f",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



