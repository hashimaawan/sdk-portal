# Kubernetes Cluster User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVyVXNlcg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`KubernetesClusterUser`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Groups` | `List<string>` | Optional | A list of in-cluster groups that the user belongs to. |
| `Username` | `string` | Optional | The username for the cluster admin user. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

KubernetesClusterUser kubernetesClusterUser = new KubernetesClusterUser
{
    Groups = new List<string>
    {
        "k8saas:authenticated",
    },
    Username = "sammy@digitalocean.com",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



