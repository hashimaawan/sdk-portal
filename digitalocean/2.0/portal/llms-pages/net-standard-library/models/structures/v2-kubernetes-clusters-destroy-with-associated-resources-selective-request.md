# V2 Kubernetes Clusters Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing the IDs of resources to be destroyed along with their associated with a Kubernetes cluster.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancers` | `List<string>` | Optional | A list of IDs for associated load balancers to destroy along with the cluster. |
| `VolumeSnapshots` | `List<string>` | Optional | A list of IDs for associated volume snapshots to destroy along with the cluster. |
| `Volumes` | `List<string>` | Optional | A list of IDs for associated volumes to destroy along with the cluster. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest v2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest = new V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest
{
    LoadBalancers = new List<string>
    {
        "4de7ac8b-495b-4884-9a69-1050c6793cd6",
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



