# V2 1 Clicks Kubernetes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMEt1YmVybmV0ZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V21ClicksKubernetesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddonSlugs` | `List<string>` | Required | An array of 1-Click Application slugs to be installed to the Kubernetes cluster. |
| `ClusterUuid` | `string` | Required | A unique ID for the Kubernetes cluster to which the 1-Click Applications will be installed. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V21ClicksKubernetesRequest v21ClicksKubernetesRequest = new V21ClicksKubernetesRequest
{
    AddonSlugs = new List<string>
    {
        "kube-state-metrics",
        "loki",
    },
    ClusterUuid = "50a994b6-c303-438f-9495-7e896cfe6b08",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



