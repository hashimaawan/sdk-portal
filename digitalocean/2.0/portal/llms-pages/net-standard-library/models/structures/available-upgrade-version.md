# Available Upgrade Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkF2YWlsYWJsZVVwZ3JhZGVWZXJzaW9u

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`AvailableUpgradeVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `KubernetesVersion` | `string` | Optional | The upstream version string for the version of Kubernetes provided by a given slug. |
| `Slug` | `string` | Optional | The slug identifier for an available version of Kubernetes for use when creating or updating a cluster. The string contains both the upstream version of Kubernetes as well as the DigitalOcean revision. |
| `SupportedFeatures` | `List<string>` | Optional | The features available with the version of Kubernetes provided by a given slug. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

AvailableUpgradeVersion availableUpgradeVersion = new AvailableUpgradeVersion
{
    KubernetesVersion = "1.16.13",
    Slug = "1.16.13-do.0",
    SupportedFeatures = new List<string>
    {
        "cluster-autoscaler",
        "docr-integration",
        "token-authentication",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



